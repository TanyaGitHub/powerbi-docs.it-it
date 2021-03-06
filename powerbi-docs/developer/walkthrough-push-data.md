---
title: Eseguire il push dei dati in un set di dati
description: Eseguire il push dei dati in un set di dati di Power BI
author: markingmyname
ms.author: maghan
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-developer
ms.topic: conceptual
ms.date: 01/05/2017
ms.openlocfilehash: 01bcc545d3ba8edb23ef583467322401780e657d
ms.sourcegitcommit: 698b788720282b67d3e22ae5de572b54056f1b6c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/17/2018
ms.locfileid: "45974185"
---
# <a name="push-data-into-a-power-bi-dataset"></a>Eseguire il push dei dati in un set di dati di Power BI

Con l'API Power BI è possibile eseguire il push dei dati in un set di dati di Power BI. Si supponga ad esempio di voler estendere un flusso di lavoro aziendale esistente per eseguire il push dei dati chiave in un set di dati. In questo caso, è possibile eseguire il push di un set di dati Sales Marketing che contiene una tabella Product in un set di dati.

Prima di iniziare il push dei dati in un set di dati, è necessario avere Azure Active Directory (Azure AD) e un [account Power BI](create-an-azure-active-directory-tenant.md).

## <a name="steps-to-push-data-into-a-dataset"></a>Procedura per eseguire il push dei dati in un set di dati

* Passaggio 1: [Registrare un'app in Azure AD](walkthrough-push-data-register-app-with-azure-ad.md)
* Passaggio 2: [Ottenere un token di accesso per l'autenticazione](walkthrough-push-data-get-token.md)
* Passaggio 3: [Creare un set di dati in Power BI](walkthrough-push-data-create-dataset.md)
* Passaggio 4: [Ottenere un set di dati per aggiungere righe in una tabella di Power BI](walkthrough-push-data-get-datasets.md)
* Passaggio 5: [Aggiungere righe a una tabella di Power BI](walkthrough-push-data-add-rows.md)

La sezione successiva fornisce una descrizione generale delle operazioni dell'API di Power BI che seguono il push dei dati.

## <a name="power-bi-api-operations-to-push-data"></a>Operazioni dell'API di Power BI per eseguire il push dei dati

Con l'API REST di Power BI è possibile eseguire il push di origini dati in Power BI. Quando un'app aggiunge righe a un set di dati, i riquadri del dashboard vengono aggiornati automaticamente con i dati aggiornati. Per eseguire il push dei dati, usare l'operazione [PostDataset](https://docs.microsoft.com/rest/api/power-bi/pushdatasets) con l'operazione [PostRows](https://docs.microsoft.com/rest/api/power-bi/pushdatasets/datasets_postrows). Per trovare un set di dati, usare l'operazione [Get Datasets](https://docs.microsoft.com/rest/api/power-bi/datasets/getdatasets). Per ognuna di queste operazioni, è possibile passare un ID di gruppo per lavorare con un gruppo. Usare l'operazione [Get Groups](https://docs.microsoft.com/rest/api/power-bi/groups/getgroups) per ottenere un elenco di ID del gruppo.

Ecco le operazioni per eseguire il push dei dati in un set di dati:

* [PostDataset](https://docs.microsoft.com/rest/api/power-bi/pushdatasets/datasets_postdataset)
* [Recupera set di dati](https://docs.microsoft.com/rest/api/power-bi/datasets/getdatasets)
* [PostRows](https://docs.microsoft.com/rest/api/power-bi/pushdatasets/datasets_postrows)
* [Recupera gruppi](https://docs.microsoft.com/rest/api/power-bi/groups/getgroups)

Viene creato un set di dati in Power BI passando una stringa JSON (JavaScript Object Notation) al servizio Power BI. Per altre informazioni su JSON, vedere l'[introduzione a JSON](http://json.org/).

La stringa JSON per un set di dati ha il formato seguente:

**Oggetto JSON del set di dati di Power BI**

    {"name": "dataset_name", "tables":
        [{"name": "", "columns":
            [{ "name": "column_name1", "dataType": "data_type"},
             { "name": "column_name2", "dataType": "data_type"},
             { ... }
            ]
          }
        ]
    }

Pertanto, per il set di dati Sales Marketing di esempio, si passerà una stringa JSON come nell'esempio seguente. In questo esempio, **SalesMarketing** è il nome del set e **Product** è il nome della tabella. Dopo aver definito la tabella, si definisce lo schema di tabella. Per il set di dati **SalesMarketing** , lo schema di tabella contiene le colonne ProductID, Manufacturer, Category, Segment, Product e IsCompete.

**Esempio JSON per l'oggetto set di dati**

    {
        "name": "SalesMarketing",
        "tables": [
            {
                "name": "Product",
                "columns": [
                {
                    "name": "ProductID",
                    "dataType": "int"
                },
                {
                    "name": "Manufacturer",
                    "dataType": "string"
                },
                {
                    "name": "Category",
                    "dataType": "string"
                },
                {
                    "name": "Segment",
                    "dataType": "string"
                },
                {
                    "name": "Product",
                    "dataType": "string"
                },
                {
                    "name": "IsCompete",
                    "dataType": "bool"
                }
                ]
            }
        ]
    }

Per uno schema di tabella di Power BI, è possibile usare i tipi di dati seguenti.

## <a name="power-bi-table-data-types"></a>Tipi di dati per una tabella di Power BI

| **Tipo di dati** | **Restrizioni** |
| --- | --- |
| Int64 |Int64.MaxValue e Int64.MinValue non sono consentiti. |
| Double |Double.MaxValue e Double.MinValue non sono consentiti. NaN non supportato. +Infinity e -Infinity non supportati in alcune funzioni, ad esempio Min, Max. |
| Booleano |Nessuno |
| DateTime |Durante il caricamento dei dati, i valori vengono quantizzati con frazioni giornaliere fino a multipli interi di 1/300 secondi (3,33 ms). |
| String |Sono attualmente consentiti al massimo 128.000 caratteri. |

## <a name="learn-more-about-pushing-data-into-power-bi"></a>Altre informazioni sul push dei dati in Power BI

Per le attività iniziali per il push dei dati in un set di dati, vedere [Passaggio 1: Registrare un'app in Azure AD](walkthrough-push-data-register-app-with-azure-ad.md) nel riquadro di spostamento a sinistra.

[Passaggio successivo >](walkthrough-push-data-register-app-with-azure-ad.md)

## <a name="next-steps"></a>Passaggi successivi

[Iscriversi a Power BI](create-an-azure-active-directory-tenant.md)  
[Introduzione a JSON](http://json.org/)  
[Panoramica dell'API REST di Power BI](overview-of-power-bi-rest-api.md)  
Altre domande? [Provare la community di Power BI](http://community.powerbi.com/)