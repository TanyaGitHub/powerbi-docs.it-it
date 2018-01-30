---
title: Installare Power BI Desktop ottimizzato per il server di report di Power BI
description: Informazioni su come installare Power BI Desktop ottimizzato per il server di report di Power BI
services: powerbi
documentationcenter: 
author: maggiesMSFT
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
ms.date: 12/15/2017
ms.author: maggies
ms.openlocfilehash: c1c38d9d98c92963534081049cdcc6a557313639
ms.sourcegitcommit: ea247cb3cfc1cac076d4b076c1ad8e2fc37e15a1
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/19/2017
---
# <a name="install-power-bi-desktop-optimized-for-power-bi-report-server"></a>Installare Power BI Desktop ottimizzato per il server di report di Power BI
Informazioni su come installare Power BI Desktop ottimizzato per il server di report di Power BI.

Per creare report di Power BI per il server di report di Power BI, è necessario installare Power BI Desktop ottimizzato per il server di report di Power BI. Si tratta di una versione diversa dalla versione di Power BI Desktop usata con il servizio Power BI, Ad esempio, la versione di Power BI Desktop per il servizio Power BI include funzionalità in anteprima disponibili nella versione del server di report di Power BI solo dopo il rilascio. necessaria per assicurarsi che il server di report possa interagire con una versione nota dei report e del modello. 

> [!NOTE]
> Power BI Desktop e Power BI Desktop ottimizzato per il server di report di Power BI possono essere installati side-by-side.

## <a name="download-and-install-power-bi-desktop"></a>Scaricare e installare Power BI Desktop

Il modo più facile per assicurarsi di aver installato la versione più aggiornata di Power BI Desktop ottimizzato per il server di report di Power BI è iniziare dal portale Web del server di report.

1. Nel portale Web del server di report selezionare la freccia **Scarica** > **Power BI Desktop**.

    ![Scaricare Power BI Desktop dal portale Web](media/install-powerbi-desktop/report-server-download-web-portal.png)

    In alternativa è possibile passare direttamente a [Microsoft Power BI Desktop](https://go.microsoft.com/fwlink/?linkid=861076) (ottimizzato per il server di report di Power BI - ottobre 2017) nell'Area download Microsoft.

2. Nella pagina dell'Area download selezionare **Scarica**.

3. In base al computer specifico, selezionare: 

    - **PBIDesktopRS.msi** (versione a 32 bit) oppure

    - **PBIDesktopRS_x64.msi** (versione a 64 bit).

1. Dopo il download del programma di installazione, eseguire l'installazione guidata di Power BI Desktop (ottobre 2017).
2. Al termine dell'installazione, selezionare **Avvia Power BI Desktop**.
   
    Verrà avviato automaticamente e si è pronti per iniziare.

## <a name="verify-you-are-using-the-correct-version"></a>Verificare di usare la versione corretta
È possibile verificare che si sta usando la versione corretta di Power BI Desktop esaminando la schermata di avvio o la barra del titolo all'interno di Power BI Desktop. La barra del titolo indicherà il mese e l'anno di rilascio della versione.

![Barra del titolo per Power BI Desktop ottimizzato per il server di report di Power BI](media/quickstart-create-powerbi-report/report-server-desktop-october-2017-version.png)

La versione di Power BI Desktop per il servizio Power BI non avrà il mese e l'anno nella barra del titolo.

## <a name="file-extension-association"></a>Associazione dell'estensione di file
Se sono stati installati sia Power BI Desktop sia Power BI Desktop ottimizzato per il server di report di Power BI nello stesso computer, l'ultima installazione di Power BI desktop avrà l'associazione file con l'estensione pbix. Ciò significa che quando si fa doppio clic su un file PBIX, verrà avviata la versione di Power BI Desktop installata per ultima.

Se è stata eseguita l'installazione di Power BI Desktop ottimizzato per il server di report di Power BI in un computer che conteneva già Power BI Desktop, per impostazione predefinita tutti i file PBIX verranno aperti in Power BI Desktop ottimizzato per il server di report di Power BI. Se invece si preferisce avviare per impostazione predefinita Power BI Desktop all'apertura di un file PBIX, reinstallarlo dal servizio Power BI.

È sempre possibile aprire la versione di Power BI Desktop che si vuole usare per prima, quindi aprire il file da Power BI Desktop.

Se si modifica un report di Power BI da un server di report di Power BI o si crea un nuovo report di Power BI dal portale Web, verrà sempre aperta la versione corretta di Power BI Desktop.

## <a name="considerations-and-limitations"></a>Considerazioni e limitazioni
I report nel server di report di Power BI e nel servizio Power BI (http://powerbi.com) operano quasi esattamente allo stesso modo, ma alcune funzionalità sono diverse.

### <a name="in-a-browser"></a>In un browser
I report del server di report di Power BI supportano tutte le visualizzazioni, tra cui:

* Oggetti visivi personalizzati

I report del server di report di Power BI non supportano:

* Oggetti visivi R
* Mappe di ArcGIS
* Percorsi di navigazione
* Funzionalità in anteprima di Power BI Desktop

### <a name="in-the-power-bi-mobile-apps"></a>Nelle app Power BI per dispositivi mobili
I report del server di report di Power BI supportano tutte le funzionalità di base nelle [app Power BI per dispositivi mobili](../mobile-apps-for-mobile-devices.md), tra cui:

* [Layout del report per il telefono](../desktop-create-phone-report.md): è possibile ottimizzare un report per le app Power BI per dispositivi mobili. Sul telefono cellulare i report ottimizzati hanno un layout e un'icona speciale, ![Icona del layout del report per il telefono](media/quickstart-create-powerbi-report/power-bi-rs-mobile-optimized-icon.png).
  
    ![Report ottimizzati per i telefoni](media/quickstart-create-powerbi-report/power-bi-rs-mobile-optimized-report.png)

I report del server di report di Power BI non supportano queste funzionalità nelle app Power BI per dispositivi mobili:

* Oggetti visivi R
* Mappe di ArcGIS
* Oggetti visivi personalizzati
* Percorsi di navigazione
* Filtro geografico o codici a barre

## <a name="next-steps"></a>Passaggi successivi
Ora che è stato installato Power BI Desktop, è possibile iniziare a creare i report di Power BI.

[Avvio rapido: Creare un report di Power BI per il server di report di Power BI](quickstart-create-powerbi-report.md)  
[Introduzione a Power BI Desktop](../desktop-getting-started.md)  
Apprendimento guidato: [Introduzione a Power BI Desktop](../guided-learning/gettingdata.yml#step-2)  
[Panoramica sul manuale per l'utente, Server di report di Power BI](user-handbook-overview.md)

Altre domande? [Provare a rivolgersi alla community di Power BI](https://community.powerbi.com/)
