---
title: Connettersi a SweetIQ con Power BI
description: SweetIQ per Power BI
author: SarinaJoan
manager: kfile
ms.reviewer: maggiesMSFT
ms.service: powerbi
ms.component: powerbi-service
ms.topic: conceptual
ms.date: 10/16/2017
ms.author: sarinas
LocalizationGroup: Connect to services
ms.openlocfilehash: 738fbadb7be4d474cdc6f8a2aa86e6160d6c0234
ms.sourcegitcommit: 0ff358f1ff87e88daf837443ecd1398ca949d2b6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/21/2018
ms.locfileid: "46543429"
---
# <a name="connect-to-sweetiq-with-power-bi"></a>Connettersi a SweetIQ con Power BI
Il pacchetto di contenuto di Power BI estrae i dati dall'account SweetIQ e genera un set di contenuto predefinito che consente di esplorare facilmente i dati. Usare il pacchetto di contenuto SweetIQ per analizzare i dati relativamente a posizioni, elenchi, classificazioni e revisioni. I dati sono impostati in modo da essere aggiornati quotidianamente.

Connettersi al [pacchetto di contenuto SweetIQ](https://app.powerbi.com/groups/me/getdata/services/sweetiq) per Power BI.

## <a name="how-to-connect"></a>Come connettersi
1. Nel riquadro di spostamento a sinistra fare clic su **Recupera dati**.
   
    ![](media/service-connect-to-sweetiq/getdata.png)
2. Selezionare **SweetIQ** e fare clic su **Recupera**.
   
    ![](media/service-connect-to-sweetiq/sweetiq.png)
3. Fornire l'ID client di SweetIQ. In genere si tratta di un valore alfanumerico. Per altre informazioni dettagliate sull'individuazione di questo valore, vedere le informazioni seguenti.
   
    ![](media/service-connect-to-sweetiq/parameter.png)
4. Selezionare il tipo di autenticazione **Chiave** e fornire la chiave API di Sweet IQ. In genere si tratta di un valore alfanumerico. Per altre informazioni dettagliate sull'individuazione di questo valore, vedere le informazioni seguenti.
   
    ![](media/service-connect-to-sweetiq/credentials.png)
5. Power BI inizierà a caricare i dati, operazione che richiederà alcuni minuti a seconda della dimensione dei dati dell'account. Dopo aver completato il caricamento, nel riquadro di spostamento sinistro vengono visualizzati il nuovo dashboard, il nuovo report e il nuovo set di dati.
   
    ![](media/service-connect-to-sweetiq/dashboard.png)

**Altre operazioni**

* Provare a [porre una domanda nella casella Domande e risposte](consumer/end-user-q-and-a.md) nella parte superiore del dashboard
* [Cambiare i riquadri](service-dashboard-edit-tile.md) nel dashboard.
* [Selezionare un riquadro](consumer/end-user-tiles.md) per aprire il report sottostante.
* Anche se la pianificazione prevede che il set di dati venga aggiornato quotidianamente, è possibile modificarne la frequenza di aggiornamento o provare ad aggiornarlo su richiesta usando **Aggiorna ora**

## <a name="finding-parameters"></a>Individuazione dei parametri
L'ID client e la chiave API per questo pacchetto di contenuto non è uguale al nome utente e password di SweetIQ.

Selezionare un ID client per uno dei client a cui ha accesso il proprio account. È possibile trovare l'elenco di client in "Gestione dei client" nell'account SweetIQ.

Rivolgersi all'amministratore per la propria chiave API, per accedere ai dati per un client specifico.

## <a name="next-steps"></a>Passaggi successivi
[Che cos'è Power BI?](power-bi-overview.md)

[Recuperare dati per Power BI](service-get-data.md)

