---
title: Incorporare con web part report in SharePoint Online
description: Con la nuova web part report di Power BI per SharePoint Online è possibile incorporare facilmente report interattivi di Power BI nelle pagine di SharePoint Online.
author: markingmyname
ms.author: maghan
manager: kfile
ms.reviewer: ''
featuredvideoid: ''
ms.service: powerbi
ms.component: powerbi-service
ms.topic: conceptual
LocalizationGroup: Share your work
ms.date: 10/01/2018
ms.openlocfilehash: b701ce9921d055dfe124c5a419f02900b15a9f62
ms.sourcegitcommit: a764e4b9d06b50d9b6173d0fbb7555e3babe6351
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/22/2018
ms.locfileid: "49641207"
---
# <a name="embed-with-report-web-part-in-sharepoint-online"></a>Incorporare con web part report in SharePoint Online

Con la nuova web part report di Power BI per SharePoint Online è possibile incorporare facilmente report interattivi di Power BI nelle pagine di SharePoint Online.

Quando si usa la nuova opzione **Incorpora in SharePoint Online**, i report incorporati sono completamente protetti in modo che sia possibile creare facilmente portali interni protetti.

## <a name="requirements"></a>Requisiti

Per il corretto funzionamento dell'opzione **Incorpora in SharePoint Online** relativa ai report esistono alcuni requisiti.

* È necessaria una licenza di Power BI Pro o una [capacità Power BI Premium (SKU EM o P)](service-premium.md#premium-capacity-nodes) con una licenza di Power BI.
* La web part Power BI per SharePoint Online richiede le [pagine moderne](https://support.office.com/article/Allow-or-prevent-creation-of-modern-site-pages-by-end-users-c41d9cc8-c5c0-46b4-8b87-ea66abc6e63b).

## <a name="embed-your-report"></a>Incorporare il report

Per incorporare il report in SharePoint Online, è prima di tutto necessario ottenere l'URL per il report e quindi usarlo con la nuova web part Power BI all'interno di SharePoint Online.

### <a name="get-a-url-to-your-report"></a>Ottenere un URL al report

1. Visualizzare il report all'interno del servizio Power BI.

2. Selezionare la voce di menu **File**.

3. Selezionare **Incorpora in SharePoint Online**.
   
    ![](media/service-embed-report-spo/powerbi-file-menu.png)

4. Copiare l'URL dalla finestra di dialogo.

    ![](media/service-embed-report-spo/powerbi-embed-link-sharepoint.png)

   > [!NOTE]
   > È anche possibile usare l'URL che viene visualizzato nella barra degli indirizzi del web browser quando si visualizza un report. L'URL contiene la pagina del report che si sta visualizzando. È necessario rimuovere la sezione del report dall'URL se si vuole usare una pagina diversa.

### <a name="add-the-power-bi-report-to-a-sharepoint-online-page"></a>Aggiungere il report di Power BI a una pagina di SharePoint Online

1. Aprire la pagina desiderata in SharePoint Online e selezionare **Modifica**.

    ![](media/service-embed-report-spo/powerbi-sharepoint-edit-page.png)

    In alternativa, creare una nuova pagina moderna selezionando **+ Nuovo** all'interno di SharePoint Online.

    ![](media/service-embed-report-spo/powerbi-sharepoint-new-page.png)

2. Selezionare **+** e selezionare la web part **Power BI**.

    ![](media/service-embed-report-spo/powerbi-sharepoint-new-web-part.png)

3. Selezionare **Aggiungi report**.

    ![](media/service-embed-report-spo/powerbi-sharepoint-new-report.png)

4. Incollare l'URL del report nel riquadro proprietà. Questo è l'URL copiato dai passaggi precedenti. Il report viene caricato automaticamente.

    ![](media/service-embed-report-spo/powerbi-sharepoint-new-web-part-properties.png)

5. Selezionare **Pubblica** per rendere visibile la modifica agli utenti di SharePoint Online.

    ![](media/service-embed-report-spo/powerbi-sharepoint-report-loaded.png)

## <a name="granting-access-to-reports"></a>Concessione dell'accesso ai report

Incorporare un report in SharePoint Online non autorizza automaticamente gli utenti a visualizzare il report. Le autorizzazioni per visualizzare il report vengono impostate all'interno del servizio Power BI.

> [!IMPORTANT]
> Assicurarsi di controllare chi può visualizzare il report all'interno del servizio Power BI e concedere l'accesso a chi non è elencato.

Esistono due modi per fornire l'accesso al report all'interno del servizio Power BI. Se si usa un gruppo di Office 365 per creare il sito del team di SharePoint Online è possibile aggiungere l'utente come membro dell'**area di lavoro per le app all'interno del servizio Power BI** e della **pagina SharePoint**. Questo garantisce che gli utenti possano visualizzare il contenuto di tale gruppo. Per altre informazioni, vedere [Creare e distribuire un'app in Power BI](service-create-distribute-apps.md).

In alternativa, è possibile concedere agli utenti l'accesso al report seguendo questi passaggi.

1. Aggiungere un riquadro dal report a un dashboard.

2. Condividere il dashboard con gli utenti che richiedono l'accesso al report. Per altre informazioni, vedere [Condividere un dashboard con i colleghi e altri utenti](service-share-dashboards.md).

## <a name="web-part-settings"></a>Impostazioni della web part

Di seguito è riportata una descrizione delle impostazioni che possono essere modificate per la web part Power BI per SharePoint Online.

![](media/service-embed-report-spo/powerbi-sharepoint-web-part-properties.png)

| Proprietà | Descrizione |
| --- | --- |
| Nome pagina |Imposta la pagina predefinita che viene visualizzata per la web part. Selezionare un valore nell'elenco a discesa. Se non viene visualizzata alcuna pagina, il report contiene una sola pagina o l'URL incollato contiene un nome di pagina. Rimuovere la sezione del report dall'URL per selezionare una pagina specifica. |
| Visualizza |Opzione per adattare il report all'interno della pagina di SharePoint Online. |
| Mostra il riquadro di spostamento |Mostra o nasconde il riquadro di spostamento. |
| Mostra riquadro Filtri |Mostra o nasconde il riquadro filtri. |

## <a name="multi-factor-authentication"></a>Multi-Factor Authentication

Se l'ambiente di Power BI richiede di eseguire l'accesso con l'autenticazione a più fattori, potrà essere richiesto di accedere con un dispositivo di sicurezza per verificare la propria identità. Ciò si verifica se non si è eseguito l'accesso a SharePoint Online usando Multi-Factor Authentication, ma l'ambiente di Power BI richiede un account convalidato da un dispositivo di sicurezza.

> [!NOTE]
> Multi-Factor Authentication non è ancora supportato con Azure Active Directory 2.0. Gli utenti ricevono un messaggio di *errore*. Se l'utente accede nuovamente a SharePoint Online con il dispositivo di sicurezza, potrebbe riuscire a visualizzare il report.

## <a name="reports-that-do-not-load"></a>Report che non vengono caricati

Il report potrebbe non essere caricato all'interno della web part Power BI e visualizzare il messaggio seguente.

*Questo contenuto non è disponibile.*

![](media/service-embed-report-spo/powerbi-sharepoint-report-not-found.png)

Esistono due motivi comuni per questo messaggio.

1. Non si è autorizzati ad accedere al report.
2. Il report è stato eliminato.

Contattare il proprietario della pagina SharePoint Online per risolvere il problema.

## <a name="known-issues-and-limitations"></a>Limitazioni e problemi noti

* Errore: "Si è verificato un errore. Provare a disconnettersi e riconnettersi, quindi visitare di nuovo questa pagina. ID di correlazione: non definito, Stato risposta HTTP: 400, Codice errore server 10001, messaggio: Token di aggiornamento mancante"
  
  Se si riceve questo errore, provare una delle soluzioni seguenti.
  
  1. Disconnettersi da SharePoint e accedere nuovamente. Assicurarsi di chiudere tutte le finestre del browser prima di accedere nuovamente.

  2. Se l'account utente richiede Multi-Factor Authentication, assicurarsi di accedere a SharePoint con il dispositivo Multi-Factor Authentication (app per telefono, smart card e così via).
  
  3. Gli account degli utenti Guest di Azure B2B non sono supportati. Per gli utenti viene visualizzato il logo Power BI che indica che è in corso il caricamento del componente ma non viene visualizzato il report.

* Power BI non supporta le stesse lingue localizzate supportate da SharePoint Online. Di conseguenza, la localizzazione all'interno del report incorporato potrebbe non essere corretta.

* Se si usa Internet Explorer 10, potrebbero verificarsi problemi. Per informazioni, vedere il [supporto dei browser per Power BI](consumer/end-user-browsers.md) e per [Office 365](https://products.office.com/office-system-requirements#Browsers-section).

* La web part Power BI non è disponibile nei [cloud sovrani](https://powerbi.microsoft.com/en-us/clouds/).

* SharePoint Server classico non è supportato con questa web part.

* I [filtri URL](service-url-filters.md) non sono supportati con la web part SPO.

## <a name="next-steps"></a>Passaggi successivi

[Consentire o impedire la creazione di pagine del sito moderne dagli utenti finali](https://support.office.com/article/Allow-or-prevent-creation-of-modern-site-pages-by-end-users-c41d9cc8-c5c0-46b4-8b87-ea66abc6e63b)  
[Creare e distribuire un'app in Power BI](service-create-distribute-apps.md)  
[Condividere un dashboard con i colleghi e altri utenti](service-share-dashboards.md)  
[Che cos'è Power BI Premium?](service-premium.md)  

Altre domande? [Provare a rivolgersi alla community di Power BI](http://community.powerbi.com/)