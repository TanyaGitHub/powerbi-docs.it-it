---
title: Che cos'è Microsoft Power BI Premium?
description: Power BI Premium offre una capacità dedicata all'organizzazione o al team, con prestazioni più affidabili e volumi di dati superiori, senza richiedere l'acquisto di licenze per ogni utente.
author: mgblythe
ms.author: mblythe
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-admin
ms.topic: conceptual
ms.date: 10/21/2018
LocalizationGroup: Premium
ms.openlocfilehash: 2ca75f191f27bd158b9fab67c7be6902154f8ac1
ms.sourcegitcommit: a764e4b9d06b50d9b6173d0fbb7555e3babe6351
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/22/2018
ms.locfileid: "49641230"
---
# <a name="what-is-microsoft-power-bi-premium"></a>Che cos'è Microsoft Power BI Premium?

Microsoft Power BI Premium offre risorse dedicate per l'esecuzione del servizio Power BI nell'organizzazione, garantendo prestazioni più affidabili e con il supporto di volumi di dati superiori. Premium consente anche la distribuzione generalizzata dei contenuti senza dover acquistare licenze Pro per utente singolo per i consumer del contenuto. Per informazioni sull'acquisto, vedere [Come acquistare Power BI Premium](service-admin-premium-purchase.md).

<iframe width="560" height="315" src="https://www.youtube.com/embed/lNQDkN0GXzU?rel=0&amp;showinfo=0" frameborder="0" allowfullscreen></iframe>

## <a name="premium-capacity-and-shared-capacity"></a>Capacità Premium e capacità condivisa

È possibile sfruttare Power BI Premium assegnando alle aree di lavoro una *capacità Premium*. La capacità Premium è una risorsa dedicata per l'organizzazione. Le aree di lavoro a cui non viene assegnata una capacità Premium hanno una *capacità condivisa*. Con la capacità condivisa i carichi di lavoro vengono eseguiti in risorse di calcolo condivise da altri clienti.

L'immagine seguente visualizza la relazione tra capacità Premium e capacità condivisa, con l'organizzazione Contoso come esempio.

![Illustrazione di Power BI Premium](media/service-premium/premium-chart.png)

| Area | Descrizione |
| --- | --- |
| **(1)** Elementi all'interno di una capacità Premium | <ul><li>L'accesso alle aree di lavoro delle app, come membri o amministratori, e la pubblicazione di app richiedono una licenza di Power BI Pro.<li>Per condividere un'app è necessaria una licenza Pro, per usarla invece non occorre.<li>Tutti i destinatari del dashboard, indipendentemente dalla licenza loro assegnata, possono impostare gli avvisi dati.<li>Le API REST per l'incorporamento usano un account del servizio con una licenza Pro, invece di un account utente.</ul> |
| **(2)** Area di lavoro personale nella capacità condivisa | <ul><li>Sia per condividere che per usare un'app è necessaria una licenza Pro.</ul> |
| **(3)** Aree di lavoro delle app nella capacità condivisa | <ul><li>L'uso di qualsiasi app richiede una licenza Pro.</ul>|
| | |

Nella capacità condivisa, Power BI pone più limiti sui singoli utenti in modo da garantire la qualità dell'esperienza per tutti gli utenti. Per impostazione predefinita, l'area di lavoro ha una capacità condivisa, incluse l'*Area di lavoro personale* e le Aree di lavoro per le app.

La tabella seguente offre un riepilogo delle differenze tra la capacità condivisa e la capacità Premium.

|  | Capacità condivisa | Capacità Power BI Premium |
| --- | --- | --- |
| **Frequenza di aggiornamento** |8/giorno |48/giorno |
| **Isolamento con hardware dedicato** |![](media/service-premium/not-available.png "Non disponibile") |![](media/service-premium/available.png "Disponibile") |
| **Distribuzione aziendale per** ***tutti gli utenti*** | | |
| App e condivisione |![](media/service-premium/not-available.png "Non disponibile") |![](media/service-premium/available.png "Disponibile")<sup>1</sup> |
| API e controlli incorporati |![](media/service-premium/not-available.png "Non disponibile") |![](media/service-premium/available.png "Disponibile")<sup>2</sup> |
| **Pubblicazione dei report di Power BI locali** |![](media/service-premium/not-available.png "Non disponibile") |![](media/service-premium/available.png "Disponibile") |
| | | |

*<sup>1</sup> Per altre informazioni, vedere [Funzionalità in base al tipo di licenza](service-features-license-type.md).*  
*<sup>2</sup> Miglioramenti in arrivo per Power BI Premium.*

Per altre informazioni sull'assegnazione delle aree di lavoro alla capacità Premium, vedere [Gestire Power BI Premium](service-admin-premium-manage.md).

<a name="premiumskus"/>

### <a name="premium-capacity-nodes"></a>Nodi della capacità Premium

Power BI Premium è disponibile nelle configurazioni del nodo con diverse capacità v-core. Per altre informazioni sulle offerte e i prezzi delle SKU specifiche, vedere [Prezzi di Power BI](https://powerbi.microsoft.com/pricing/). È disponibile un [calcolatore dei costi](https://powerbi.microsoft.com/calculator/). Per informazioni sulla pianificazione della capacità analitica incorporata, vedere [Planning a Power BI Enterprise Deployment whitepaper](https://aka.ms/pbienterprisedeploy) (White paper sulla pianificazione della distribuzione aziendali di Power BI) Per riassumere:

* I nodi P possono essere usati per le distribuzioni di servizi o incorporate.

* I nodi EM possono essere usati solo per le distribuzioni incorporate. I nodi EM non hanno accesso alle funzionalità Premium, ad esempio la condivisione di app per gli utenti che non hanno una licenza di Power BI Pro.

>[!NOTE]
>I collegamenti disponibili in questa tabella funzionano correttamente per gli utenti che hanno il ruolo di amministratore globale di Office 365. Gli altri utenti ricevono un errore di tipo 404.

| Nodo della capacità | Totale vCore<br/>*(Back-end + front-end)* | vCore back-end | vCore front-end | Limiti di connessione dinamica/DirectQuery | Rendering massimo della pagina all'ora di punta | Disponibilità |
| --- | --- | --- | --- | --- | --- | --- |
| [EM1 (mensile)](https://portal.office.com/SubscriptionDetails?OfferId=4004702D-749C-4F74-BF47-3048F1833780&adminportal=1) |1 vCore |0,5 v-core, 2.5 GB di RAM |0,5 v-core |3,75 al secondo |150-300 |Disponibile |
| [EM2 (mensile)](https://portal.office.com/SubscriptionDetails?OfferId=4004702D-749C-4F74-BF47-3048F1833780&adminportal=1) |2 v-core |1 v-core, 5 GB di RAM |1 vCore |7,5 al secondo |301-600 |Disponibile |
| [EM3 (mensile)](https://portal.office.com/SubscriptionDetails?OfferId=4004702D-749C-4F74-BF47-3048F1833780&adminportal=1) |4 v-core |2 v-core, 10 GB di RAM |2 v-core | |601-1.200 |Disponibile |
| [P1](https://portal.office.com/SubscriptionDetails?OfferId=b3ec5615-cc11-48de-967d-8d79f7cb0af1&adminportal=1) |8 v-core |4 v-core, 25 GB di RAM |4 v-core |30 al secondo |1.201-2.400 |Disponibile (è disponibile anche l'opzione [mensile](https://portal.office.com/SubscriptionDetails?OfferId=E4C8EDD3-74A1-4D42-A738-C647972FBE81&adminportal=1)) |
| [P2](https://portal.office.com/SubscriptionDetails?OfferId=062F2AA7-B4BC-4B0E-980F-2072102D8605&adminportal=1) |16 v-core |8 v-core, 50 GB di RAM |8 v-core |60 al secondo |2.401-4.800 |Disponibile |
| [P3](https://portal.office.com/SubscriptionDetails?OfferId=40c7d673-375c-42a1-84ca-f993a524fed0&adminportal=1) |32 v-core |16 v-core, 100 GB di RAM |16 v-core |120 al secondo |4.801-9600 |Disponibile |
| | | | | | | |

* I vCore di front-end sono responsabili della gestione dei documenti relativi a servizio Web, dashboard e report, della gestione dei diritti di accesso, della pianificazione, delle API, dei caricamenti e dei download e in genere di tutto ciò che riguarda l'esperienza utente.

* I vCore di back-end sono responsabili del lavoro più oneroso: elaborazione delle query, gestione della cache, esecuzione dei server R, aggiornamento dei dati, elaborazione del linguaggio naturale, feed in tempo reale e rendering lato server di report e immagini. Con i vCore di back-end viene riservata anche una certa quantità di memoria. Le disponibilità di uno spazio in memoria sufficiente è particolarmente importante quando si usano modelli di dati di grandi dimensioni o un numero elevato di set di dati attivi.

## <a name="power-bi-report-server"></a>Server di report Power BI

Power BI Premium include anche la capacità di eseguire il Server di report di Power BI in locale nell'organizzazione. Per altre informazioni, vedere [Introduzione a Server di report di Power BI](report-server/get-started.md).

## <a name="next-steps"></a>Passaggi successivi

[Domande frequenti su Power BI Premium](service-premium-faq.md)
[Come acquistare Power BI Premium](service-admin-premium-purchase.md)
[Gestione di Power BI Premium](service-admin-premium-manage.md)
[White paper: Microsoft Power BI Premium](https://aka.ms/pbipremiumwhitepaper)
[White paper: Pianificazione di una distribuzione Power BI Enterprise](https://aka.ms/pbienterprisedeploy)
[Amministrazione di Power BI nell'organizzazione](service-admin-administering-power-bi-in-your-organization.md)

Altre domande? [Provare a rivolgersi alla community di Power BI](https://community.powerbi.com/)
