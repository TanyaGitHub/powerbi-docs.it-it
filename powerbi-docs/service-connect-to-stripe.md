---
title: Connettersi a Stripe con Power BI
description: Stripe per Power BI
services: powerbi
documentationcenter: 
author: joeshoukry
manager: kfile
backup: maggiesMSFT
editor: 
tags: 
qualityfocus: no
qualitydate: 
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 10/16/2017
ms.author: yshoukry
ms.openlocfilehash: 5ed68a3ee64803fa895ad9837fe37351163d09af
ms.sourcegitcommit: d803e85bb0569f6b357ba0586f5702c20d27dac4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/19/2018
---
# <a name="connect-to-stripe-with-power-bi"></a>Connettersi a Stripe con Power BI
Visualizzare ed esplorare i dati di Stripe in Power BI con il pacchetto di contenuto Power BI. Il pacchetto di contenuto Stripe di Power BI esegue il pull dei dati su clienti, spese, eventi e fatture. I dati includono i diecimila eventi più recenti e le cinquemila spese effettuate negli ultimi 30 giorni. Il contenuto verrà aggiornato automaticamente una volta al giorno secondo una pianificazione controllata dall'utente. 

Connettersi al [pacchetto di contenuto Stripe per Power BI](https://app.powerbi.com/getdata/services/stripe).

## <a name="how-to-connect"></a>Come connettersi
1. Selezionare Recupera dati nella parte inferiore del riquadro di spostamento sinistro.  
   
    ![](media/service-connect-to-stripe/getdata.png)
2. Nella casella **Servizi** selezionare **Recupera**.  
   
    ![](media/service-connect-to-stripe/services.png)  
3. Selezionare **Stripe** &gt; **Recupera**.  
   
    ![](media/service-connect-to-stripe/stripe.png)  
4. Specificare la [chiave API](https://dashboard.stripe.com/account/apikeys) di Stripe per la connessione.  
   
    ![](media/service-connect-to-stripe/creds.png)
5. Il processo di importazione inizierà automaticamente. Al termine nel riquadro di spostamento verranno visualizzati un nuovo dashboard, un nuovo report e un nuovo set di dati, contrassegnato con un asterisco. Selezionare il dashboard per visualizzare i dati importati.
   
    ![](media/service-connect-to-stripe/dashboard.png)

**Altre operazioni**

* Provare a [porre una domanda nella casella Domande e risposte](power-bi-q-and-a.md) nella parte superiore del dashboard
* [Cambiare i riquadri](service-dashboard-edit-tile.md) nel dashboard.
* [Selezionare un riquadro](service-dashboard-tiles.md) per aprire il report sottostante.
* Anche se la pianificazione prevede che il set di dati venga aggiornato quotidianamente, è possibile modificare la frequenza di aggiornamento o provare ad aggiornarlo su richiesta usando **Aggiorna ora**

## <a name="next-steps"></a>Passaggi successivi
[Introduzione a Power BI](service-get-started.md)

[Recuperare dati per Power BI](service-get-data.md)
