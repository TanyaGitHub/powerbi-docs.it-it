---
title: Esplorare i report nelle app Power BI per dispositivi mobili
description: 'Informazioni sulla visualizzazione e sull''interazione con i report nelle app Power BI nel telefono o nel tablet. Creare report nel servizio Power BI o Power BI Desktop, quindi interagire con essi nelle app per dispositivi mobili. '
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
ms.date: 10/13/2017
ms.author: maggies
ms.openlocfilehash: 3515a57f88db1c8a7b12706680c0aade8b2cdbfa
ms.sourcegitcommit: 284b09d579d601e754a05fba2a4025723724f8eb
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/15/2017
---
# <a name="explore-reports-in-the-power-bi-mobile-apps"></a>Esplorare i report nelle app Power BI per dispositivi mobili
Si applica a:

| ![iPhone](media/mobile-reports-in-the-mobile-apps/ios-logo-40-px.png) | ![iPad](media/mobile-reports-in-the-mobile-apps/ios-logo-40-px.png) | ![Telefono Android](media/mobile-reports-in-the-mobile-apps/android-logo-40-px.png) | ![Tablet Android](media/mobile-reports-in-the-mobile-apps/android-logo-40-px.png) | ![Dispositivi Windows 10](media/mobile-reports-in-the-mobile-apps/win-10-logo-40-px.png) |
|:--- |:--- |:--- |:--- |:--- |
| iPhone |iPad |Telefoni Android |Tablet Android |Dispositivi Windows 10 |

Un report di Power BI è una vista interattiva dei dati con elementi visivi che rappresentano conclusioni e approfondimenti diversi ottenuti da tali dati. La visualizzazione dei report nella app Power BI per dispositivi mobili è il terzo passaggio in un processo in tre fasi.

1. [Creare report in Power BI Desktop](desktop-report-view.md). In Power BI Desktop è persino possibile [ottimizzare un report per i telefoni](mobile-apps-view-phone-report.md). 
2. Pubblicare i report nel servizio Power BI [(https://powerbi.com)](https://powerbi.com) o nel [server di report di Power BI](report-server/get-started.md).  
3. È quindi possibile interagire con questi report nelle app Power BI per dispositivi mobili.

## <a name="open-a-power-bi-report-in-the-mobile-app"></a>Aprire un report di Power BI nell'app per dispositivi mobili
A seconda della provenienza, i report di Power BI sono archiviati in posizioni diverse nell'app per dispositivi mobili. Possono trovarsi in App, Condivisi con l'utente corrente, Aree di lavoro (inclusa l'Area di lavoro personale) oppure in un server di report. In alcuni casi si accede attraverso un dashboard correlato per ottenere un report, e talvolta sono elencati.

* In un dashboard, toccare i puntini di sospensione (...) nell'angolo superiore destro di un riquadro > **Apri report**.
  
  ![Aprire un report](media/mobile-reports-in-the-mobile-apps/power-bi-android-open-report-tile.png)
  
  Non tutti i riquadri offrono l'opzione di apertura in un report. Ad esempio, i riquadri creati ponendo una domanda nella casella Domande e risposte non aprono i report quando vengono toccati. 
  
  In un telefono, il report verrà aperto in modalità orizzontale, a meno che non sia [ottimizzato per la visualizzazione in un telefono](mobile-reports-in-the-mobile-apps.md#view-reports-optimized-for-phones).
  
  ![Report per il telefono in modalità orizzontale](media/mobile-reports-in-the-mobile-apps/power-bi-iphone-report-landscape.png)

## <a name="view-reports-optimized-for-phones"></a>Visualizzare i report ottimizzati per i telefoni
Gli autori di report di Power BI possono creare un layout di report ottimizzato in modo specifico per telefoni. In un elenco di report un report ottimizzato è contrassegnato da un'icona speciale ![Icona del report per il telefono](media/mobile-reports-in-the-mobile-apps/power-bi-phone-report-icon.png):

![Aprire il report per il telefono](media/mobile-reports-in-the-mobile-apps/power-bi-android-phone-report.png)

Quando si visualizza tale report in un telefono, viene aperto in visualizzazione verticale.

![Report in visualizzazione verticale](media/mobile-reports-in-the-mobile-apps/07-power-bi-phone-report-portrait.png)

Un report può includere una combinazione di pagine che non sono ottimizzate per i telefoni. In tal caso, quando si scorrono i report la visualizzazione passerà da verticale a orizzontale per ogni pagina.

Altre informazioni sui [report ottimizzati per la visualizzazione telefono](mobile-apps-view-phone-report.md).

## <a name="use-slicers-to-filter-a-report-page"></a>Usare i filtri dei dati per filtrare una pagina del report
Quando si progetta un report nel servizio Power BI [(https://powerbi.com)](https://powerbi.com), tenere presente che in un telefono non è possibile vedere il riquadro Filtri, ma è possibile [vedere i filtri dei dati in una pagina del report](power-bi-visualization-slicers.md). Aggiungere filtri dei dati a un report in modo che sia possibile usare i filtri dei dati per filtrare la pagina in un telefono.

* Quando si seleziona un valore in un filtro dei dati nella pagina del report, vengono filtrati gli altri oggetti visivi nella pagina.
  
  ![Filtro dei dati del report](media/mobile-reports-in-the-mobile-apps/power-bi-android-tablet-report-slicer.png)
  
  In questa illustrazione, il filtro dei dati filtra l'istogramma in modo da mostrare solo i valori di luglio.

## <a name="cross-filter-and-highlight-a-power-bi-report-page"></a>Evidenziare e filtrare a vicenda una pagina del report di Power BI
Quando si seleziona un valore in un oggetto visivo, gli altri oggetti visivi non vengono filtrati, ma vengono evidenziati i valori correlati in altri oggetti visivi.

* Toccare un valore in un oggetto visivo.
  
  ![Filtro incrociato di una pagina](media/mobile-reports-in-the-mobile-apps/power-bi-android-tablet-report-highlight.png)
  
  Se si tocca la colonna Large in un grafico, vengono evidenziati i valori correlati negli altri oggetti visivi. 

## <a name="sort-a-visual-on-an-ipad-or-a-tablet"></a>Ordinare un oggetto visivo in un iPad o un tablet
* Toccare il grafico, toccare i puntini di sospensione (**...**) e toccare il nome del campo.
  
   ![Ordinare un oggetto visivo](media/mobile-reports-in-the-mobile-apps/power-bi-android-tablet-report-sort.png)
* Per invertire l'ordinamento, toccare di nuovo i puntini di sospensione (**...**), quindi toccare di nuovo il nome dello stesso campo.

## <a name="drill-down-and-up-in-a-visual-on-an-ipad-or-a-tablet"></a>Eseguire il drill-down e il drill-up in un iPad o un tablet
Se l'autore di un report ha aggiunto questa funzionalità a un oggetto visivo, in un tablet o un iPad, è possibile eseguire il drill-down in un oggetto visivo per visualizzare i valori che ne fanno parte. È possibile [aggiungere il drill-down a un oggetto visivo](power-bi-visualization-drill-down.md) in Power BI Desktop o nel servizio Power BI. 

> [!NOTE]
> Attualmente il drill-down non funziona con le mappe nell'iPad o nel tablet.
> 
> 

* Toccare un elemento visivo. Se sono presenti frecce in su e in giù negli angoli superiori ![Icone di drill-up e drill-down](media/mobile-reports-in-the-mobile-apps/power-bi-mobile-drill-up-down.png), è possibile eseguire il drill-down. Per eseguire il drill-down in un valore, toccare la freccia nell'angolo superiore destro, quindi toccare un valore nell'oggetto visivo (in questo caso, la bolla FD-04 di colore blu scuro).
  
  ![Eseguire il drill-down in un oggetto visivo](media/mobile-reports-in-the-mobile-apps/power-bi-mobile-drill-down-one.png)
* Per eseguire il drill-down del backup, toccare la freccia in su nell'angolo superiore sinistro.
  
  ![Drill-up](media/mobile-reports-in-the-mobile-apps/power-bi-mobile-drill-up.png)

## <a name="go-back-to-my-workspace"></a>Tornare all'Area di lavoro
* Toccare la freccia accanto al nome del report > toccare **Area di lavoro personale**.
  
  ![Tornare indietro](media/mobile-reports-in-the-mobile-apps/power-bi-iphone-report-back.png)

## <a name="next-steps"></a>Passaggi successivi
* [Visualizzare e interagire con i report di Power BI ottimizzati per il proprio telefono](mobile-apps-view-phone-report.md)
* [Creare una versione di un report ottimizzata per i telefoni](desktop-create-phone-report.md)
* Domande? [Provare a rivolgersi alla community di Power BI](http://community.powerbi.com/)
