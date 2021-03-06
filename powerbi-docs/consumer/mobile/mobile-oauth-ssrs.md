---
title: Uso di OAuth per la connessione al Server di report di Power BI e a SSRS
description: Informazioni su come configurare l'ambiente per supportare l'autenticazione OAuth con l'app Power BI per dispositivi mobili e connettersi a SQL Server Reporting Services 2016 o versioni successive.
author: markingmyname
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-mobile
ms.topic: conceptual
ms.date: 06/07/2018
ms.author: maghan
ms.openlocfilehash: a03870fd0443a00803edceb5d4821161ccb7693a
ms.sourcegitcommit: d8109b605052096fc0eb613f2a1340570b99b2f5
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/23/2018
ms.locfileid: "49651035"
---
# <a name="using-oauth-to-connect-to-power-bi-report-server-and-ssrs"></a>Uso di OAuth per la connessione al Server di report di Power BI e a SSRS
Informazioni su come configurare l'ambiente per supportare l'autenticazione OAuth con l'app Power BI per dispositivi mobili e connettersi a Server di report di Microsoft Power BI e a SQL Server Reporting Services 2016 o versioni successive.

![](media/mobile-oauth-ssrs/powerbi-mobile-oauth.png)

È possibile usare OAuth per connettersi al Server di report di Power BI e a Reporting Services e visualizzare report per dispositivi mobili o indicatori KPI. Per consentire questo tipo di autenticazione, Windows Server 2016 offre alcuni miglioramenti per il ruolo di Proxy applicazione Web.

   > [!NOTE]
   > La visualizzazione dei report di Power BI ospitati nel Server di report di Power BI che usano WAP per l'autenticazione non è al momento supportata ufficialmente.

## <a name="requirements"></a>Requisiti
Windows Server 2016 è necessario per i server Proxy applicazione Web (WAP) e Active Directory Federation Services (ADFS). Non è necessario avere un dominio di livello funzionale di Windows 2016.

## <a name="domain-name-services-dns-configuration"></a>Configurazione Domain Name Services (DNS)
È necessario determinare a quale URL pubblico si connetterà l'app Power BI per dispositivi mobili. Ad esempio, potrebbe essere simile a quello indicato di seguito.

```
https://reports.contoso.com
```

È necessario indirizzare il record DNS per i **report** all'indirizzo IP pubblico del server Proxy applicazione Web (WAP). Sarà anche necessario configurare un record DNS pubblico per il server ADFS. Il server ADFS, ad esempio, potrebbe essere stato configurato con l'URL seguente.

```
https://fs.contoso.com
```

È necessario indirizzare il record DNS per i **fs** all'indirizzo IP pubblico del server Proxy applicazione Web (WAP), perché verrà pubblicato come parte dell'applicazione WAP.

## <a name="certificates"></a>Certificati
È necessario configurare i certificati per l'applicazione WAP e il server ADFS. Entrambi questi certificati devono essere parte di un'autorità di certificazione valida e riconosciuta dai dispositivi mobili.

## <a name="reporting-services-configuration"></a>Configurazione di Reporting Services
Per quanto riguarda Reporting Services, non c'è molto da configurare. È sufficiente assicurarsi di avere un nome dell'entità servizio (SPN) valido per abilitare l'autenticazione Kerberos corretta e che il server di Reporting Services sia abilitato per la negoziazione dell'autenticazione.

### <a name="service-principal-name-spn"></a>Nome dell'entità servizio (SPN)
Il nome dell'entità servizio (SPN) è un identificatore univoco per un servizio che usa l'autenticazione Kerberos. È necessario assicurarsi di avere un nome SPN HTTP corretto per il server di report.

Per informazioni su come configurare il corretto nome dell'entità servizio (SPN) per il server di report, vedere [Registrare un nome dell'entità servizio (SPN) per un server di report](https://msdn.microsoft.com/library/cc281382.aspx).

### <a name="enabling-negotiate-authentication"></a>Abilitare la negoziazione dell'autenticazione
Per abilitare l'uso dell'autenticazione Kerberos in un server di report è necessario configurare il tipo di autenticazione del server di report come RSWindowsNegotiate. Questa operazione viene eseguita all'interno del file rsreportserver.config.

```
<AuthenticationTypes>  
    <RSWindowsNegotiate />  
    <RSWindowsKerberos />  
    <RSWindowsNTLM />  
</AuthenticationTypes>
```

Per altre informazioni, vedere [Modificare un file di configurazione di Reporting Services](https://msdn.microsoft.com/library/bb630448.aspx) e [Configurare l'autenticazione di Windows nel server di report](https://msdn.microsoft.com/library/cc281253.aspx).

## <a name="active-directory-federation-services-adfs-configuration"></a>Configurazione di Active Directory Federation Services (ADFS)
È necessario configurare ADFS in un server Windows 2016 all'interno dell'ambiente. Questa operazione può essere eseguita usando Server Manager e selezionando Aggiungi ruoli e funzionalità in Gestione. Per altre informazioni, vedere [Active Directory Federation Services](https://technet.microsoft.com/windows-server-docs/identity/active-directory-federation-services).

### <a name="create-an-application-group"></a>Creare un gruppo di applicazioni
All'interno della schermata di gestione di ADFS, è consigliabile creare un gruppo di applicazioni per Reporting Services, che includerà informazioni per le app Power BI per dispositivi mobili.

È possibile creare il gruppo di applicazioni con i passaggi seguenti.

1. All'interno dell'app di gestione di ADFS, fare clic con il pulsante destro del mouse su **Gruppi di applicazioni** e selezionare **Aggiungi gruppo di applicazioni…**
   
   ![](media/mobile-oauth-ssrs/adfs-add-application-group.png)
2. Nell'aggiunta guidata del gruppo di applicazioni, fornire un **nome** per il gruppo di applicazioni e selezionare **Applicazione nativa che accede a un'API Web**.
   
   ![](media/mobile-oauth-ssrs/adfs-application-group-wizard1.png)
3. Fare clic su **Avanti**.
4. Fornire un **nome** per l'applicazione che si sta aggiungendo. 
5. Mentre il **ID client** verrà generato automaticamente, immettere *484d54fc-b481-4eee-9505-0258a1913020* per iOS e Android.
6. È consigliabile aggiungere i seguenti **gli URL di reindirizzamento**:
   
   **Voci per Power BI per dispositivi mobili - iOS:**  
   msauth://code/mspbi-adal://com.microsoft.powerbimobile  
   msauth://code/mspbi-adalms://com.microsoft.powerbimobilems  
   mspbi-adal://com.microsoft.powerbimobile  
   mspbi-adalms://com.microsoft.powerbimobilems
   
   **Le app Android necessitano solo degli elementi seguenti:**  
   urn:ietf:wg:oauth:2.0:oob
   
   ![](media/mobile-oauth-ssrs/adfs-application-group-wizard2.png)
7. Fare clic su **Avanti**.
8. Fornire l'URL del server di report. Questo è l'URL esterno che raggiungerà il Proxy di applicazione Web. Deve essere nel formato seguente.
   
   > [!NOTE]
   > L'URL rispetta la distinzione tra maiuscole e minuscole.
   > 
   > 
   
   *https://<url to report server>/reports*
   
   ![](media/mobile-oauth-ssrs/adfs-application-group-wizard3.png)
9. Fare clic su **Avanti**.
10. Scegliere i **Criteri di controllo di accesso** idonei alle esigenze della propria organizzazione.
    
    ![](media/mobile-oauth-ssrs/adfs-application-group-wizard4.png)
11. Fare clic su **Avanti**.
12. Fare clic su **Avanti**.
13. Fare clic su **Avanti**.
14. Selezionare **Chiudi**.

Al termine, le proprietà del gruppo di applicazioni avranno un aspetto simile al seguente.

![](media/mobile-oauth-ssrs/adfs-application-group.png)

## <a name="web-application-proxy-wap-configuration"></a>Configurazione del Proxy applicazione Web (WAP)
È consigliabile abilitare il ruolo di Proxy applicazione Web Windows in un server nell'ambiente in uso. Deve essere in un server Windows 2016. Per altre informazioni, vedere [Proxy di applicazione Web in Windows Server 2016](https://technet.microsoft.com/windows-server-docs/identity/web-application-proxy/web-application-proxy-windows-server) e [Pubblicazione di applicazioni con la preautenticazione di ADFS](https://technet.microsoft.com/windows-server-docs/identity/web-application-proxy/publishing-applications-using-ad-fs-preauthentication#a-namebkmk14apublish-an-application-that-uses-oauth2-such-as-a-windows-store-app).

### <a name="constrained-delegation-configuration"></a>Configurazione della delega vincolata
Per passare dall'autenticazione OAuth all'autenticazione di Windows, è necessario usare la delega vincolata con transizione del protocollo. Fa parte della configurazione di Kerberos. È già stato definito il nome SPN di Reporting Services all'interno della configurazione di Reporting Services.

È necessario configurare la delega vincolata nell'account del computer Server WAP all'interno di Active Directory. Potrebbe essere necessario collaborare con un amministratore di dominio se non si hanno i diritti per Active Directory.

Per configurare la delega vincolata, si dovranno eseguire le operazioni seguenti.

1. Sul computer in cui sono installati gli strumenti di Active Directory, avviare **Utenti e computer di Active Directory**.
2. Trovare l'account del computer per il server WAP. Per impostazione predefinita, si troverà nel contenitore computer.
3. Fare clic con il pulsante destro sul server WAP e passare a **Proprietà**.
4. Selezionare la scheda **Delega**.
5. Selezionare **Computer attendibile per la delega solo ai servizi specificati** e quindi **Utilizza un qualsiasi protocollo di autenticazione**.
   
   ![](media/mobile-oauth-ssrs/wap-contrained-delegation1.png)
   
   Consente di impostare una delega vincolata per l'account di computer Server WAP. È quindi necessario specificare i servizi che questo computer è autorizzato a delegare.
6. Selezionare **Aggiungi…** nella casella Servizi.
   
   ![](media/mobile-oauth-ssrs/wap-contrained-delegation2.png)
7. Selezionare **Utenti o computer…**
8. Immettere l'account del servizio che si sta usando per Reporting Services. Si tratta dell'account a cui è stato aggiunto il nome SPN all'interno della configurazione di Reporting Services.
9. Selezionare il nome SPN per Reporting Services e quindi **OK**.
   
   > [!NOTE]
   > Potrebbe essere visualizzato solo il nome SPN di NetBIOS. Se esistono entrambi, verranno effettivamente selezionati i nomi SPN di NetBIOS e FQDN.
   > 
   > 
   
   ![](media/mobile-oauth-ssrs/wap-contrained-delegation3.png)
10. Il risultato dovrebbe essere simile al seguente quando la casella di controllo **Espansa** è selezionata.
    
    ![](media/mobile-oauth-ssrs/wap-contrained-delegation4.png)
11. Selezionare **OK**.

### <a name="add-wap-application"></a>Aggiungere applicazione WAP
Mentre è possibile pubblicare applicazioni nella console di gestione di accesso ai report, è consigliabile creare l'applicazione con PowerShell. Ecco il comando per aggiungere l'applicazione.

```
Add-WebApplicationProxyApplication -Name "Contoso Reports" -ExternalPreauthentication ADFS -ExternalUrl https://reports.contoso.com/reports/ -ExternalCertificateThumbprint "0ff79c75a725e6f67e3e2db55bdb103efc9acb12" -BackendServerUrl http://ContosoSSRS/reports/ -ADFSRelyingPartyName "Reporting Services - Web API" -BackendServerAuthenticationSPN "http/ContosoSSRS.contoso.com" -UseOAuthAuthentication
```

| Parametro | Commenti |
| --- | --- |
| **ADFSRelyingPartyName** |Questo è il nome dell'API Web che è stato creato come parte del gruppo di applicazioni all'interno di ADFS. |
| **ExternalCertificateThumbprint** |Questo è il certificato da usare per gli utenti esterni. È importante che il certificato sia valido per i dispositivi mobili e provenga da un'autorità di certificazione attendibile. |
| **BackendServerUrl** |Si tratta dell'URL per il server di report dal server WAP. Se il server WAP è in una rete perimetrale, è necessario usare un nome di dominio completo. Assicurarsi che sia possibile raggiungere l'URL dal browser Web nel server WAP. |
| **BackendServerAuthenticationSPN** |Questo è il nome SPN che è stato creato come parte della configurazione di Reporting Services. |

### <a name="setting-integrated-authentication-for-the-wap-application"></a>Impostazione dell'autenticazione integrata per l'applicazione WAP
Dopo aver aggiunto l'applicazione WAP, è necessario impostare BackendServerAuthenticationMode in modo da usare IntegratedWindowsAuthentication. A tale scopo, è necessario l'ID dell'applicazione WAP.

```
Get-WebApplicationProxyApplication “Contoso Reports” | fl
```

![](media/mobile-oauth-ssrs/wap-application-id.png)

Eseguire il comando seguente per impostare il nome BackendServerAuthenticationMode usando l'ID dell'applicazione WAP.

```
Set-WebApplicationProxyApplication -id 30198C7F-DDE4-0D82-E654-D369A47B1EE5 -BackendServerAuthenticationMode IntegratedWindowsAuthentication
```

![](media/mobile-oauth-ssrs/wap-application-backendauth.png)

## <a name="connecting-with-the-power-bi-mobile-app"></a>Connessione con l'app Power BI per dispositivi mobili
All'interno dell'app Power BI per dispositivi mobili è consigliabile connettersi all'istanza di Reporting Services. A tale scopo, specificare l'**URL esterno** per l'applicazione WAP.

![](media/mobile-oauth-ssrs/powerbi-mobile-app1.png)

Quando si seleziona **Connect**, si verrà indirizzati alla pagina di accesso di ADFS. Immettere le credenziali valide per il dominio.

![](media/mobile-oauth-ssrs/powerbi-mobile-app2.png)

Dopo aver selezionato **Accedi**, verranno visualizzati gli elementi dal server di Reporting Services.

![](media/mobile-oauth-ssrs/powerbi-mobile-app2.png)

## <a name="multi-factor-authentication"></a>Multi-Factor Authentication
È possibile abilitare Multi-Factor Authentication per applicare una protezione aggiuntiva per l'ambiente. Per altre informazioni, vedere [Configurare AD FS 2016 e Azure MFA](https://technet.microsoft.com/windows-server-docs/identity/ad-fs/operations/configure-ad-fs-2016-and-azure-mfa).

## <a name="troubleshooting"></a>Risoluzione dei problemi

### <a name="you-receive-the-error-failed-to-login-to-ssrs-server-please-verify-server-configuration"></a>Viene visualizzato l'errore Non è stato possibile connettersi al server SSRS. Verificare la configurazione server.

![](media/mobile-oauth-ssrs/powerbi-mobile-error.png)

È possibile impostare [Fiddler](http://www.telerik.com/fiddler) in modo che funga da proxy per i dispositivi mobili e visualizzi l'avanzamento della richiesta. Per abilitare un proxy di Fiddler per il dispositivo telefonico, è necessario configurare [CertMaker per iOS e Android](http://www.telerik.com/fiddler/add-ons) nel computer che esegue Fiddler. Si tratta di un componente aggiuntivo da Telerik per Fiddler.

Se l'accesso funziona correttamente quando si usa Fiddler, potrebbe essere un problema di certificato con l'applicazione WAP o il server ADFS. È possibile usare uno strumento come [Microsoft Message Analyzer](https://www.microsoft.com/download/details.aspx?id=44226) per verificare che i certificati siano validi.

## <a name="next-steps"></a>Passaggi successivi
[Registrare un nome dell'entità servizio (SPN) per un server di report](https://msdn.microsoft.com/library/cc281382.aspx)  
[Modificare un file di configurazione di Reporting Services](https://msdn.microsoft.com/library/bb630448.aspx)  
[Configurare l'autenticazione di Windows in un server di report](https://msdn.microsoft.com/library/cc281253.aspx)  
[Active Directory Federation Services](https://technet.microsoft.com/windows-server-docs/identity/active-directory-federation-services)  
[Proxy applicazione Web in Windows Server 2016](https://technet.microsoft.com/windows-server-docs/identity/web-application-proxy/web-application-proxy-windows-server)  
[Pubblicazione di applicazioni usando la preautenticazione di ADFS](https://technet.microsoft.com/windows-server-docs/identity/web-application-proxy/publishing-applications-using-ad-fs-preauthentication#a-namebkmk14apublish-an-application-that-uses-oauth2-such-as-a-windows-store-app)  
[Configurare AD FS 2016 e Azure MFA](https://technet.microsoft.com/windows-server-docs/identity/ad-fs/operations/configure-ad-fs-2016-and-azure-mfa)  
Altre domande? [Provare la community di Power BI](http://community.powerbi.com/)

