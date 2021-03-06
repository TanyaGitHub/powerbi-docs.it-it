---
title: 'Pacchetti di contenuto aziendali: Gestire e aggiornare'
description: Scoprire di più sulla gestione, sull'aggiornamento e sull'eliminazione dei pacchetti di contenuto aziendali in Power BI.
author: maggiesMSFT
manager: kfile
ms.reviewer: lukaszp
ms.service: powerbi
ms.component: powerbi-service
ms.topic: conceptual
ms.date: 08/02/2018
ms.author: maggies
LocalizationGroup: Share your work
ms.openlocfilehash: d00ad254e25f8806f6cf2bc944e849e32167b1f8
ms.sourcegitcommit: 52ac456bf2ac025b22ea634c28482f22e1cc19ac
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/10/2018
ms.locfileid: "48908395"
---
# <a name="manage-update-and-delete-organizational-content-packs"></a>Gestire, aggiornare ed eliminare pacchetti di contenuto aziendali
> [!NOTE]
> Non è possibile creare pacchetti di contenuto aziendali né installarli nell'anteprima delle nuove esperienze delle aree di lavoro. Questo è un buon momento per aggiornare i pacchetti di contenuto per le app, se non è ancora stato fatto. [Altre informazioni sulla nuova esperienza dell'area di lavoro](service-create-the-new-workspaces.md).
> 

È possibile creare pacchetti di dashboard, report, cartelle di lavoro di Excel e set di dati e condividerli con i colleghi come [pacchetti di contenuto aziendali](service-organizational-content-pack-introduction.md). I colleghi utilizzarli così come sono o possono creare le proprie copie.

La creazione di pacchetti di contenuto è diversa dalla condivisione di dashboard o dalla collaborazione negli stessi in un gruppo. Per scegliere la soluzione migliore in base alla situazione specifica, leggere [Come si condividono i dashboard e i report e in che modo ci si collabora?](service-how-to-collaborate-distribute-dashboards-reports.md).

L'autore del pacchetto di contenuto può eseguire solo alcune attività organizzative relative al pacchetto di contenuto:

* Ripubblicare.
* Limitare o estendere l'accesso al pacchetto di contenuto.
* Impostare e modificare l'aggiornamento pianificato.
* Eliminare il pacchetto di contenuto.

## <a name="modify-and-re-publish-an-organizational-content-pack"></a>Modificare e ripubblicare un pacchetto di contenuto aziendale
Se si modifica il dashboard, il report o la cartella di lavoro di Excel del pacchetto di contenuto originale, Power BI chiederà di ripubblicarlo. Inoltre, l'autore del pacchetto di contenuto può aggiornare tutte le opzioni selezionate nella finestra Crea pacchetto di contenuto durante la creazione del pacchetto originale. 

## <a name="republish-with-new-content"></a>Ripubblicare con nuovo contenuto
Quando si apporta e si salva una modifica al dashboard incluso in un pacchetto di contenuto, Power BI ricorda di eseguirne l'aggiornamento per fare in modo che altri utenti possano vedere le modifiche. Ad esempio, se si aggiunge un nuovo riquadro o si modifica semplicemente il nome del dashboard.

1. Selezionare **Visualizza pacchetti di contenuto** nel messaggio.
   
   ![](media/service-organizational-content-pack-manage-update-delete/pbi_contpkchangesmessage.png)
2. Oppure selezionare l'icona dell'ingranaggio nell'angolo superiore destro ![](media/service-organizational-content-pack-manage-update-delete/cog.png) e selezionare **Visualizza pacchetto di contenuto**.
   
   ![](media/service-organizational-content-pack-manage-update-delete/pbi_contpkview.png)
   
   Si noti l'icona di avviso ![](media/service-organizational-content-pack-manage-update-delete/pbi_contpkwarningicon.png).  Indica che il pacchetto di contenuto è stato modificato e non corrisponde più a quello pubblicato.
3. Selezionare **Modifica**.  
4. Apportare le modifiche necessarie nella finestra **Aggiorna pacchetto di contenuto** e selezionare **Aggiorna**. Viene visualizzato un messaggio di **operazione completata**.
   
   * Per i membri del gruppo che non hanno personalizzato il pacchetto di contenuto, l'aggiornamento viene applicato automaticamente.
   * I membri del gruppo che hanno personalizzato il pacchetto di contenuto ricevono una notifica dell'esistenza di una nuova versione.  Potranno quindi passare ad AppSource e scaricare il pacchetto aggiornato senza perdere la propria versione personalizzata.  A questo punto hanno 2 versioni: quella personalizzata e il pacchetto di contenuto aggiornato.  Nella versione personalizzata non saranno più presenti tutti i riquadri dal pacchetto di contenuto originale.  Verrà comunque eseguito il rendering dei riquadri aggiunti da altri report. Tuttavia, se il proprietario del pacchetto di contenuto elimina il set di dati su cui si basa il pacchetto di contenuto, l'intero report va perduto.  

## <a name="update-the-audience-expand-or-restrict-access"></a>Aggiornare i destinatari: estendere o limitare l'accesso
Un'altra modifica che possono eseguire gli autori di pacchetti di contenuti è l'estensione o la limitazione dell'accesso ai pacchetti.  Può accadere, ad esempio, di pubblicare un pacchetto di contenuto per un ampio numero di destinatari e che in seguito sia stato deciso di limitarne l'accesso a un gruppo meno numeroso.  

1. Selezionare l'icona dell'ingranaggio ![](media/service-organizational-content-pack-manage-update-delete/cog.png) e scegliere **Visualizza pacchetti di contenuto**.
2. Selezionare **Modifica**. 
3. Apportare le modifiche necessarie nella finestra **Aggiorna pacchetto di contenuto** e selezionare **Aggiorna**. Ad esempio, eliminare il gruppo di distribuzione originale nel campo **Gruppi specifici** e sostituirlo con un altro gruppo di distribuzione (che include meno membri).
   
   Viene visualizzato un messaggio di operazione completata.
   
   Per un collaboratore che non fa parte del nuovo alias:
   
   * Per i membri del gruppo che non hanno personalizzato il pacchetto di contenuto, il dashboard e i report associati al pacchetto non sono più disponibili e il pacchetto di contenuto non viene visualizzato nel riquadro di spostamento.
   * Per i membri del gruppo che hanno personalizzato il pacchetto di contenuto, alla successiva apertura del dashboard personalizzato non saranno più presenti tutti i riquadri dal pacchetto di contenuto originale.  Verrà comunque eseguito il rendering dei riquadri aggiunti da altri report. I report e il set di dati del pacchetto di contenuto originale non sono più disponibili e il pacchetto di contenuto non viene visualizzato nel riquadro di spostamento.   

## <a name="refresh-an-organizational-content-pack"></a>Aggiornare un pacchetto di contenuto aziendale
L'autore del pacchetto di contenuto può [pianificare l'aggiornamento dei set di dati](refresh-data.md).  Quando si crea e si carica il pacchetto di contenuto, la pianificazione dell'aggiornamento viene caricata insieme ai set di dati. Se viene modificata, è necessario ripubblicare il pacchetto di contenuto (vedere sopra).

## <a name="delete-an-organizational-content-pack-from-appsource"></a>Eliminare un pacchetto di contenuto aziendale da AppSource
Solo l'autore di un pacchetto di contenuto può eliminarlo da AppSource. Se è stato creato un pacchetto di contenuto aziendale in un'area di lavoro per le app e si decide di eliminare l'area di lavoro, assicurarsi di eliminare prima il pacchetto di contenuto. Se si elimina l'area di lavoro senza eliminare prima il pacchetto di contenuto, non è più possibile accedere ai pacchetti di contenuto ed è necessario contattare il supporto tecnico Microsoft per assistenza. 

> [!TIP]
> È possibile [eliminare la connessione a un pacchetto di contenuto](service-organizational-content-pack-disconnect.md) di cui non si è l'autore. Il pacchetto di contenuto non verrà eliminato da AppSource.
> 
> 

1. Per eliminare un pacchetto di contenuto da AppSource, passare all'area di lavoro dell'app in cui è stato creato il pacchetto di contenuto, selezionare l'icona a forma di ingranaggio ![](media/service-organizational-content-pack-manage-update-delete/cog.png) e scegliere **Visualizza pacchetti di contenuto**.
2. Selezionare **Elimina \> Elimina**. 
   
   * Per i membri del gruppo che non hanno personalizzato il pacchetto di contenuto, il dashboard e i report associati a tale pacchetto di contenuto vengono automaticamente rimossi. Non sono più disponibili e il pacchetto di contenuto non viene visualizzato nel riquadro di spostamento.
   * Per i membri del gruppo che hanno personalizzato il pacchetto di contenuto, alla successiva apertura del dashboard personalizzato non saranno più presenti tutti i riquadri dal pacchetto di contenuto originale.  Verrà comunque eseguito il rendering dei riquadri aggiunti da altri report. I report e il set di dati del pacchetto di contenuto originale non sono più disponibili e il pacchetto di contenuto non viene visualizzato nel riquadro di spostamento.   

## <a name="next-steps"></a>Passaggi successivi
* [Introduzione ai pacchetti di contenuto aziendali](service-organizational-content-pack-introduction.md)
* [Creare e distribuire un'app in Power BI](service-create-distribute-apps.md) 
* Altre domande? [Provare la community di Power BI](http://community.powerbi.com/)

