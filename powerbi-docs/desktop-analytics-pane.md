---
title: Uso del riquadro Analisi in Power BI Desktop
description: Creare linee di riferimento dinamiche per gli oggetti visivi in Power BI Desktop
services: powerbi
documentationcenter: 
author: davidiseminger
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
ms.date: 10/12/2017
ms.author: davidi
ms.openlocfilehash: add95532f645c143aea0f58200f9e3b1467320d0
ms.sourcegitcommit: 284b09d579d601e754a05fba2a4025723724f8eb
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/15/2017
---
# <a name="using-the-analytics-pane-in-power-bi-desktop"></a>Uso del riquadro Analisi in Power BI Desktop
Con il riquadro **Analisi** in **Power BI Desktop** è possibile aggiungere *linee di riferimento* dinamiche agli oggetti visivi e incentrare l'attenzione su tendenze o informazioni importanti. Il riquadro **Analisi** è disponibile nell'area **Visualizzazioni** di Power BI Desktop, a partire dalla versione di agosto 2016, ovvero la versione 2.37.4464.321 o versioni successive, come illustrato di seguito.

![](media/desktop-analytics-pane/analytics-pane_1.png)

> [!NOTE]
> Il riquadro **Analisi** viene visualizzato solo quando si seleziona un oggetto visivo nell'area di disegno di Power BI Desktop.
> 
> 

## <a name="enable-forecasting-preview"></a>Abilitare la previsione (anteprima)
Con il rilascio di settembre 2016 di **Power BI Desktop** (versione 2.39.4526.362 o versioni successive), è anche possibile eseguire le *previsioni* dal riquadro **Analisi**. È necessario abilitare questa funzionalità di anteprima passando a **File > Opzioni e impostazioni -> Opzioni** quindi selezionando **Funzionalità di anteprima** dal riquadro a sinistra. Per abilitare la funzionalità, selezionare la casella di controllo accanto a **Previsione** come mostrato nella figura seguente. Per rendere effettiva la modifica, è necessario riavviare **Power BI Desktop**.

![](media/desktop-analytics-pane/analytics-pane_1b.png)

## <a name="using-the-analytics-pane"></a>Uso del riquadro Analisi
Con il riquadro **Analisi** è possibile creare i seguenti tipi di linee di riferimento dinamiche, anche se non tutte le linee sono disponibili per tutti i tipi di oggetti visivi:

* Linea costante asse X
* Linea costante asse Y
* Linea minima
* Linea massima
* Linea media
* Linea mediana
* Linea percentile

Le sezioni seguenti mostrano come usare il riquadro **Analisi** e le linee di riferimento dinamiche nelle visualizzazioni.

Per visualizzare le linee di riferimento dinamiche disponibili per un oggetto visivo, seguire questa procedura:

1. Selezionare o creare un oggetto visivo, quindi selezionare l'icona **Analisi** dalla sezione **Visualizzazioni**.
   
   ![](media/desktop-analytics-pane/analytics-pane_2.png)
2. Selezionare la freccia rivolta verso il basso per il tipo di linea che si desidera creare per espandere le opzioni. In questo caso, si selezionerà **Linea media**.
   
   ![](media/desktop-analytics-pane/analytics-pane_3.png)
3. Per creare una nuova linea, selezionare **+ Aggiungi**. È quindi possibile specificare un nome per la linea facendo doppio clic sulla casella di testo, quindi digitando il nome.
   
   Sono disponibili moltissime opzioni per la linea, ad esempio per impostare *colore*, *trasparenza*, *stile* e *posizione* relativamente a elementi dati dell'oggetto visivo, oltre alla possibilità di scegliere se includere l'etichetta. Soprattutto, è possibile selezionare su quale **Misura** nell'oggetto visivo si desidera basare la linea selezionando il menu a discesa **Misura**, che viene automaticamente popolato con gli elementi dati dell'oggetto visivo. In questo caso, si selezionerà *Weather* come misura, si etichetterà l'opzione come *Average Weather* e si personalizzeranno altre opzioni come illustrato di seguito.
   
   ![](media/desktop-analytics-pane/analytics-pane_4.png)
4. Se si desidera visualizzare un'etichetta dati, spostare il dispositivo di scorrimento **Etichetta dati** su On. In questo caso, si ottiene una serie completa di opzioni aggiuntive per l'etichetta dati come illustrato nell'immagine seguente.
   
   ![](media/desktop-analytics-pane/analytics-pane_5.png)
5. Notare il numero visualizzato accanto all'elemento **Linea media** nel riquadro **Analisi**. Questo numero indica quante linee dinamiche sono attualmente presenti nell'oggetto visivo e di che tipo sono. Se si aggiunge una **Linea massima** per *Cost of Living*, è possibile vedere nel riquadro **Analisi** che è ora presente anche una linea di riferimento dinamica **Linea massima** applicata a questo oggetto visivo.
   
   ![](media/desktop-analytics-pane/analytics-pane_6.png)

Se l'oggetto visivo selezionato non può contenere linee di riferimento dinamiche applicate, in questo caso un oggetto visivo **Mappa**, verrà visualizzato quanto segue nel momento in cui si seleziona il riquadro **Analisi**.

![](media/desktop-analytics-pane/analytics-pane_7.png)

Sono moltissime le informazioni interessanti da poter evidenziare creando linee di riferimento dinamiche con il riquadro **Analisi**.

Sono previste altre funzionalità, ad esempio l'espansione degli oggetti visivi che possono avere linee di riferimento dinamiche applicate, pertanto è consigliabile tenersi aggiornati sulle novità.

## <a name="apply-forecasting"></a>Applicare la previsione
È possibile usare la funzionalità **Previsione** selezionando un oggetto visivo, quindi espandendo la sezione **Previsione** del riquadro **Analisi**. È possibile specificare molti input per modificare la previsione, ad esempio *Lunghezza previsione*, *Intervallo di confidenza* e altri. La figura seguente mostra un oggetto visivo di base con previsione applicata, ma è possibile attingere alla propria immaginazione (e sperimentare con la funzionalità *Previsione*) per vedere come è possibile applicarla ai propri modelli.

![](media/desktop-analytics-pane/analytics-pane_8.png)

## <a name="limitations"></a>Limitazioni
La possibilità di usare linee di riferimento dinamiche dipende dal tipo di oggetto visivo in uso. L'elenco seguente mostra le linee dinamiche attualmente disponibili per i vari oggetti visivi:

Gli oggetti visivi seguenti possono usufruire pienamente delle linee dinamiche:

* Grafico ad aree
* Grafico a linee
* Grafico a dispersione
* Istogramma a colonne raggruppate
* Grafico a barre raggruppate

Gli oggetti visivi seguenti possono usare solo una *linea costante* dal riquadro **Analisi**:

* Area in pila
* Barre in pila
* Istogramma in pila
* Barre in pila 100%
* Istogramma in pila 100%

Per gli oggetti visivi seguenti è attualmente disponibile solo la *linea di tendenza*:

* Linee non in pila
* Istogramma a colonne raggruppate

Infine, gli oggetti visivi non cartesiani attualmente non possono applicare linee dinamiche dal riquadro **Analisi**, ad esempio:

* Matrice
* Grafico a torta
* Grafico ad anello
* Tabella

## <a name="next-steps"></a>Passaggi successivi
Power BI Desktop offre infinite possibilità. Per altre informazioni sulle capacità disponibili, vedere le risorse seguenti:

* [Novità di Power BI Desktop](desktop-latest-update.md)
* [Scarica Power BI Desktop](desktop-get-the-desktop.md)
* [Introduzione a Power BI Desktop](desktop-getting-started.md)
* [Panoramica delle query con Power BI Desktop](desktop-query-overview.md)
* [Tipi di dati in Power BI Desktop](desktop-data-types.md)
* [Effettuare il data shaping e combinare i dati con Power BI Desktop](desktop-shape-and-combine-data.md)
* [Attività di query comuni in Power BI Desktop](desktop-common-query-tasks.md)    
