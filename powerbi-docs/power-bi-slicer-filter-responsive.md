---
title: Creare un filtro dei dati reattivo e ridimensionabile in Power BI
description: Informazioni su come creare un filtro dei dati reattivo ridimensionabile per adattarsi al report
services: powerbi
documentationcenter: 
author: maggiesMSFT
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
ms.date: 12/08/2017
ms.author: maggies
ms.openlocfilehash: f95f126cc6a7c95fbe3227b712281a7d3f81e320
ms.sourcegitcommit: b780b7108fd9b52398b8377b52836f0e0fedc96e
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/09/2017
---
# <a name="create-a-responsive-slicer-you-can-resize-in-power-bi-preview"></a>Creare un filtro dei dati reattivo e ridimensionabile in Power BI (anteprima)

I filtri dei dati reattivi possono essere ridimensionati per adattarsi a qualunque spazio nel report. Ridimensionando i filtri dei dati reattivi in base a dimensioni e forme diverse, ad esempio orizzontale, quadrata o verticale, i valori del filtro dei dati verranno automaticamente ridisposti. In Power BI Desktop e nel servizio Power BI, è possibile rendere reattivi i filtri dei dati orizzontali e i filtri dei dati data/intervallo. I filtri dei dati data/intervallo offrono anche aree di tocco migliorate per modificarli più facilmente con la punta del dito. È possibile creare filtri dei dati reattivi di piccole o grandi dimensioni. Verranno ridimensionati automaticamente per adattarsi ai report nel servizio Power BI e alle app Power BI per dispositivi mobili. 

![È disponibile un'ampia gamma di forme per i filtri dei dati reattivi](media/power-bi-slicer-filter-responsive/responsive-slicer-gif.gif)

## <a name="create-a-slicer"></a>Creare un filtro dei dati

Il primo passaggio per creare un filtro dei dati dinamico prevede la creazione di un filtro dei dati di base. 

1. Selezionare l'icona del **filtro dei dati** ![icona Filtro dei dati](media/power-bi-slicer-filter-responsive/power-bi-slicer-icon.png) nel riquadro **Visualizzazioni**.
2. Trascinare il campo da filtrare su **Campo**.

    ![Aggiungere un campo al filtro dei dati](media/power-bi-slicer-filter-responsive/power-bi-slicer-field.png)

## <a name="convert-to-a-horizontal-slicer"></a>Convertire un filtro dei dati in filtro dei dati orizzontale

1. Con il filtro dei dati selezionato, nel riquadro **Visualizzazioni** selezionare la scheda **Formato**.
2. Espandere la sezione **Generale**, quindi in **Orientamento** selezionare **Orizzontale**.

    ![Impostare il filtro dei dati su orizzontale](media/power-bi-slicer-filter-responsive/power-bi-slicer-horizontal.png) 

1.  Sarà probabilmente necessario allargarlo per visualizzare un maggior numero di valori.

     ![Allargare il filtro dei dati](media/power-bi-slicer-filter-responsive/power-bi-slicer-wide-horizontal.png)

## <a name="make-it-responsive-and-experiment-with-it"></a>Renderlo reattivo e provare a usarlo

Questo passaggio è facile. 

1. In **Orientamento**, nella sezione **Generale** della scheda **Formato**, impostare **Reattivo (anteprima)** su **Sì**.  

    ![A questo punto, il filtro dei dati è reattivo](media/power-bi-slicer-filter-responsive/power-bi-slicer-wide-responsive.png)

1. ed è possibile provarlo. Trascinare gli angoli per abbassarlo, allungarlo, allargarlo o restringerlo. Se lo si imposta molto piccolo, diventa un'icona di filtro.

    ![Filtro dei dati così piccolo da diventare un'icona di filtro](media/power-bi-slicer-filter-responsive/power-bi-slicer-small-filter-icon.png)

## <a name="add-it-to-a-phone-report-layout"></a>Aggiungerlo al layout del report per il telefono

In Power BI Desktop è possibile creare un layout telefono per ogni pagina di un report. Se una pagina ha un layout telefono, in un telefono cellulare verrà visualizzata con l'orientamento verticale. In caso contrario, sarà necessario visualizzarla con l'orientamento orizzontale. 

1. Nel menu **Visualizza** selezionare **Layout telefono**.

     ![Icona Layout telefono, menu Visualizza](media/power-bi-slicer-filter-responsive/power-bi-phone-layout-menu.png)
    
1. Trascinare tutti gli oggetti visivi desiderati nel report per il telefono sulla griglia. Quando si trascina il filtro dei dati reattivo, impostare le dimensioni desiderate. In questo caso, semplicemente un'icona di filtro.

    ![Aggiungere il filtro dei dati al layout del report per il telefono](media/power-bi-slicer-filter-responsive/power-bi-slicer-phone-layout.png)

Altre informazioni su come creare [report ottimizzati per l'app Power BI per dispositivi mobili](desktop-create-phone-report.md).

## <a name="make-a-time-or-range-slicer-responsive"></a>Impostare un filtro dei dati temporale o di intervallo su reattivo

Per impostare un riquadro o un filtro dei dati di intervallo su reattivo, è possibile seguire la stessa procedura. Dopo aver impostato l'opzione **Reattivo** su **Sì**, osservare quanto segue:

- Gli oggetti visivi ottimizzano l'ordine delle caselle di input a seconda delle dimensioni consentite nell'area di disegno. 
- La visualizzazione dell'elemento dati è ottimizzata per aumentare al massimo l'usabilità del filtro dei dati, a seconda delle dimensioni consentite nell'area di disegno. 
- Le nuove barre di controllo arrotondate su filtri dei dati ottimizzano le interazioni tramite tocco. 
- Quando un oggetto visivo diventa troppo piccolo per essere utile, assume la forma di un'icona che rappresenta il tipo di oggetto visivo sottostante. Toccare due volte l'icona per aprire l'oggetto visivo in modalità messa a fuoco e interagire con esso. Questo permette di risparmiare spazio prezioso nella pagina del report senza alcuna perdita di funzionalità.

## <a name="next-steps"></a>Passaggi successivi

- [Esercitazione: Filtri dei dati nel servizio Power BI](power-bi-visualization-slicers.md)
- Altre domande? [Provare a rivolgersi alla community di Power BI](http://community.powerbi.com/)