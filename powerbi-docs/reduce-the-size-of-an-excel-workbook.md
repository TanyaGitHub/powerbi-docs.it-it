---
title: Ridurre le dimensioni di una cartella di lavoro di Excel per visualizzarla in Power BI
description: Ridurre le dimensioni di una cartella di lavoro di Excel per visualizzarla in Power BI
author: davidiseminger
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-service
ms.topic: conceptual
ms.date: 07/27/2018
ms.author: davidi
LocalizationGroup: Data from files
ms.openlocfilehash: 12ff54b1aa44edaead98b1fab6942acbd76216c7
ms.sourcegitcommit: fbb7924603f8915d07b5e6fc8f4d0c7f70c1a1e1
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/02/2018
ms.locfileid: "39329432"
---
# <a name="reduce-the-size-of-an-excel-workbook-to-view-it-in-power-bi"></a>Ridurre le dimensioni di una cartella di lavoro di Excel per visualizzarla in Power BI
È possibile caricare in Power BI qualsiasi cartella di lavoro di Excel inferiore a 1 GB. Una cartella di lavoro di Excel può essere composta da due parti: un modello di dati e il resto del report, cioè il contenuto di base del foglio di lavoro. Se il report rispetta i limiti di dimensioni seguenti, lo si può salvare in **OneDrive for Business**, ci si può connettere da Power BI e lo si può visualizzare in Excel Online:

* La cartella di lavoro complessiva può raggiungere le dimensioni massime di 1 GB.
* Il contenuto di base del foglio di lavoro può avere dimensioni massime di 10 MB.

## <a name="what-makes-core-worksheet-contents-larger-than-10-mb"></a>Cosa rende il contenuto di base del foglio di lavoro più grande di 10 MB
Ecco alcuni elementi che possono far aumentare il contenuto di base del foglio di lavoro oltre 10 MB:

* Immagini.
* Celle ombreggiate. [Rimuovere un formato di ombreggiatura delle celle](https://support.office.com/article/Add-or-change-the-background-color-of-cells-ac10f131-b847-428f-b656-d65375fb815e).
* Fogli di lavoro colorati. [Rimuovere uno sfondo di un foglio](https://support.office.com/en-US/article/add-or-remove-a-sheet-background-3577a762-8450-4556-96a2-cc265abc00a8).
* Caselle di testo.
* ClipArt.

Provare, se possibile, a rimuovere questi elementi. 

Se il report include un modello di dati, sono disponibili altre opzioni: 

* Rimuovere i dati dai fogli di lavoro e archiviarli nel modello di dati. Per i dettagli, vedere "Rimuovere i dati dai fogli di lavoro" più avanti. 
* [Creare un modello di dati con un utilizzo efficiente della memoria](https://support.office.com/article/Create-a-memory-efficient-Data-Model-using-Excel-2013-and-the-Power-Pivot-add-in-951c73a9-21c4-46ab-9f5e-14a2833b6a70) per ridurre le dimensioni complessive del report.

Per effettuare una di queste modifiche, è necessario modificare la cartella di lavoro in Excel.

Altre informazioni sui [limiti di dimensioni dei file per le cartelle di lavoro di Excel in SharePoint Online](https://support.office.com/article/File-size-limits-for-workbooks-in-SharePoint-Online-9e5bc6f8-018f-415a-b890-5452687b325e).

## <a name="remove-data-from-worksheets"></a>Rimuovere i dati dai fogli di lavoro
Se si importano i dati in Excel dalla scheda Power Query o dalla scheda Dati di Excel, la cartella di lavoro potrebbe contenere gli stessi dati in una tabella di Excel e nel modello di dati. Le tabelle di Excel di grandi dimensioni possono rendere il contenuto di base del foglio di lavoro più grande di 10 MB. Se si rimuove la tabella in Excel mantenendo i dati nel modello di dati, è possibile ridurre di molto il contenuto di base del foglio di lavoro del report. 

Quando si importano i dati in Excel, seguire questi suggerimenti:

* **In Power Query**: deselezionare la casella **Carica in foglio di lavoro** .
  
  I dati vengono importati solo nel modello di dati, senza dati nei fogli di lavoro di Excel.
* **Nella scheda Dati di Excel**, se in precedenza è stato selezionato **Tabella** nell'Importazione guidata: passare a **Connessioni esistenti** \> fare clic sulla connessione \>**Crea solo connessione**. Eliminare la tabella o le tabelle originali create durante l'importazione iniziale.
* **Nella scheda Dati di Excel**: non selezionare **Tabella** nella casella **Importa dati** .

## <a name="workbook-size-optimizer"></a>Strumento di ottimizzazione delle dimensioni della cartella di lavoro
Se la cartella di lavoro contiene un modello di dati, è possibile eseguire lo strumento di ottimizzazione delle dimensioni della cartella di lavoro per ridurre le dimensioni della cartella di lavoro. [Scaricare lo strumento di ottimizzazione delle dimensioni della cartella di lavoro](https://www.microsoft.com/en-us/download/details.aspx?id=38793).

## <a name="related-info"></a>Informazioni correlate
[Creare un modello di dati con un utilizzo efficiente della memoria mediante Excel 2013 e il componente aggiuntivo PowerPivot](https://support.office.com/article/Create-a-memory-efficient-Data-Model-using-Excel-2013-and-the-Power-Pivot-add-in-951c73a9-21c4-46ab-9f5e-14a2833b6a70)

[Usare collegamenti OneDrive for Business in Power BI Desktop](desktop-use-onedrive-business-links.md)

