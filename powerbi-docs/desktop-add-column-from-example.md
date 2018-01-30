---
title: Aggiungere una colonna da un esempio in Power BI Desktop
description: Creare rapidamente una nuova colonna in Power BI Desktop usando le colonne esistenti come esempi
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
ms.date: 11/21/2017
ms.author: davidi
ms.openlocfilehash: f82bcc9d9add1683f593da6457fde2a4bbce2e02
ms.sourcegitcommit: 47ea78f58ad37a751171d01327c3381eca3a960e
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/22/2017
---
# <a name="add-a-column-from-an-example-in-power-bi-desktop"></a>Aggiungere una colonna da un esempio in Power BI Desktop
A partire dalla versione di aprile 2017 di **Power BI Desktop**, è possibile aggiungere nuove colonne di dati al modello usando l'**Editor di query** e fornendo semplicemente uno o più valori di esempio per la nuova colonna. È possibile creare un nuovo esempio di colonna da una selezione corrente oppure fornendo input basati su tutte le colonne (o solo su alcune di esse) in una determinata tabella.

![](media/desktop-add-column-from-example/add-column-from-example_01.png)

Questo approccio consente di creare rapidamente e facilmente nuove colonne ed è ideale nelle situazioni seguenti:

* Si conosce il risultato dei dati che si vuole ottenere nella nuova colonna, ma non si è certi di quale trasformazione (o raccolta di trasformazioni) consenta di ottenerlo.
* Si sa già qual è la trasformazione necessaria, ma non si è sicuri di dove fare clic o selezionare nell'interfaccia utente per eseguirla.
* Si hanno tutte le informazioni sulle trasformazioni necessarie usando un'espressione *Colonna personalizzata* in **M**, ma una o più espressioni non sono disponibili per la selezione o l'aggiunta nell'interfaccia utente.

L'uso della funzionalità **Aggiungi colonna da esempi** è semplice e lineare. Nelle prossime sezioni, si osserverà quanto sia facile usarla.

## <a name="use-query-editor-to-add-a-new-column-from-examples"></a>Usare l'Editor di query per aggiungere una nuova colonna da esempi
Per creare una nuova colonna da un esempio, avviare l'**Editor di query**. A tale scopo, selezionare **Modifica query** nella barra multifunzione **Home** in **Power BI Desktop**.

![](media/desktop-add-column-from-example/add-column-from-example_02.png)

In questo articolo, verranno usati i dati dall'articolo di Wikipedia seguente (è un collegamento, quindi è possibile fare clic su di esso per ottenere i dati e seguire la procedura):

* [**Elenco di stati e territori degli Stati Uniti**](https://wikipedia.org/wiki/List_of_states_and_territories_of_the_United_States)

Dopo aver avviato l'**Editor di query** e aver caricato alcuni dati, sarà possibile iniziare ad aggiungere una colonna da esempi. Per aggiungere una nuova colonna, nell'**Editor di query** selezionare la scheda **Aggiungi colonna** nella barra multifunzione e quindi selezionare **Colonna da esempi**. Se si sceglie l'elenco a discesa, è possibile selezionare **Da tutte le colonne** (impostazione predefinita, se si seleziona solo il pulsante anziché l'elenco a discesa) o **Dalla selezione**. In questo articolo verrà esaminata la procedura dopo aver selezionato **Da tutte le colonne**.

![](media/desktop-add-column-from-example/add-column-from-example_03.png)

## <a name="the-add-column-from-examples-pane"></a>Riquadro Aggiungi colonna da esempi
Dopo aver effettuato una selezione per aggiungere una nuova colonna da esempi, viene visualizzato un nuovo riquadro che mostra le colonne nella tabella corrente (potrebbe essere necessario scorrere per visualizzarle tutte). La nuova **Colonna1** viene visualizzata anche a destra, cioè la colonna che **Power BI Desktop** creerà in base agli esempi dell'utente. Sotto la nuova intestazione **Colonna1** ci sono celle vuote, in cui è possibile digitare i propri esempi, che Power BI usa per creare regole e trasformazioni corrispondenti all'esempio.

Si noti anche che si tratta di un **Passaggio applicato** nel riquadro **Impostazioni query**. Come sempre, l'**Editor di query** registrerà i passaggi della trasformazione e li applicherà alla query, in quest'ordine.

![](media/desktop-add-column-from-example/add-column-from-example_04.png)

Questo è il riquadro **Aggiungi colonne da esempi** e consiste in quattro aree principali:

1. La **Barra dei comandi**, che include una breve descrizione della funzionalità o della trasformazione.
2. L'opzione **Invia commenti e suggerimenti**, per aiutare Power BI a migliorare questa funzionalità.
3. I pulsanti **OK** e **Annulla**, che consentono di salvare le trasformazioni e aggiungere la colonna o annullare.
4. L'area della nuova colonna, in cui è possibile digitare i valori di esempio in qualsiasi riga (per fornire a Power BI il proprio esempio) in relazione alle altre colonne nella stessa riga.

![](media/desktop-add-column-from-example/add-column-from-example_05.png)

Mentre si digita il proprio esempio nella nuova colonna, Power BI offre un'anteprima dell'aspetto della colonna che si sta creando, in base alle trasformazioni che rileva. Ad esempio, si è digitato *Alabama* nella prima riga corrispondente al valore *Alabama* nella prima colonna della tabella: non appena si preme *INVIO*, Power BI compila la colonna in base a tale valore.

Quindi, però, si è passati alla riga che includeva *Massachusetts [E]* ed è stata eliminata l'ultima parte *[E]* (perché indesiderata); Power BI ha rilevato la modifica e usato l'esempio per creare una trasformazione. Si noti la spiegazione della trasformazione nel riquadro centrale superiore.

![](media/desktop-add-column-from-example/add-column-from-example_06.png)

Mentre si continua a fornire esempi, l'**Editor di query** aggiunge altre trasformazioni. Quando si è soddisfatti, è possibile selezionare **OK** per salvare le modifiche.

## <a name="see-add-column-from-examples-in-action"></a>Vedere Aggiungi colonna da esempi in azione
Per vedere questa funzionalità in azione, guardare il video seguente, che ne mostra il funzionamento in base all'origine dati fornita precedentemente in questo esempio. Dopo la visione, si potrà procedere autonomamente.

<iframe width="560" height="315" src="https://www.youtube.com/embed/-ykbVW9wQfw" frameborder="0" allowfullscreen></iframe>

## <a name="considerations-and-limitations"></a>Considerazioni e limitazioni
Sono disponibili molte trasformazioni quando si usa il riquadro **Aggiungi colonna da esempi**, ma non tutte le trasformazioni sono incluse. Di seguito sono elencate tutte le trasformazioni che *sono* supportate.

* **Riferimento**
  
  * Riferimento a una colonna specifica (incluse le trasformazioni di taglio, pulizia e maiuscole/minuscole)

* **Trasformazioni di testo**
  
  * Combina (supporta la combinazione di stringhe letterali e di interi valori di colonna)
  * Sostituisci
  * Lunghezza
  * Estrai   
    * Primi caratteri
    * Ultimi caratteri
    * Intervallo
    * Testo prima del delimitatore
    * Testo dopo il delimitatore
    * Testo racchiuso tra delimitatori
    * Lunghezza

* Le **trasformazioni di testo** supportate seguenti sono disponibili a partire dalla versione di novembre 2017 di **Power BI Desktop**:
    
  * Rimuovi caratteri
  * Mantieni caratteri

> [!NOTE]
> Tutte le trasformazioni di *testo* tengono conto dell'eventuale necessità di tagliare, pulire o di applicare una trasformazione di maiuscole/minuscole al valore della colonna.
> 
> 

* **Trasformazioni di data**
  
  * Giorno
  * Giorno della settimana
  * Nome giorno della settimana
  * Giorno dell'anno
  * Mese
  * Nome del mese
  * Trimestre dell'anno
  * Settimana del mese
  * Settimana dell'anno
  * Anno
  * Età
  * Inizio dell'anno
  * Fine dell'anno
  * Inizio del mese
  * Fine del mese
  * Inizio del trimestre
  * Giorni del mese
  * Fine del trimestre
  * Inizio della settimana
  * Fine della settimana
  * Giorno del mese
  * Inizio della giornata
  * Fine della giornata


* **Trasformazioni di ora**
  
  * Ora
  * Minuto
  * Secondo  
  * In Ora Locale

> [!NOTE]
> Tutte le trasformazioni di *data* e *ora* prendono in considerazione l'eventuale necessità di convertire il valore della colonna in *Date*, *Time* o *DateTime*.
> 
> 

* **Trasformazioni di numero** 

  * Valore assoluto
  * Arcocoseno
  * Arcoseno
  * Arcotangente
  * Converti in numero
  * Coseno
  * Cubo
  * Dividi
  * Esponente
  * Fattoriale
  * Divisione intera
  * È pari
  * È dispari
  * Ri
  * Logaritmo in base 10
  * Modulo
  * Moltiplica
  * Arrotonda per difetto
  * Arrotonda per eccesso
  * Segno
  * Seno
  * Radice quadrata
  * Quadrato
  * Sottrai
  * Somma
  * Tangente

* La **trasformazione di numero** supportata seguente è disponibile a partire dalla versione di novembre 2017 di **Power BI Desktop**:

  * Bucket/Intervalli

* **Generale**
  
  * Colonna condizionale