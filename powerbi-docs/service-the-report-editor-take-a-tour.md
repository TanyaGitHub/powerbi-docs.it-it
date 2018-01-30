---
title: Presentazione dell'editor di report
description: Presentazione dell'editor di report.
services: powerbi
documentationcenter: 
author: mihart
manager: kfile
backup: 
editor: 
featuredvideoid: IkJda4O7oGs
tags: 
qualityfocus: no
qualitydate: 
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 10/30/2017
ms.author: mihart
ms.openlocfilehash: e5ee6db22fe0fa7fd1e61ebbfb7dbee9d3458159
ms.sourcegitcommit: 99cc3b9cb615c2957dde6ca908a51238f129cebb
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/13/2017
---
# <a name="the-report-editortake-a-tour"></a>Presentazione dell'editor di report
Gli editor di report disponibili nel servizio Power BI e in Power BI Desktop sono molto simili. Il video mostra l'editor di report in Power BI Desktop e questo articolo illustra l'editor di report nel servizio Power BI. 

<iframe width="560" height="315" src="https://www.youtube.com/embed/IkJda4O7oGs" frameborder="0" allowfullscreen></iframe>

Nel servizio Power BI l'*editor di report* è disponibile solo nella [Visualizzazione di modifica](service-reading-view-and-editing-view.md). Per aprire un report nella Visualizzazione di modifica, è necessario essere un proprietario del report.

L'editor di report di Power BI è organizzato in tre sezioni:  

1. Riquadri **Campi**, **Visualizzazioni** e **Filtri**
2. Barre di spostamento superiori    
3. Area di disegno report     

![](media/service-the-report-editor-take-a-tour/power-bi-report-canvas.png)

## <a name="1-the-report-editor-panes"></a>1. Riquadri dell'editor di report
![](media/service-the-report-editor-take-a-tour/power-bi-report-panes.png)

All'apertura di un report sono visibili tre riquadri, ovvero Visualizzazioni, Filtri e Campi. I riquadri sul lato sinistro, Visualizzazioni e Filtri, controllano l'aspetto delle visualizzazioni, vale a dire tipo, colori, filtro, formattazione.  Il riquadro a destra, Campi, consente di gestire i dati sottostanti usati nelle visualizzazioni. 

Il contenuto visualizzato nell'editor di report varia in base alle selezioni effettuate nell'area di disegno report.  Ad esempio, quando si seleziona un oggetto visivo singolo: 

|  |  |
| --- | --- |
| ![](media/service-the-report-editor-take-a-tour/power-bi-panes.png) |<ul><li>La parte superiore del riquadro Visualizzazione identifica il tipo di oggetto visivo in uso, in questo esempio un istogramma a colonne raggruppate.<br><br></li> <li>La parte inferiore del riquadro Visualizzazione (potrebbe essere necessario scorrere verso il basso) mostra i campi usati nell'oggetto visivo. Questo grafico usa FiscalMonth, DistrictManager e Total Sales Variance. <br><br></li><li>Il riquadro Filtri (potrebbe essere necessario scorrere verso il basso) mostra eventuali filtri che sono stati applicati. <br><br></li><li>Il riquadro Campi elenca le tabelle disponibili e, se si espande il nome di una tabella, i campi che costituiscono tale tabella. Il carattere giallo indica che almeno un campo della tabella usato nella visualizzazione.<br><br></li><li>![](media/service-the-report-editor-take-a-tour/power-bi-paint-roller-icon.png) Per visualizzare il riquadro di formattazione, per la visualizzazione selezionata, selezionare l'icona del rullo.<br><br></li><li>![](media/service-the-report-editor-take-a-tour/power-bi-magnifying-icon.png) Per visualizzare il riquadro Analisi, selezionare l'icona della lente di ingrandimento.</ul> |
|  | |

## <a name="the-visualizations-pane-from-top-to-bottom"></a>Riquadro Visualizzazioni (dall'alto verso il basso)
![](media/service-the-report-editor-take-a-tour/selectviz.png)

In questo riquadro è possibile selezionare un tipo di visualizzazione. Le immagini di piccole dimensioni sono dette *modelli*. Nell'immagine precedente è selezionato un grafico a barre raggruppate. Se invece di selezionare prima un tipo di visualizzazione, si inizia a creare una visualizzazione selezionando i campi, Power BI sceglierà automaticamente il tipo di visualizzazione. È possibile accettare il tipo proposto da Power BI o cambiarlo selezionando un modello diverso. È possibile cambiare tipo più volte finché non si individua quello che meglio rappresenta i propri dati.

### <a name="manage-the-fields-used-in-your-visual"></a>Gestire i campi usati nell'oggetto visivo
![](media/service-the-report-editor-take-a-tour/power-bi-field-list.png)

I bucket (noti anche come *aree*) visualizzati in questo riquadro variano a seconda del tipo di visualizzazione selezionato.  Ad esempio, se si è selezionato un grafico a barre, si vedranno bucket per: Valori, Asse e Legenda. Quando si seleziona un campo o lo si trascina nell'area di disegno, Power BI lo aggiunge a uno dei bucket.  È anche possibile trascinare campi dall'elenco Campi direttamente nei bucket.  Alcuni bucket sono limitati a determinati tipi di dati.  Ad esempio, **Valori** non accetta i campi non numerici. Dunque, se si trascina un campo **employeename** nel bucket **Valori**, Power BI lo cambia in **count of employeename**.

### <a name="remove-a-field"></a>Rimuovere un campo
Per rimuovere un campo dalla visualizzazione, selezionare la **X** a destra del nome del campo.

![](media/service-the-report-editor-take-a-tour/deletefield.png)

Per altre informazioni, vedere [Aggiungere visualizzazioni a un report di Power BI](power-bi-report-add-visualizations-i.md).

### <a name="format-your-visuals"></a>Formattare gli oggetti visivi
Selezionare l'icona del rullo per visualizzare il riquadro Formato. L'opzione disponibile dipende dal tipo di visualizzazione selezionato.

![](media/service-the-report-editor-take-a-tour/power-bi-formatting.png)

Le opzioni di formattazione sono praticamente infinite.  Per informazioni, esplorarle autonomamente o vedere gli articoli seguenti:

* [Personalizzazione di visualizzazione, sfondo e legenda della visualizzazione](power-bi-visualization-customize-title-background-and-legend.md)
* [Formattazione dei colori](service-getting-started-with-color-formatting-and-axis-properties.md)
* [Personalizzazione delle proprietà degli assi X e Y](power-bi-visualization-customize-x-axis-and-y-axis.md)

### <a name="add-analytics-to-your-visualizations"></a>Aggiungere il riquadro Analisi alle visualizzazioni
Per visualizzare il riquadro Analisi, selezionare l'icona della lente di ingrandimento. L'opzione disponibile dipende dal tipo di visualizzazione selezionato.

![](media/service-the-report-editor-take-a-tour/power-bi-analytics.png)    
Il riquadro Analisi nel servizio Power BI consente di aggiungere linee di riferimento dinamiche alle visualizzazioni e di concentrare l'attenzione su tendenze o informazioni importanti. Per altre informazioni, vedere [Riquadro Analisi nel servizio Power BI](service-analytics-pane.md) o [Riquadro Analisi in Power BI Desktop](desktop-analytics-pane.md).

- - -
## <a name="the-filters-pane"></a>Riquadro Filtri
Consente di visualizzare, impostare e modificare i filtri a livello di pagina, report, drill-through e oggetto visivo.

![](media/service-the-report-editor-take-a-tour/power-bi-formatting-pane.png)

Per altre informazioni, vedere [Aggiungere un filtro a un report](power-bi-report-add-filter.md).

- - -
## <a name="the-fields-pane"></a>Riquadro Campi
Il riquadro Campi mostra tabelle e campi esistenti nei dati e utilizzabili per creare visualizzazioni.

|  |  |
| --- | --- |
| ![](media/service-the-report-editor-take-a-tour/reportfields.png) |<ul><li>Trascinare un campo sulla pagina per avviare una nuova visualizzazione.  È anche possibile trascinare un campo in una visualizzazione esistente per aggiungervi il campo.<br><br></li> <li>Quando si aggiunge un segno di spunta accanto a un campo, Power BI aggiunge tale campo alla visualizzazione attiva o a quella nuova. Decide anche in quale bucket posizionare il campo.  Ad esempio, il campo deve essere usato come legenda, asse o valore? Power BI ipotizza l'uso del campo, che può comunque essere spostato in un altro bucket se necessario. <br><br></li><li>In entrambi i casi, ogni campo selezionato viene aggiunto al riquadro Visualizzazioni nell'editor di report.</li></ul> |

**NOTA**: se si usa Power BI Desktop, sono anche disponibili opzioni per mostrare/nascondere campi, aggiungere calcoli e così via.

### <a name="what-do-the-field-icons-mean"></a>Cosa significano le icone di campo?
* **Aggregati ∑** Un aggregato è un valore numerico che verrà sommato o per cui sarà calcolata la media, ad esempio. Gli aggregati vengono importati con i dati definiti nel modello di dati su cui si basa il report.
  Per altre informazioni, vedere [Aggregati nei report di Power BI](service-aggregates.md).
* ![](media/service-the-report-editor-take-a-tour/pbi_calculated_icon.png) **Misure calcolate (dette anche campi calcolati)**  
   Ogni campo calcolato ha una propria formula hardcoded. Non è possibile modificare il calcolo; ad esempio, se è una somma, può essere solo una somma. Per altre informazioni, leggere [Informazioni sulle misure](desktop-measures.md)
* ![](media/service-the-report-editor-take-a-tour/icon.png) **Campi univoci**  
   I campi con questa icona sono stati importati da Excel e sono impostati in modo da mostrare tutti i valori, anche se hanno duplicati. Ad esempio i dati potrebbero contenere due record per utenti denominati "Lorenzo Russo" e ognuno verrà considerato come univoco (non saranno sommati).  
* **![](media/service-the-report-editor-take-a-tour/pbi_geo_icon.png) Campi geografici**  
   I campi di posizione possono essere usati per creare visualizzazioni mappa. 
* **![](media/service-the-report-editor-take-a-tour/power-bi-hierarchy-icon.png) Gerarchia**  
   Selezionare la freccia per visualizzare i campi che costituiscono la gerarchia. 

- - -
## <a name="2-the-top-navigation-bar"></a>2. Barra di spostamento superiore
Le azioni disponibili nella barra di spostamento superiore sono numerose e in continuo aumento. Per informazioni su una determinata azione, usare il Sommario della documentazione o la casella di ricerca di Power BI.

## <a name="3-the-report-canvas"></a>3. Area di disegno report
Nell'area di disegno report viene visualizzato il lavoro. Quando si usano i riquadri Campi, Filtri e Visualizzazioni per creare oggetti visivi, questi vengono creati e visualizzati nell'area di disegno report. Ogni scheda nella parte inferiore dell'area di disegno rappresenta una pagina del report. Selezionare una scheda per aprire tale pagina. 

## <a name="next-steps"></a>Passaggi successivi:
[Creare un report](service-report-create-new.md)

[Modificare un report](service-interact-with-a-report-in-editing-view.md)

Altre informazioni sui [report in Power BI](service-reports.md)

[Introduzione a Power BI](service-get-started.md)

[Power BI - Concetti di base](service-basic-concepts.md)

Altre domande? [Provare la community di Power BI](http://community.powerbi.com/)
