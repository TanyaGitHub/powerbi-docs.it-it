---
title: Visualizzare un report nel servizio Power BI
description: Aprire un report di Power BI nella visualizzazione di lettura.
author: mihart
manager: kvivek
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-service
ms.topic: conceptual
ms.date: 10/10/2018
ms.author: mihart
ms.openlocfilehash: 4d37c1389628078466d8fedb290d928c3f02e7d5
ms.sourcegitcommit: dc8b8a2cf2dcc96ccb46159802ebd9342a7fa840
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/11/2018
ms.locfileid: "49112016"
---
# <a name="view-a-report-in-power-bi-service-apppowerbicom"></a>Visualizzare un report nel servizio Power BI (app.powerbi.com)
Un report è costituito da una o più pagine di oggetti visivi. I report vengono creati dai *progettisti* di Power BI e [condivisi con i consumer direttamente](end-user-shared-with-me.md) o nel contesto di un'[app](end-user-apps.md). 

Esistono diversi modi per aprire un report e ne verranno illustrati due: apertura dalla home page e apertura da un dashboard. 

<!-- add art-->


## <a name="open-a-report-from-your-home-page"></a>Aprire un report dalla home page
Di seguito viene descritta la procedura per aprire un report che è stato condiviso con l'utente direttamente e quindi per aprire un report che è stato condiviso come parte di un'app.

   ![Home page](./media/end-user-report-open/power-bi-home.png)

### <a name="open-a-report-that-has-been-shared-with-you"></a>Aprire un report condiviso con l'utente
I *progettisti* di Power BI possono condividere un report direttamente con un utente facendo clic su un pulsante **Condividi** nella barra dei menu principale. Il contenuto condiviso in questo modo viene visualizzato nel contenitore **Condivisi con l'utente corrente** nella barra di spostamento a sinistra e nella sezione **Condivisi con l'utente corrente** della home page dell'utente destinatario.

1. Aprire il servizio Power BI (app.powerbi.com).

2. Dalla barra di spostamento a sinistra selezionare **Home page (anteprima)** per aprire la home page.  

   ![Home page](./media/end-user-report-open/power-bi-select-home.png)
   
3. Scorrere verso il basso fino a visualizzare **Condivisi con l'utente corrente**. Cercare l'icona del report ![icona del report](./media/end-user-report-open/power-bi-report-icon.png). In questo screenshot sono disponibili due report: *Financial* e *Northwind*. 
   
   ![Sezione Condivisi con l'utente corrente della home page](./media/end-user-report-open/power-bi-shared.png)

4. È sufficiente selezionare una delle schede di report per aprire il report.

   ![Pagina del report](./media/end-user-report-open/power-bi-report1.png)

5. Si notino le schede nella parte inferiore. Ogni scheda rappresenta una *pagina* del report. Attualmente, è aperta la pagina *IT Spend Trend*. Selezionare una scheda diversa per aprire la pagina del report. 

   ![Schede delle pagine del report](./media/end-user-report-open/power-bi-tabs.png)

6. Al momento è possibile vedere solo una parte della pagina del report. Per modificare la visualizzazione (zoom) della pagina, selezionare **Visualizza** > **Adatta alla pagina**.

   ![Modificare lo zoom](./media/end-user-report-open/power-bi-fit.png)

   ![Adatta alla pagina](./media/end-user-report-open/power-bi-report2.png)

### <a name="open-a-report-that-is-part-of-an-app"></a>Aprire un report che fa parte di un'app
Se si ricevono app da colleghi o da AppSource, tali app sono disponibili dalla home page e dal contenitore **App** nella barra di spostamento a sinistra. Un'[app](end-user-apps.md) è un'aggregazione di dashboard e report.

1. Tornare alla home page selezionando **Home page (anteprima)** dalla barra di spostamento a sinistra.

7. Scorrere verso il basso fino a visualizzare **App personali**.

   ![Home page](./media/end-user-report-open/power-bi-my-apps.png)

8. Selezionare una delle app per aprirla. A seconda delle opzioni impostate dal *progettista* dell'app, l'app aprirà un dashboard o un report. Se quando si seleziona l'app:
    - Viene aperto il report, è tutto pronto.
    - Viene aperto un dashboard, vedere [Aprire un report da un dashboard](#Open-a-report-from-a-dashboard) di seguito.



## <a name="open-a-report-from-a-dashboard"></a>Aprire un report da un dashboard
I report possono essere aperti da un dashboard. La maggior parte dei riquadri del dashboard viene *aggiunta* dai report. Se si seleziona un riquadro, viene aperto il report usato per creare il riquadro stesso. 

1. In un dashboard selezionare un riquadro. In questo esempio è stato selezionato il riquadro dell'istogramma "Total Units YTD".

    ![Dashboard con riquadro selezionato](./media/end-user-report-open/power-bi-dashboard.png)

2.  Viene aperto il report associato. Si noti che viene ora visualizzata la pagina "YTD Category". Si tratta della pagina del report che contiene l'istogramma selezionato dal dashboard.

    ![Report aperto nella Visualizzazione di lettura](./media/end-user-report-open/power-bi-report-new.png)

> [!NOTE]
> Non tutti i riquadri portano a un report. Se si seleziona un riquadro [creato con Domande e risposte](../service-dashboard-pin-tile-from-q-and-a.md), verrà visualizzata la schermata Domande e risposte. Se si seleziona un riquadro [creato tramite il widget **Aggiungi riquadro** del dashboard](../service-dashboard-add-widget.md), verrà aperta la procedura guidata **Edit tile** (Modifica riquadro).  


##  <a name="still-more-ways-to-open-a-report"></a>Altri modi per aprire un report
Quando si acquisisce maggiore esperienza nello spostamento in un servizio Power BI, sarà possibile individuare i flussi di lavoro ottimali per le proprie esigenze. Altri modi per accedere ai report:
- Dal riquadro di spostamento a sinistra usando **Preferiti** e **Recenti**    
- Tramite [Visualizza elementi correlati](end-user-related.md).    
- In un messaggio di posta elettronica in caso di [condivisione con l'utente](../service-share-reports.md) o quando si [configura un avviso](../service-set-data-alerts.md)    
- Dal [Centro notifiche] (end-user-notification-center.md)    
- E altro ancora.

## <a name="next-steps"></a>Passaggi successivi
Esistono [moltissimi modi per interagire con un report](end-user-reading-view.md).  Iniziare l'esplorazione selezionando ogni scheda nella parte inferiore dell'area di disegno report.

