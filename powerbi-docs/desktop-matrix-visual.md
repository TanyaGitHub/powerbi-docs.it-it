---
title: Usare l'oggetto visivo matrice in Power BI Desktop
description: Informazioni su come l'oggetto visivo matrice consenta i layout con rientri e l'evidenziazione granulare in Power BI Desktop
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
ms.date: 10/05/2017
ms.author: davidi
ms.openlocfilehash: 23be6fdb45572e6f47220bba666637757b7f4862
ms.sourcegitcommit: 284b09d579d601e754a05fba2a4025723724f8eb
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/15/2017
---
# <a name="use-the-matrix-visual-in-power-bi-desktop"></a>Usare l'oggetto visivo Matrice in Power BI Desktop
Con l'oggetto visivo **Matrice** è possibile creare oggetti visivi matrice (detti anche *tabelle*) nei report di **Power BI Desktop** e usare l'evidenziazione incrociata degli elementi all'interno della matrice con altri oggetti visivi. È anche possibile selezionare singole celle, colonne e righe e usare l'evidenziazione incrociata. Infine, per usare al meglio lo spazio del layout, l'oggetto visivo matrice supporta un layout con rientri.

![](media/desktop-matrix-visual/matrix-visual_2a.png)

Alla matrice sono associate molte funzionalità, che verranno illustrate nelle sezioni seguenti di questo articolo.

> [!NOTE]
> A partire dalla versione di luglio 2017 di **Power BI Desktop**, gli oggetti visivi matrice e tabella riflettono lo stile, inclusi i colori, dal **Tema report** applicato. Potrebbero non essere i colori previsti per l'oggetto visivo matrice, ma è possibile modificarli nella configurazione del **tema del report**. Per altre informazioni sui temi, vedere [**Usare i temi dei report in Power BI Desktop**](desktop-report-themes.md).
> 
> 

## <a name="using-drill-down-with-the-matrix-visual"></a>Uso del drill-down con l'oggetto visivo Matrice
L'oggetto visivo **Matrice** consente di eseguire moltissime interessanti attività di drill-down che in precedenza non erano disponibili. Ciò include la possibilità di eseguire il drill-down usando righe e colonne e persino in singole sezioni e celle. Esaminiamo il funzionamento di ognuna di queste attività.

### <a name="drill-down-on-row-headers"></a>Drill-down nelle intestazioni di riga
Nel riquadro **Visualizzazioni**, quando si aggiungono più campi alla sezione **Righe** dell'area **Campi**, si abilita il drill-down nelle righe dell'oggetto visivo matrice. La procedura è simile alla creazione di una gerarchia, che consente poi di eseguire il drill-down (e in seguito il backup) tramite la gerarchia e di analizzare i dati a ogni livello.

Nell'immagine seguente la sezione **Righe** contiene *Category* e *SubCategory*, creando un raggruppamento (o gerarchia) nelle righe in cui è possibile eseguire il drill-through.

![](media/desktop-matrix-visual/matrix-visual_4.png)

Quando per l'oggetto visivo sono stati creati raggruppamenti nella sezione **Righe**, vengono visualizzate le icone per il *drill-down* e l'*espansione* nell'angolo in alto a sinistra dell'oggetto visivo.

![](media/desktop-matrix-visual/matrix-visual_5.png)

Analogamente al comportamento di drill-down ed espansione in altri oggetti visivi, questi pulsanti consentono di eseguire il drill-down (o backup) nella gerarchia. In questo caso si può eseguire il drill-down da *Category* a *SubCategory*, come mostrato nell'immagine seguente, in cui è stata selezionata l'icona relativa al drill-down di un livello (diapason).

![](media/desktop-matrix-visual/matrix-visual_6.png)

Oltre a usare queste icone, è possibile fare clic su una delle intestazioni di riga ed eseguire il drill-down selezionandolo un'opzione nel menu visualizzato.

![](media/desktop-matrix-visual/matrix-visual_7.png)

Si noti che nel menu visualizzato sono presenti alcune opzioni, che generano risultati diversi:

Se si sceglie **Drill-down** viene espansa la matrice per *quel* livello di riga, *escludendo* tutte le altre intestazioni di riga eccetto quella su cui si è fatto clic con il pulsante destro del mouse. Nell'immagine seguente si è fatto clic con il pulsante destro del mouse su *Computers* ed è stata selezionata l'opzione **Drill-down**. Si noti che le altre righe di livello principale non compaiono più nella matrice. Questa funzionalità è molto utile e risulterà particolarmente interessante nella sezione dedicata all'**evidenziazione incrociata**.

![](media/desktop-matrix-visual/matrix-visual_8.png)

Per tornare alla precedente visualizzazione di livello principale, è possibile fare clic sull'icona **Drill-up**. Se si sceglie **Mostra il livello successivo** dal menu di scelta rapida si ottiene un elenco alfabetico di tutti gli elementi di livello successivo (in questo caso, il campo *SubCategory*), senza la categorizzazione della gerarchia di livello superiore.

![](media/desktop-matrix-visual/matrix-visual_8a.png)

Quando si fa clic sull'icona **Drill-up** nell'angolo in alto a sinistra per mostrare tutte le categorie di livello principale e quindi si fa di nuovo clic con il pulsante destro del mouse e si sceglie **Espandi al livello successivo**, viene visualizzato quanto segue:

![](media/desktop-matrix-visual/matrix-visual_9.png)

Si possono anche usare le voci di menu **Includi** ed **Escludi** per mantenere (o rimuovere) la riga su cui si è fatto clic con il pulsante destro del mouse (e le eventuali sottocategorie) nella matrice specificata.

### <a name="drill-down-on-column-headers"></a>Drill-down nelle intestazioni di colonna
Così come si può eseguire il drill-down nelle righe, si può anche eseguire il drill-down nelle **Colonne**. Nell'immagine seguente sono presenti due campi nell'area dei campi **Colonne**, creando una gerarchia simile a quella usata per le righe in precedenza in questo articolo. L'area dei campi **Colonne** include *Class* e *Color*.

![](media/desktop-matrix-visual/matrix-visual_10.png)

Nell'oggetto visivo **Matrice**, quando si fa clic con il pulsante destro del mouse su una colonna, viene visualizzata l'opzione per il drill-down. Nell'immagine seguente si fa clic con il pulsante destro del mouse su *Deluxe* e si seleziona **Drill-down**.

![](media/desktop-matrix-visual/matrix-visual_11.png)

Quando l'opzione **Drill-down** è selezionata, viene visualizzato il livello successivo della gerarchia di colonne per *Deluxe*, che in questo caso è *Color*.

![](media/desktop-matrix-visual/matrix-visual_12.png)

Le altre voci del menu di scelta rapida per le colonne funzionano esattamente come per le righe (vedere la sezione precedente, **Drill-down nelle intestazioni di riga**). Anche per le colonne, come per le righe, è possibile scegliere **Mostra il livello successivo**, **Espandi al livello successivo** e **Includi** o **Escludi**.

> [!NOTE]
> Le icone per il drill-down e il drill-up icone nell'angolo superiore sinistro dell'oggetto visivo matrice si applicano solo alle righe. Per eseguire il drill-down nelle colonne, è necessario usare il menu di scelta rapida.
> 
> 

## <a name="stepped-layout-with-matrix-visuals"></a>Layout con rientri con gli oggetti visivi matrice
L'oggetto visivo **Matrice** applica automaticamente un rientro alle sottocategorie in una gerarchia al di sotto di ogni elemento padre. Questa funzionalità è detta **Layout con rientri**.

Nella versione *originale* dell'oggetto visivo matrice, le sottocategorie sono visualizzate in una colonna totalmente diversa, occupando più spazio nell'oggetto visivo. L'immagine seguente mostra la tabella nell'oggetto visivo **matrice** originale, con le sottocategorie visualizzate in una colonna completamente separata.

![](media/desktop-matrix-visual/matrix-visual_14.png)

Nell'immagine seguente è presente un oggetto visivo **Matrice** a cui è applicato il **layout con rientri**. La categoria *Computers* include alcune sottocategorie (Computers Accessories, Desktops, Laptops, Monitors e così via) leggermente rientrate, per cui l'oggetto visivo risulta più chiaro e conciso.

![](media/desktop-matrix-visual/matrix-visual_13.png)

È possibile regolare facilmente le impostazioni **Layout con rientri**. Con l'oggetto visivo **Matrice** selezionato, nella sezione **Formato** (icona del rullo) del riquadro **Visualizzazioni** espandere la sezione **Intestazioni di riga**. Sono presenti due opzioni: l'interruttore **Layout con rientri** (per attivarlo o disattivarlo) e **Rientro del layout con rientri** (per specificare il rientro, in pixel).

![](media/desktop-matrix-visual/matrix-visual_15.png)

Se si disattiva **Layout con rientri**, le sottocategorie vengono visualizzate in un'altra colonna anziché rientrate sotto la categoria padre.

## <a name="subtotals-with-matrix-visuals"></a>Subtotali con oggetti visivi matrice
Negli oggetti visivi matrice è possibile attivare o disattivare i subtotali, sia per le righe che per le colonne. L'immagine seguente mostra che i subtotali delle righe sono impostati su **Sì**.

![](media/desktop-matrix-visual/matrix-visual_20.png)

Nella sezione **Formato** del riquadro **Visualizzazioni** espandere la scheda **Subtotali** e impostare il dispositivo di scorrimento di **Subtotali righe** su **No**. In questo caso, i subtotali non vengono visualizzati.

![](media/desktop-matrix-visual/matrix-visual_21.png)

Lo stesso processo vale per i subtotali delle colonne.

## <a name="cross-highlighting-with-matrix-visuals"></a>Evidenziazione incrociata con gli oggetti visivi matrice
Con l'oggetto visivo **Matrice** è possibile selezionare qualsiasi elemento nella matrice come base per l'evidenziazione incrociata. Quando si seleziona una colonna in un oggetto visivo **Matrice**, la colonna viene evidenziata, come anche gli altri oggetti visivi nella pagina del report. Questa caratteristica accomuna da sempre altri oggetti visivi e la selezione di un punto dati e ora è estesa anche all'oggetto visivo **Matrice**.

Anche per l'evidenziazione incrociata è possibile usare CTRL+clic per selezionare. Nell'immagine seguente, ad esempio, è stato selezionato un insieme di sottocategorie dall'oggetto visivo **Matrice**. Si noti come gli elementi che non sono stati selezionati nell'oggetto visivo sono visualizzati in grigio, mentre gli altri oggetti visivi nella pagina riflettono le selezioni effettuate nell'oggetto visivo **Matrice**.

![](media/desktop-matrix-visual/matrix-visual_16.png)

## <a name="shading-and-font-colors-with-matrix-visuals"></a>Ombreggiatura e colore carattere con gli oggetti visivi matrice
L'oggetto visivo **Matrice** consente di applicare la **formattazione condizionale** (colori e ombreggiatura) allo sfondo delle celle nella matrice, nonché di applicare la formattazione condizionale al testo e ai valori stessi.

Per applicare la formattazione condizionale, selezionare un oggetto visivo matrice ed eseguire una delle operazioni seguenti:

* Nel riquadro **Campi** fare clic con il pulsante destro del mouse su Campo e scegliere **Formattazione condizionale** dal menu di scelta rapida.
  
  ![](media/desktop-matrix-visual/matrix-visual_17.png)
* In alternativa, nel riquadro **Formato** espandere la scheda **Formattazione condizionale** e per **Scale dei colori di sfondo** o **Scale dei colori carattere** impostare il dispositivo di scorrimento su **Sì**. Attivando queste opzioni, viene visualizzato un collegamento ai *Controlli avanzati* in cui è possibile personalizzare i colori e i valori per la formattazione dei colori.
  
  ![](media/desktop-matrix-visual/matrix-visual_18.png)

Entrambi gli approcci garantiscono lo stesso risultato. Se si seleziona *Controlli avanzati* viene visualizzata la finestra di dialogo seguente che consente di apportare modifiche:

![](media/desktop-matrix-visual/matrix-visual_19.png)

## <a name="limitations-and-considerations"></a>Limitazioni e considerazioni
Per questa versione dell'oggetto visivo **Matrice** occorre tenere presenti alcune limitazioni e considerazioni.

* Il drill-down nelle colonne può essere eseguito solo usando il menu di scelta rapida e attualmente nell'oggetto visivo non è indicato il alcun modo che è possibile eseguirlo in gruppi di righe o colonne
* È solo possibile espandere contemporaneamente tutti gli elementi di un livello anziché espandere una categoria alla volta
* Nel menu di scelta rapida visualizzato quando si fa clic con il pulsante destro del mouse su un'intestazione di colonna può comparire la voce **Visualizza record**, ma non è operativa
* Attualmente non esiste una riga *Totale complessivo*
* La disattivazione della riga del subtotale nel layout con rientri non ha alcun effetto
* Le intestazioni di colonna possono essere troncate se il testo dei gruppi interni è più breve rispetto al gruppo esterno
* La modifica del rientro per il layout con rientri non dovrebbe incidere sul rientro del gruppo di righe più esterno

Le opinioni degli utenti sono sempre importanti per noi. Stiamo conducendo un **sondaggio** sull'oggetto visivo **Matrice**. Ringraziamo fin da ora gli utenti che decideranno di [partecipare al sondaggio](https://www.instant.ly/s/PYXT1).
