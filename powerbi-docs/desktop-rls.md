---
title: Informazioni sulla sicurezza a livello di riga con Power BI Desktop
description: Come configurare la sicurezza a livello di riga per i set di dati importati e DirectQuery con Power BI Desktop.
author: markingmyname
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-desktop
ms.topic: conceptual
ms.date: 05/03/2018
ms.author: maghan
LocalizationGroup: Create reports
ms.openlocfilehash: 022668737f6bcce987b2923ba7a4416f4a08460a
ms.sourcegitcommit: 001ea0ef95fdd4382602bfdae74c686de7dc3bd8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 07/11/2018
ms.locfileid: "38875989"
---
# <a name="row-level-security-rls-with-power-bi-desktop"></a>Sicurezza a livello di riga con Power BI Desktop
La sicurezza a livello di riga con Power BI Desktop consente di limitare l'accesso ai dati per determinati utenti. I filtri limitano l'accesso ai dati a livello di riga. È possibile definire i filtri nei ruoli.

È ora possibile configurare la sicurezza a livello di riga per i modelli di dati importati in Power BI con Power BI Desktop. È anche possibile configurare la sicurezza a livello di riga nei set di dati che usano DirectQuery, ad esempio SQL Server. In precedenza, era possibile implementare la sicurezza a livello di riga solo nei modelli di Analysis Services all'esterno di Power BI. Per le connessioni dinamiche ad Analysis Services è possibile configurare la sicurezza a livello di riga nel modello locale. L'opzione di sicurezza non viene visualizzata per i set di dati di connessione dinamica.

> [!IMPORTANT]
> Se sono stati definiti ruoli e regole all'interno del servizio Power BI, sarà necessario creare di nuovo tali ruoli all'interno di Power BI Desktop e pubblicare il report nel servizio.
> 
> 

Altre informazioni sulle opzioni per la [sicurezza a livello di riga all'interno del servizio Power BI](service-admin-rls.md).

[!INCLUDE [include-short-name](./includes/rls-desktop-define-roles.md)]

[!INCLUDE [include-short-name](./includes/rls-desktop-view-as-roles.md)]

[!INCLUDE [include-short-name](./includes/rls-limitations.md)]

[!INCLUDE [include-short-name](./includes/rls-faq.md)]

## <a name="next-steps"></a>Passaggi successivi
[Sicurezza a livello di riga con il servizio Power BI](service-admin-rls.md)  

Altre domande? [Provare a rivolgersi alla community di Power BI](http://community.powerbi.com/)

