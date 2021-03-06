---
title: Usare SAP HANA in Power BI Desktop
description: Usare SAP HANA in Power BI Desktop
author: davidiseminger
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-desktop
ms.topic: conceptual
ms.date: 07/27/2018
ms.author: davidi
LocalizationGroup: Connect to data
ms.openlocfilehash: c2a2069eb5f4d056db5840a08ecb1a871bf587c8
ms.sourcegitcommit: f01a88e583889bd77b712f11da4a379c88a22b76
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 07/27/2018
ms.locfileid: "39329869"
---
# <a name="use-sap-hana-in-power-bi-desktop"></a>Usare SAP HANA in Power BI Desktop
Con Power BI Desktop è ora possibile accedere ai database **SAP HANA** . Per usare **SAP HANA**, il driver ODBC di SAP HANA deve essere installato nel computer client locale in modo che la connessione dati **SAP HANA** di Power BI Desktop funzioni correttamente. È possibile scaricare il driver ODBC di SAP HANA da [SAP Software Download Center](https://support.sap.com/swdc). Da qui, cercare il CLIENT SAP HANA per i computer Windows. Dal momento che **SAP Software Download Center** cambia struttura di frequente, non sono disponibili indicazioni più specifiche per la navigazione.

Per connettersi a un database **SAP HANA**, selezionare **Recupera dati > Database > Database SAP HANA** come illustrato nella figura seguente:

![](media/desktop-sap-hana/sap-hana-1.png)

Quando ci si connette a un database SAP HANA, specificare il nome del server e la porta nel formato *server:porta*. L'immagine seguente mostra un esempio con un server denominato *ServerXYZ* e la porta *30015*.

![](media/desktop-sap-hana/sap-hana-2.png)

In questa versione, **SAP HANA** in modalità [DirectQuery](desktop-directquery-sap-hana.md) è supportato in Power BI Desktop e nel servizio Power BI ed è possibile pubblicare e caricare report che usano **SAP HANA** in modalità DirectQuery nel servizio Power BI. È anche possibile pubblicare e caricare i report nel servizio Power BI se non si usa **SAP HANA** nella modalità DirectQuery.

### <a name="supported-features-for-sap-hana"></a>Funzionalità supportate per SAP HANA
Questa versione presenta molte funzionalità per **SAP HANA**, come illustrato nell'elenco seguente:

* Il connettore di Power BI per **SAP HANA** usa il driver ODBC di SAP per offrire la migliore esperienza di utilizzo
* **SAP HANA** supporta le opzioni di DirectQuery e Import
* Power BI supporta i modelli informativi HANA (quali le viste analitiche e di calcolo) e dispone di navigazione ottimizzata
* Con **SAP HANA** è possibile usare anche la funzionalità SQL diretta per la connessione alle tabelle Riga e Colonna
* Esso include la struttura ottimizzata per i modelli HANA
* Power BI supporta le variabili e i parametri di input di **SAP HANA**

### <a name="installing-the-sap-hana-odbc-driver"></a>Installazione del driver ODBC di SAP HANA
### <a name="limitations-of-sap-hana"></a>Limitazioni di SAP HANA
Esistono inoltre alcune limitazioni all'uso di **SAP HANA**, come illustrato di seguito:

* Le stringhe NVARCHAR vengono troncate alla lunghezza massima di 4000 caratteri Unicode
* SMALLDECIMAL non è supportato
* VARBINARY non è supportato
* Le date valide sono comprese tra 30/12/1899 e 31/12/9999


## <a name="next-steps"></a>Passaggi successivi
Per altre informazioni su DirectQuery, vedere le risorse seguenti:

* [DirectQuery and SAP HANA](desktop-directquery-sap-hana.md) (DirectQuery e SAP HANA)
* [DirectQuery in Power BI](desktop-directquery-about.md)
* [Data sources supported by DirectQuery](desktop-directquery-data-sources.md) (Origini dati supportate da DirectQuery)

