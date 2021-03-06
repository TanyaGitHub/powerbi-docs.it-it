---
title: Origini dati supportate da DirectQuery in Power BI
description: Ottenere un elenco di origini dati che possono essere usati da DirectQuery.
author: davidiseminger
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-desktop
ms.topic: conceptual
ms.date: 08/10/2018
ms.author: davidi
LocalizationGroup: Connect to data
ms.openlocfilehash: d37ed22c0abba4e843d37fd6df465f9a755fbdc6
ms.sourcegitcommit: 126e5eca8bfab6273581dabd7603df88be755240
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2018
ms.locfileid: "40257084"
---
# <a name="data-sources-supported-by-directquery-in-power-bi"></a>Origini dati supportate da DirectQuery in Power BI
**Power BI Desktop** e il **servizio Power BI** dispongono di diverse origini dati a cui è possibile connettersi per accedere ai dati. Questo articolo descrive le origini dati per Power BI che supportano il metodo di connessione noto come **DirectQuery**. Per altre informazioni su DirectQuery, vedere [**DirectQuery in Power BI**](desktop-directquery-about.md).

Le origini dati seguenti supportano DirectQuery in Power BI:

* Amazon Redshift
* Azure Databricks
* Spark in Azure HDInsight (Beta)
* Database SQL di Azure
* Azure SQL Data Warehouse
* Google BigQuery (Beta)
* IBM Netezza (Beta)
* Impala (versione 2.x)
* Database di Oracle (versione 12 e successive)
* Server applicazioni SAP Business Warehouse
* Server messaggi SAP Business Warehouse (Beta)
* SAP HANA
* Snowflake
* Spark (Beta) (versione 0.9 e successive)
* SQL Server
* Database Teradata
* Vertica (Beta)

Le origini dati il cui nome è seguito da **(Beta)** o **(Anteprima)** sono soggette a modifiche e non sono supportate per l'uso in produzione. Possono anche non essere supportate dopo la pubblicazione di un report per il **servizio Power BI**, il che significa che l'apertura di un report pubblicato o l'esplorazione del set di dati può comportare un errore.

L'unica differenza tra le origini dati **(Beta)** e **(Anteprima)** è che le origini **(anteprima)** devono essere abilitate come funzionalità di anteprima prima di poter essere usate. Per abilitare un connettore dati **(Anteprima)**, in **Power BI Desktop**, passare a **File > Opzioni e impostazioni** e quindi selezionare **Funzionalità di anteprima**.

> [!NOTE]
> Le query DirectQuery per SQL Server richiedono l'autenticazione tramite credenziali di autenticazione di Windows o credenziali del database valide per stabilire l'accesso. Le credenziali alternative non sono supportate.
>

## <a name="on-premises-gateway-requirements"></a>Requisiti del gateway locale
La tabella seguente specifica se è necessario un **gateway dati locale** per connettersi all'origine dati specificata, dopo la pubblicazione di un report nel **servizio Power BI**.

| Origine | Gateway necessario? |
| --- | --- |
| SQL Server |Sì |
| Database SQL di Azure |No |
| Azure SQL Data Warehouse |No |
| SAP HANA |Sì |
| Database Oracle |Sì |
| Database Teradata |Sì |
| Amazon Redshift |No |
| Impala (versione 2.x) |Sì |
| Snowflake |Sì |
| Spark (Beta), versione 0.9 e successive |Non è ancora supportato nel **servizio Power BI** |
| Spark in Azure HDInsight (Beta) |No |
| IBM Netezza |Sì |
| Server applicazioni SAP Business Warehouse |Sì |
| Server messaggi SAP Business Warehouse |Non è ancora supportato nel **servizio Power BI** |
| Google BigQuery |No |


## <a name="next-steps"></a>Passaggi successivi
Per altre informazioni su DirectQuery, vedere le risorse seguenti:

* [DirectQuery in Power BI](desktop-directquery-about.md)
* [DirectQuery and SAP HANA](desktop-directquery-sap-hana.md) (DirectQuery e SAP HANA)
* [DirectQuery e SAP BW](desktop-directquery-sap-bw.md)
* [Gateway dati locale](service-gateway-onprem.md)

