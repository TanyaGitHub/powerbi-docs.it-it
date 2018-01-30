---
title: Esportare un report dal servizio Power BI in Desktop (anteprima)
description: Scaricare un report dal servizio Power BI in un file di Power BI Desktop
services: powerbi
documentationcenter: 
author: mihart
manager: kfile
backup: 
editor: 
tags: 
qualityfocus: no
qualitydate: 
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 09/27/2017
ms.author: mihart
ms.openlocfilehash: 30975e9192633043aed7e4196820ef34044b8fcb
ms.sourcegitcommit: 99cc3b9cb615c2957dde6ca908a51238f129cebb
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/13/2017
---
# <a name="export-a-report-from-power-bi-service-to-desktop-preview"></a>Esportare un report dal servizio Power BI in Desktop (anteprima)
In Power BI Desktop è possibile esportare un report nel servizio Power BI (operazione talvolta definita *download*) salvando il report e selezionando **Pubblica**. È possibile esportare anche nell'altra direzione e scaricare un report dal servizio Power BI a Desktop. L'estensione per i file di esportazione, in entrambe le direzioni, è *pbix*.

Occorre tenere presenti alcune limitazioni e considerazioni, che verranno discusse più avanti in questo articolo.

![](media/service-export-to-pbix/power-bi-file-export.png)

## <a name="download-the-report-as-a-pbix"></a>Scaricare il report come file con estensione pbix
Per scaricare il file con estensione pbix, seguire questi passaggi:

1. Nel **servizio Power BI** aprire il report che si vuole scaricare in [Visualizzazione di modifica](service-reading-view-and-editing-view.md).
2. Nella barra dei menu selezionare **File > Scarica report**.
   
   > [!NOTE]
   > Per poterlo scaricare, il report deve essere stato [creato con Power BI Desktop](guided-learning/publishingandsharing.yml#step-2) dopo il 23 novembre 2016 (o aggiornato dopo tale data). In caso contrario, la voce di menu *Scarica report* nel servizio Power BI è inattiva.
   > 
   > 
3. Durante la creazione del file con estensione pbix, un messaggio di stato indica lo stato di avanzamento. Quando il file è pronto, verrà chiesto di aprire o salvare il file con estensione pbix. Il nome del file corrisponde al titolo del report.
   
    ![](media/service-export-to-pbix/power-bi-save-pbix.png)
   
    È ora possibile aprire il file con estensione pbix nel servizio Power BI (app.powerbi.com) o in Power BI Desktop.     
4. Per aprire immediatamente il report in Desktop, selezionare **Apri**.  Se non è stato ancora fatto, [installare Power BI Desktop](desktop-get-the-desktop.md).
   
    Quando si apre il report in Desktop, può essere visualizzato un messaggio di avviso che informa che alcune funzionalità disponibili nel report del servizio Power BI potrebbero non essere disponibili in Desktop.
   
    ![](media/service-export-to-pbix/power-bi-export-to-pbix_2.png)
5. Per aprire il report nel servizio Power BI, selezionare **Salva** e quindi usare **Recupera dati** per passare al percorso in cui è stato salvato il file con estensione pbix.
   
    ![](media/service-export-to-pbix/power-bi-get-data.png)

## <a name="considerations-and-troubleshooting"></a>Considerazioni e risoluzione dei problemi
Per il download (esportazione) di un file con estensione *pbix* dal servizio Power BI esistono alcune importanti considerazioni e limitazioni.

* Per scaricare il file, è necessario avere l'accesso in modifica al report
* Il report deve provenire da **Power BI Desktop** ed essere stato *pubblicato* nel **servizio Power BI** oppure il file con estensione pbix deve essere stato *caricato* nel servizio.
* I report devono essere stati pubblicati o aggiornati dopo il 23 novembre 2016. I report pubblicati prima di tale data non sono scaricabili.
* Questa funzionalità non funzionerà con i report creati in origine nel **servizio Power BI**, inclusi i pacchetti di contenuto.
* Per aprire i file scaricati è consigliabile usare sempre la versione più recente di **Power BI Desktop**. Potrebbe non essere possibile aprire i file *PBIX* scaricati nelle versioni non correnti di **Power BI Desktop**.
* Se l'amministratore ha disattivato la possibilità di esportare i dati, questa funzionalità non sarà visibile nel **servizio Power BI**.

## <a name="next-steps"></a>Passaggi successivi
Visualizzare il video di **Guy in a Cube** (durata: 1 minuto) che illustra questa funzionalità:

<iframe width="560" height="315" src="https://www.youtube.com/embed/ymWqU5jiUl0" frameborder="0" allowfullscreen></iframe>

Ecco alcuni articoli supplementari che possono essere d'aiuto per imparare a usare il **servizio Power BI**:

* [Report in Power BI](service-reports.md)
* [Power BI - Concetti di base](service-basic-concepts.md)

Dopo aver installato **Power BI Desktop**, il contenuto seguente consente di svolgere rapidamente le attività iniziali:

* [Introduzione a Power BI Desktop](desktop-getting-started.md)

Altre domande? [Provare la community di Power BI](http://community.powerbi.com/)   
