---
title: Tipi di informazioni dettagliate supportate da Power BI
description: Informazioni rapide e Visualizza informazioni dettagliate con Power BI.
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
ms.date: 12/20/2017
ms.author: mihart
ms.openlocfilehash: 53e5e67da9bacd9fc9dcbb770747823647aa3a3c
ms.sourcegitcommit: 6ea8291cbfcb7847a8d7bc4e2b6abce7eddcd0ea
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/21/2017
---
# <a name="types-of-insights-supported-by-power-bi"></a>Tipi di informazioni dettagliate supportate da Power BI
## <a name="how-does-insights-work"></a>Funzionamento delle informazioni dettagliate
Power BI cerca rapidamente diversi subset del set di dati durante l'applicazione di una serie di algoritmi complessi per individuare informazioni potenzialmente interessanti. Power BI analizza il maggior numero possibile di set di dati in un periodo di tempo stabilito.

È possibile eseguire le informazioni dettagliate rispetto a un set di dati o a un riquadro del dashboard.   

## <a name="what-types-of-insights-can-we-find"></a>Tipi di informazioni possibili
Questi sono alcuni degli algoritmi utilizzati:

## <a name="category-outliers-topbottom"></a>Category outlier (dall'alto al basso)
Evidenzia i casi in cui, per una misura nel modello, uno o due membri di una dimensione prevedono valori molto più grandi di altri membri della dimensione.  

![](media/service-insight-types/pbi_auto_insight_types_category_outliers.png)

## <a name="change-points-in-a-time-series"></a>Punti di modifica in una serie temporale
Evidenzia quando vi sono modifiche significative nelle tendenze in una serie temporale di dati.

![](media/service-insight-types/pbi_auto_insight_types_changepoint.png)

## <a name="correlation"></a>Correlazione
Consente di rilevare i casi in cui più misure mostrano una correlazione tra loro quando vengono tracciate in una dimensione del set di dati.

![](media/service-insight-types/pbi_auto_insight_types_correlation.png)

## <a name="low-variance"></a>Varianza bassa
Consente di rilevare i casi in cui i punti dati non sono distanti dalla media.

![](media/service-insight-types/power-bi-low-variance.png)

## <a name="majority-major-factors"></a>Maggioranza (fattori principali)
Consente di trovare casi in cui la maggior parte di un valore totale può essere attribuita a un fattore singolo quando ripartito da un'altra dimensione.  

![](media/service-insight-types/pbi_auto_insight_types_majority.png)

## <a name="overall-trends-in-time-series"></a>Tendenze generali nella serie temporale
Rileva le tendenze verso l'alto o verso il basso nei dati della serie temporale.

![](media/service-insight-types/pbi_auto_insight_types_trend.png)

## <a name="seasonality-in-time-series"></a>Stagionalità nella serie temporale
Trova modelli periodici nei dati della serie temporale, ad esempio stagionalità settimanale, mensile o annuale.

![](media/service-insight-types/pbi_auto_insight_types_seasonality_new.png)

## <a name="steady-share"></a>Condivisione stabile
Evidenzia i casi in cui è presente una correlazione padre-figlio tra la condivisione di un valore figlio in relazione al valore complessivo dell'elemento padre in una variabile continua.

![](media/service-insight-types/pbi_auto_insight_types_steadyshare.png)

## <a name="time-series-outliers"></a>Outlier della serie temporale
Per i dati in una serie temporale, viene rilevato quando sono presenti date o orari specifichi con valori sostanzialmente diversi da quella di altri valori di data/ora.

![](media/service-insight-types/pbi_auto_insight_types_time_series_outliers.png)

## <a name="next-steps"></a>Passaggi successivi
[Informazioni dettagliate di Power BI](service-insights.md)

Se è disponibile un set di dati, [ottimizzarlo per le informazioni dettagliate](service-insights-optimize.md).

Altre domande? [Provare la community di Power BI](http://community.powerbi.com/)
