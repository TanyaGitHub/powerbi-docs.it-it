---
title: Usare le misure in Power BI Desktop
description: Misure in Power BI Desktop
author: davidiseminger
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-desktop
ms.topic: conceptual
ms.date: 08/08/2018
ms.author: davidi
LocalizationGroup: Model your data
ms.openlocfilehash: d4b0ad34d200e3d94c60c7e3a3f524a3f3ed09cf
ms.sourcegitcommit: 0ff358f1ff87e88daf837443ecd1398ca949d2b6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/21/2018
ms.locfileid: "46550007"
---
# <a name="measures-in-power-bi-desktop"></a>Misure in Power BI Desktop

**Power BI Desktop** consente di creare informazioni dettagliate sui dati con pochi semplici clic. Tuttavia, a volte i dati non includono tutto ciò che occorre per rispondere ad alcune domande importanti. A questo scopo possono essere usate le misure.

Le misure vengono usate in alcune delle analisi dei dati più comuni. Ad esempio somme, medie, valori minimi o massimi, conteggi o calcoli più avanzati creati dall'utente con una formula DAX. I risultati calcolati delle misure vengono aggiornati costantemente in base alle operazioni dell'utente nei report e consentono un'esplorazione dei dati ad hoc, rapida e dinamica, come verrà illustrato nelle sezioni successive.

## <a name="understanding-measures"></a>Informazioni sulle misure

In **Power BI Desktop** le misure vengono create e usate in **Visualizzazione Report** e **Vista dati**. Le misure create dall'utente vengono visualizzate nell'elenco di campi con un'icona a forma di calcolatrice. È possibile assegnare qualsiasi nome alle misure e aggiungerle a una visualizzazione nuova o esistente con le normali procedure usate per gli altri campi.

![](media/desktop-measures/measuresinpbid_measinfieldlist.png)

> [!NOTE]
> Potrebbe anche essere interessante ottenere informazioni sulle **misure rapide**, cioè misure già pronte selezionabili nelle finestre di dialogo. Si tratta di un buon metodo per creare rapidamente le misure, nonché per apprendere la sintassi DAX, perché le formule DAX create automaticamente sono disponibili per la revisione. Vedere l'articolo: [misure rapide](desktop-quick-measures.md).
> 
> 

## <a name="data-analysis-expressions"></a>Data Analysis Expressions

Le misure calcolano un risultato da una formula di espressione. Quando si creano misure personalizzate, viene usato il linguaggio delle formule [DAX (Data Analysis Expressions)](https://msdn.microsoft.com/library/gg413422.aspx). DAX include una libreria con oltre 200 funzioni, operatori e costrutti. Questa libreria offre un'enorme flessibilità per la creazione di misure di calcolo dei risultati per quasi tutte le esigenze di analisi dei dati.

Le formule DAX sono molto simili alle formule di Excel. DAX include anche molte delle stesse funzioni disponibili in Excel, ad esempio DATE, SUM e LEFT. Le funzioni DAX, tuttavia, sono pensate per essere usate con dati relazionali come quelli in Power BI Desktop.

## <a name="lets-look-at-an-example"></a>Esempio
Jan è un responsabile delle vendite di Contoso. Le è stato richiesto di fornire delle proiezioni sulle vendite dei rivenditori per il prossimo anno fiscale. Jan decide di basare le stime sull'importo delle vendite dell'anno precedente, con un 6% di incremento annuale risultante da diverse promozioni pianificate nei successivi sei mesi.

Per visualizzare le stime, Jan importa i dati sulle vendite dell'anno precedente in Power BI Desktop. Individua il campo SalesAmount nella tabella Reseller Sales. I dati importati contengono solo l'importo delle vendite dell'anno precedente, quindi rinomina il campo SalesAmount in Last Years Sales. Jan trascina quindi Last Years Sales nell'area di disegno del report, in cui viene visualizzato in un grafico come valore singolo pari alla somma di tutte le vendite dei rivenditori dell'anno precedente.

Jan nota che anche se non ha specificato un calcolo, ne è stato fornito uno automaticamente. Power BI Desktop ha creato la propria misura sommando tutti i valori in Last Years Sales.

Tuttavia, a Jan occorre una misura per calcolare le proiezioni delle vendite per l'anno successivo, che saranno basate sulle vendite dell'anno precedente moltiplicate per 1,06 per tenere conto dell'incremento del 6% previsto per le vendite. Per questo calcolo crea una misura personalizzata. Usando la funzionalità Nuova misura, crea una nuova misura e immette la seguente formula DAX:

    Projected Sales = SUM('Sales'[Last Years Sales])*1.06

Jan trascina quindi la nuova misura Projected Sales nel grafico.

![](media/desktop-measures/measuresinpbid_lastyearsales.png)

In poco tempo e con il minimo sforzo, ora Jan ha una misura per calcolare le vendite previste. Può analizzare ulteriormente le proiezioni filtrando per rivenditori specifici o aggiungendo altri campi al report.

## <a name="data-categories-for-measures"></a>Categorie di dati per le misure

È anche possibile selezionare le categorie di dati per le misure. 

Tra le altre cose, in questo modo è possibile usare le misure per creare gli URL in modo dinamico e contrassegnare la categoria di dati come un URL Web. 

È possibile creare tabelle che visualizzano le misure come URL Web e fare in modo che sia possibile fare clic sull'URL creato in base alla selezione. Ciò è particolarmente utile quando ci si vuole collegare ad altri report di Power BI con [parametri di filtro URL](service-url-filters.md).

## <a name="learn-more"></a>Altre informazioni
In questo articolo è stata fornita solo una rapida introduzione alle misure, ma ci sono molte altre risorse che spiegano come creare misure personalizzate. Vedere [Esercitazione: Creare misurazioni personalizzate in Power BI Desktop](desktop-tutorial-create-measures.md), da dove è possibile scaricare un file di esempio e ottenere lezioni passo-passo su come creare nuove misure.  

Per approfondire la conoscenza su DAX, assicurarsi di consultare [Nozioni di DAX in Power BI Desktop](desktop-quickstart-learn-dax-basics.md). [Riferimento a Data Analysis Expressions (DAX)](https://msdn.microsoft.com/library/gg413422.aspx) fornisce articoli dettagliati su tutte le funzioni, la sintassi, gli operatori e le convenzioni di denominazione. DAX è stato incluso per diversi anni in Power Pivot in Excel e in SQL Server Analysis Services, quindi sono disponibili molte altre risorse utili da consultare. Vedere la pagina [Wiki del centro risorse DAX](http://social.technet.microsoft.com/wiki/contents/articles/1088.dax-resource-center.aspx), in cui membri esperti della community BI condividono le proprie conoscenze su DAX.



