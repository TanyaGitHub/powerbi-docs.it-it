---
title: Gestione delle licenze di Power BI nell'organizzazione
description: 'Comprendere i vari tipi di licenza disponibili in Power BI: licenza gratuita, Power BI Pro e Power BI Premium.'
author: mgblythe
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-admin
ms.topic: conceptual
ms.date: 10/30/2018
ms.author: mblythe
LocalizationGroup: Administration
ms.openlocfilehash: bdd43c820f87bb9308478b4e2100514349644d11
ms.sourcegitcommit: 862faf948468d7f6d464b83f4e0b040d5213a580
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/30/2018
ms.locfileid: "50252377"
---
# <a name="power-bi-licensing-in-your-organization"></a>Gestione delle licenze di Power BI nell'organizzazione

Nel servizio Power BI gli utenti hanno determinate capacità in base a due tipi di licenze:

* **Per utente** - *licenze gratuite e licenze Power BI Pro*. Una licenza gratuita offre l'accesso ad alcune delle funzionalità del servizio Power BI. Una licenza Pro consente di accedere a tutto il contenuto e a tutte le funzionalità del servizio Power BI, inclusa la possibilità di condividere contenuto e collaborare con altri utenti Pro. Solo gli utenti della versione Pro possono pubblicare e usare contenuti nelle aree di lavoro delle app, condividere i dashboard e sottoscrivere dashboard e report. Per altre informazioni, vedere [Funzionalità del servizio Power BI in base al tipo di licenza](service-features-license-type.md).

* **Basata sulla capacità** - *licenze Power BI Premium*. Premium offre capacità dedicata per offrire prestazioni più coerenti e supportare volumi di dati più grandi in Power BI. Per i singoli utenti, Premium consente anche una distribuzione generalizzata del contenuto da parte degli utenti Pro senza richiedere licenze Pro per la visualizzazione del contenuto da parte dei destinatari. Per altre informazioni, vedere [What is Power BI Pro?](service-premium.md) (Che cos'è Power BI Pro?).

Questo articolo è incentrato sulle licenze per utente descritte dalla prospettiva dell'amministratore.

## <a name="manage-power-bi-pro-licenses"></a>Gestire le licenze Power BI Pro

L'amministratore può acquistare e assegnare le licenze Power BI Pro e iscriversi a una versione di valutazione di Power BI Pro per la propria organizzazione. Anche i singoli utenti possono iscriversi a una versione di valutazione di Power BI Pro.

### <a name="purchasing-power-bi-pro"></a>Acquisto di Power BI Pro

È possibile acquistare le licenze Power BI Pro tramite Microsoft Office 365 o rivolgendosi a un partner Microsoft certificato. Dopo aver acquistato le licenze, assegnarle ai singoli utenti. Per altre informazioni, vedere [Acquistare e assegnare licenze Power BI Pro](service-admin-purchasing-power-bi-pro.md).

### <a name="power-bi-pro-trial-for-individuals"></a>Versione di valutazione di Power BI Pro per utenti singoli

I singoli utenti dell'organizzazione possono iscriversi a una versione di valutazione di Power BI Pro. Per altre informazioni, vedere [Iscrizione a Power BI come utente singolo](service-self-service-signup-for-power-bi.md).

Gli utenti che usano questa versione di valutazione di Power BI Pro del prodotto non vengono visualizzati nel portale di amministrazione di Office 365 come utenti della versione di valutazione Power BI Pro (vengono visualizzati come utenti gratuiti di Power BI). Verranno tuttavia visualizzati come utenti della versione di valutazione di Power BI Pro nella pagina Gestisci archiviazione di Power BI.

### <a name="power-bi-pro-trial-for-organizations"></a>Versione di valutazione di Power BI Pro per le organizzazioni

Se si vogliono acquisire e distribuire le licenze della versione di valutazione di Power BI a più utenti dell'organizzazione senza che i singoli utenti accettino individualmente le condizioni della versione di valutazione, iscriversi a una versione di valutazione di Power BI Pro per l'organizzazione.

Prima di seguire i passaggi per l'iscrizione, tenere presente quanto segue:

* Per iscriversi, è necessario essere membro del ruolo [**Amministratore globale** o **Amministratore fatturazione**](https://support.office.com/article/about-office-365-admin-roles-da585eea-f576-4f55-a1e0-87090b6aaa9d?ui=en-US&rs=en-US&ad=US) in Office 365.

* È previsto un limite di una versione di valutazione aziendale per ogni tenant. Ciò significa che se un utente ha già applicato Power BI Pro - Versione di valutazione al tenant, non è possibile ripetere l'operazione. Se è necessaria assistenza a tal riguardo, contattare il [supporto per la fatturazione di Office 365](https://support.office.microsoft.com/en-us/article/contact-support-for-business-products-admin-help-32a17ca7-6fa0-4870-8a8d-e25ba4ccfd4b?CorrelationId=552bbf37-214f-4202-80cb-b94240dcd671&ui=en-US&rs=en-US&ad=US).

1. Accedere all'[interfaccia di amministrazione di Office 365](https://portal.office.com/adminportal/home#/homepage).

1. Nel riquadro di spostamento a sinistra, selezionare **Fatturazione** e quindi **Sottoscrizioni**.

   ![Fatturazione e sottoscrizioni](media/service-admin-licensing-organization/service-power-bi-pro-in-your-organization-05.png)

1. Selezionare **Aggiungi abbonamento** a destra.

   ![Aggiungi abbonamenti](media/service-admin-licensing-organization/service-power-bi-pro-in-your-organization-06.png)

1. In **Altri piani** passare il cursore sui puntini di sospensione (**...**) per Power BI Pro e selezionare **Avvia versione di valutazione gratuita**.

   ![Avvia versione di valutazione gratuita](media/service-admin-licensing-organization/service-power-bi-pro-in-your-organization-07.png) 

1. Nella schermata di conferma dell'ordine selezionare **Prova adesso**.

1. Selezionare **Continua** alla ricezione dell'ordine.

È ora possibile [assegnare licenze in Office 365](https://support.office.com/article/assign-licenses-to-users-in-office-365-for-business-997596b5-4173-4627-b915-36abac6786dc).

## <a name="manage-power-bi-free-licenses"></a>Gestire le licenze gratuite di Power BI

Gli utenti all'interno dell'organizzazione possono accedere alle licenze gratuite di Power BI in due modi diversi. Possono iscriversi a Power BI come utenti singoli oppure l'amministratore può assegnare loro una licenza di Power BI dall'interfaccia di amministrazione di Office 365.

Consentire l'iscrizione come utenti singoli riduce il carico di lavoro per gli amministratori dell'organizzazione, dal momento che in questo modo gli utenti interessati a Power BI possono iscriversi gratuitamente.

La disabilitazione della singola iscrizione utente consente tuttavia un maggiore controllo ed è un'opzione utilissima se si vuole controllare l'uso del servizio.

### <a name="power-bi-free-for-individuals"></a>Power BI gratuito per utenti singoli

Per impostazione predefinita, i singoli utenti dell'organizzazione possono richiedere una licenza gratuita di Power BI. Per altre informazioni, vedere [Iscrizione a Power BI come utente singolo](service-self-service-signup-for-power-bi.md).

Per bloccare le iscrizioni di singoli utenti, vedere [Abilitare o disabilitare l'iscrizione di utenti singoli in Azure Active Directory](service-admin-licensing-organization.md#enable-or-disable-individual-user-sign-up-in-azure-active-directory) più avanti in questo articolo.

### <a name="requesting-and-assigning-free-licenses"></a>Richiesta e assegnazione di licenze gratuite

Se si prevede di gestire centralmente le richieste e le assegnazioni delle licenze, verificare prima di avere il blocco delle licenze Power BI (gratuito) illimitato.

Il blocco delle licenze è disponibile la prima volta in cui qualcuno tenta di iscriversi a Power BI come utente singolo. Durante questo processo, il blocco delle licenze viene associato all'organizzazione e viene assegnata una licenza all'utente che sta eseguendo l'iscrizione.

1. Nell'interfaccia di amministrazione di Office 365, in **Fatturazione** > **Licenze**, verificare che sia presente **Illimitato**.

    ![Blocco delle licenze gratuito senza limiti](media/service-admin-licensing-organization/unlimited-licenses.png)

1. Se il blocco è disponibile, è ora possibile [assegnare le licenze in Office 365](https://support.office.com/article/assign-licenses-to-users-in-office-365-for-business-997596b5-4173-4627-b915-36abac6786dc). Se il blocco non è disponibile, sono disponibili due opzioni:

    * Fare in modo che un membro dell'organizzazione si iscriva singolarmente, attivando così la creazione del blocco illimitato.

    * Passare alla procedura successiva, in cui è possibile iscriversi per un numero fisso di licenze.

Se il blocco delle licenze di Power BI (gratuito) illimitato non è disponibile e non si vuole che un singolo utente esegua l'iscrizione, seguire la procedura descritta di seguito.

1. Accedere all'[interfaccia di amministrazione di Office 365](https://portal.office.com/admin/default.aspx).

1. Nel riquadro di spostamento a sinistra selezionare **Fatturazione** > **Abbonamenti**.

1. Selezionare **Aggiungi abbonamenti** a destra.

1. In **Altri piani** passare il puntatore del mouse sui puntini di sospensione (**...**) per Power BI (gratuito) e selezionare **Acquista ora**.

    ![Acquista ora - Power BI (gratuito)](media/service-admin-licensing-organization/buy-powerbi-free.png)

1. Immettere il numero di licenze da aggiungere e selezionare **Procedi al pagamento** oppure **Aggiungi al carrello**.

1. Immettere le informazioni necessarie nel flusso di pagamento.

    Non si esegue alcun acquisto quando si utilizza questo approccio, anche se è necessario immettere i dati della carta di credito per la fatturazione o scegliere di ricevere una fattura.

1. È ora possibile [assegnare licenze in Office 365](https://support.office.com/article/assign-licenses-to-users-in-office-365-for-business-997596b5-4173-4627-b915-36abac6786dc).

1. Se in seguito si decide di aggiungere altre licenze, è possibile tornare ad **Aggiungi abbonamenti** e selezionare **Cambia la quantità di licenze** per Power BI (gratuito).

    ![Cambia la quantità di licenze](media/service-admin-licensing-organization/change-license-quantity.png)

### <a name="enable-or-disable-individual-user-sign-up-in-azure-active-directory"></a>Abilitare o disabilitare l'iscrizione di utenti singoli in Azure Active Directory

L'amministratore può abilitare o disabilitare le iscrizioni come utente singolo in Azure Active Directory (AAD). Questa sezione dell'articolo illustra come gestire le iscrizioni con i comandi di PowerShell. Per altre informazioni su Azure PowerShell, vedere [Panoramica di Azure PowerShell](/powershell/azure/overview).

L'impostazione di AAD che controlla l'iscrizione è **AllowAdHocSubscriptions**. Nella maggior parte dei tenant questa opzione è impostata su *true*, il che significa che è abilitata. Se Power BI è stato acquistato tramite un partner, è possibile che questa opzione sia impostata su *false*, il che significa che è disabilitata. Se si modifica l'impostazione da *true* a *false*, ai nuovi utenti dell'organizzazione viene impedito di eseguire l'iscrizione singolarmente. Gli utenti iscritti a Power BI prima della modifica dell'impostazione mantengono le proprie licenze.

1. Accedere ad Azure Active Directory usando le credenziali di Office 365. La prima riga dello script PowerShell seguente richiede le credenziali. La seconda riga si connette ad Azure Active Directory.

    ```powershell
     $msolcred = get-credential
     connect-msolservice -credential $msolcred
    ```

   ![Accesso ad Azure Active Directory](media/service-admin-licensing-organization/aad-signin.png)

1. Dopo aver eseguito l'accesso, eseguire il comando seguente per vedere come è configurato il tenant.

    ```powershell
     Get-MsolCompanyInformation | fl AllowAdHocSubscriptions
    ```
1. Eseguire il comando seguente per abilitare ($true) o disabilitare ($false) **AllowAdHocSubscriptions**.

    ```powershell
     Set-MsolCompanySettings -AllowAdHocSubscriptions $true
    ```

## <a name="next-steps"></a>Passaggi successivi

[Iscrizione a Power BI in modalità self-service](service-self-service-signup-for-power-bi.md)  

[Acquistare e assegnare licenze Power BI Pro](service-admin-purchasing-power-bi-pro.md)

Altre domande? [Provare a rivolgersi alla community di Power BI](http://community.powerbi.com/)