La sezione di **apprendimento guidato** di Power BI è stata progettata per fornire informazioni introduttive su **DAX**.

**DAX** è l'acronimo di **Data Analysis Expressions** e indica il linguaggio delle formule usato in Power BI, anche in background. DAX è disponibile anche in altre offerte Microsoft, ad esempio Power Pivot e il modello tabulare di SSAS, ma questa raccolta di argomenti di apprendimento guidato è incentrata sulla modalità di utilizzo di DAX, anche da parte dell'utente, in Power BI.

## <a name="dax-and-this-guided-learning-video-series"></a>DAX e la serie di video di apprendimento guidato
L'obiettivo di questa sezione di **apprendimento guidato** consiste nel fornire informazioni di base essenziali su DAX, ovvero informazioni generali su DAX, informazioni sul funzionamento e sulle funzionalità più utili, in base a quanto illustrato (e appreso con molta esperienza) da un noto esperto di DAX, [Alberto Ferrari](http://www.sqlbi.com/learning-dax).

![Descrizione di Alberto Ferrari](media/7-1-intro-to-dax/intro_dax_6_alberto_ferrari.png)

I video in questa sezione di **apprendimento guidato** su **DAX** forniscono informazioni di base su DAX dal punto di vista del funzionamento del linguaggio delle formule DAX. Ciò risulta utile quando si creano formule DAX completamente nuove, ma è anche molto utile per comprendere il modo in cui Power BI crea le formule DAX quando si creano query nell'**Editor di query**.

## <a name="in-this-video---introduction-to-dax"></a>Contenuto del video: introduzione a DAX
I concetti di DAX sono semplici e diretti, ma DAX un linguaggio molto potente. DAX usa alcuni concetti e modelli di programmazione esclusivi, che possono renderlo difficile da usare e comprendere completamente. Poiché le tradizionali modalità di apprendimento dei linguaggi potrebbero non essere il miglior approccio a DAX, l'obiettivo di questo video è indicare i concetti e la teoria che in seguito semplificheranno l'uso di Power BI.

DAX è un *linguaggio funzionale*, ovvero tutto il codice eseguito è contenuto all'interno di una funzione.

In DAX le funzioni possono contenere altri elementi annidati, come funzioni, istruzioni condizionali e riferimenti a valori. L'esecuzione in DAX inizia dalla funzione o parametro più interno e procede verso l'esterno. Poiché in Power BI le formule DAX sono scritte su una singola riga, la corretta formattazione delle funzioni è un aspetto importante ai fini della leggibilità.

DAX è progettato per essere usato con tabelle e di conseguenza ha solo due tipi di dati principali, **numerici** e **di altro tipo**. Il tipo **numerico** può includere *interi*, *decimali* e *valute*. Tra gli **altri tipi di dati** sono inclusi *stringhe* e *oggetti binari*. Di conseguenza, se la funzione DAX viene creata per supportare un tipo di numero, funzionerà anche con qualsiasi altro tipo di dati numerici.

DAX usa l'overload degli operatori, ovvero è possibile combinare tipi di dati nei calcoli perché i risultati cambino in base al tipo usato negli input. La conversione viene eseguita automaticamente. Questo significa che non è necessario identificare i tipi di dati delle colonne usate in Power BI, ma anche che a volte la conversione può avvenire in modi imprevisti. È consigliabile saper identificare i dati usati per garantire che gli operatori si comportino nel modo previsto.

Un tipo di dati in particolare è probabile che verrà usato molto in Power BI, ovvero **Data/Ora**. Il tipo di dati **Data/Ora** è archiviato come valore a virgola mobile con una parte intera e una decimale. Il tipo di dati Data/Ora può essere usato in modo accurato per calcoli di qualsiasi periodo di tempo successivo al 1° marzo 1900.

> Contenuto video fornito da [Alberto Ferrari, SQLBI](http://www.sqlbi.com/learning-dax/?utm_source=powerbi&utm_medium=marketing&utm_campaign=after-summit)
> 
> 

