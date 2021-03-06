---
title: Connettersi ai file in OneDrive per un'area di lavoro di un'app Power BI
description: Informazioni su come archiviare e connettersi a file di Excel, CSV e di Power BI Desktop archiviati nell'area di lavoro per le app in OneDrive.
author: maggiesMSFT
manager: kfile
ms.reviewer: lukasz
ms.service: powerbi
ms.component: powerbi-service
ms.topic: conceptual
ms.date: 08/02/2018
ms.author: maggies
LocalizationGroup: Share your work
ms.openlocfilehash: c732d1128719db500e13194d36ba1db2605efd2c
ms.sourcegitcommit: 52ac456bf2ac025b22ea634c28482f22e1cc19ac
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/10/2018
ms.locfileid: "48908698"
---
# <a name="connect-to-files-stored-in-onedrive-for-your-power-bi-app-workspace"></a>Connettersi ai file archiviati in OneDrive per un'area di lavoro di un'app Power BI
Dopo aver [creato un'area di lavoro per le app in Power BI](service-create-distribute-apps.md), è possibile archiviare i file di Excel, CSV e di Power BI Desktop nell'area di lavoro per le app Power BI in OneDrive for Business. Continuando ad aggiornare i file archiviati in OneDrive, gli aggiornamenti eseguiti verranno applicati automaticamente ai report e ai dashboard di Power BI basati sui file. 

> [!NOTE]
> L'anteprima della nuova esperienza dell'area di lavoro modificherà la relazione tra le aree di lavoro di Power BI e i gruppi di Office 365. Non verrà creato automaticamente un gruppo di Office 365 ogni volta che si crea una delle nuove aree di lavoro. Informazioni sulla [creazione di nuove aree di lavoro (anteprima)](service-create-the-new-workspaces.md)

L'aggiunta di file all'area di lavoro per le app è un processo in due passaggi: 

1. Prima di tutto è necessario [caricare i file nel OneDrive for Business](service-connect-to-files-in-app-workspace-onedrive-for-business.md#1-upload-files-to-the-onedrive-for-business-for-your-app-workspace) relativo alla propria area di lavoro per le app
2. e quindi [connettersi a tali file da Power BI](service-connect-to-files-in-app-workspace-onedrive-for-business.md#2-import-excel-files-as-datasets-or-as-excel-online-workbooks).

> [!NOTE]
> Le aree di lavoro per le app sono disponibili solo con [Power BI Pro](service-features-license-type.md).
> 
> 

## <a name="1-upload-files-to-the-onedrive-for-business-for-your-app-workspace"></a>1. Caricare file nell'area di lavoro per le app in OneDrive for Business
1. Nel servizio Power BI fare clic sulla freccia accanto ad Aree di lavoro > selezionare i puntini di sospensione (**…**) accanto al nome dell'area di lavoro per le app. 
   
   ![](media/service-connect-to-files-in-app-workspace-onedrive-for-business/power-bi-app-ellipsis.png)
2. Selezionare **File** per aprire il OneDrive for Business relativo alla propria area di lavoro per le app in Office 365.
   
   > [!NOTE]
   > Se nel menu dell'area di lavoro per le app non è presente alcuna voce **File**, selezionare **Membri**  per aprire l'area di lavoro per le app in OneDrive for Business. Selezionare quindi **File**. Office 365 configura un percorso di archiviazione OneDrive per i file dell'area di lavoro del gruppo dell'app. Questo processo potrebbe richiedere alcuni minuti. 
   > 
   > 
3. In questo percorso è possibile caricare i file nell'area di lavoro per le app in OneDrive for Business. Selezionare **Carica**e passare ai file.
   
   ![](media/service-connect-to-files-in-app-workspace-onedrive-for-business/pbi_grpfilesonedrive.png)

## <a name="2-import-excel-files-as-datasets-or-as-excel-online-workbooks"></a>2. Importare i file di Excel come set di dati o come cartelle di lavoro di Excel Online
A questo punto, dopo aver aggiunto i file nell'area di lavoro per le app in OneDrive for Business, è possibile: 

* [Importare i dati dalla cartella di lavoro di Excel come un set di dati](service-get-data-from-files.md) e usarli per creare report e dashboard visualizzabili in un Web browser e su dispositivi mobili.
* In alternativa, [connettersi a un'intera cartella di lavoro di Excel in Power BI](service-excel-workbook-files.md) e visualizzarla esattamente come appare in Excel Online.

### <a name="import-or-connect-to-the-files-in-your-app-workspace"></a>Importare o connettersi ai file nell'area di lavoro per le app
1. In Power BI passare all'area di lavoro per le app, in modo da visualizzare il nome dell'area di lavoro nell'angolo in alto a sinistra. 
2. Selezionare **Recupera dati** nella parte inferiore del riquadro di spostamento sinistro. 
   
   ![](media/service-connect-to-files-in-app-workspace-onedrive-for-business/power-bi-app-get-data-button.png)
3. Nella casella **File** selezionare **Recupera**.
   
   ![](media/service-connect-to-files-in-app-workspace-onedrive-for-business/pbi_getfiles.png)
4. Selezionare **OneDrive** - *nome dell'area di lavoro per le app*.
   
    ![](media/service-connect-to-files-in-app-workspace-onedrive-for-business/pbi_grp_one_drive_shrpt.png)
5. Selezionare il file desiderato > **Connetti**.
   
    A questo punto, è necessario scegliere se [importare i dati dalla cartella di lavoro di Excel](service-get-data-from-files.md) o [connettersi a intere cartelle di lavoro di Excel](service-excel-workbook-files.md).
6. Selezionare **Importa** o **Connetti**.
   
    ![](media/service-connect-to-files-in-app-workspace-onedrive-for-business/pbi_importexceldataorwholecrop.png)
7. Se si seleziona **Importa**, la cartella di lavoro sarà visualizzata nella scheda **Set di dati**. 
   
    ![](media/service-connect-to-files-in-app-workspace-onedrive-for-business/power-bi-app-excel-file-import.png)
   
    Se si seleziona **Connetti**, la cartella di lavoro sarà visualizzata nella scheda **Cartelle di lavoro**.
   
    ![](media/service-connect-to-files-in-app-workspace-onedrive-for-business/power-bi-app-excel-file-connect.png)

## <a name="next-steps"></a>Passaggi successivi
* [Creare app e aree di lavoro per le app in Power BI](service-create-distribute-apps.md)
* [Importare i dati da cartelle di lavoro di Excel](service-get-data-from-files.md)
* [Connettersi a cartelle di lavoro di Excel complete](service-excel-workbook-files.md)
* Altre domande? [Provare la community di Power BI](http://community.powerbi.com/)
* Per inviare commenti e suggerimenti, visitare il forum [Power BI Ideas](https://ideas.powerbi.com/forums/265200-power-bi)

