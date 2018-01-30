---
title: Connettersi al pacchetto di contenuto di Microsoft Dynamics AX con Power BI
description: Pacchetto di contenuto Microsoft Dynamics AX per Power BI
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
ms.openlocfilehash: 38b9233bda842877b4c8c16df2904f5fe8b1966d
ms.sourcegitcommit: d803e85bb0569f6b357ba0586f5702c20d27dac4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/19/2018
---
# <a name="connect-to-microsoft-dynamics-ax-content-pack-with-power-bi"></a>Connettersi al pacchetto di contenuto di Microsoft Dynamics AX con Power BI
Microsoft Dynamics AX include tre pacchetti di contenuto Power BI destinati a utenti aziendali diversi. Il pacchetto di contenuto Financial Performance, progettato specificamente per i CFO, offre informazioni dettagliate sulle prestazioni finanziarie dell'organizzazione. Il pacchetto di contenuto Retail Channel Performance, destinato ai responsabili di canale, interpreta le prestazioni di vendita per prevedere tendenze e cogliere intuizioni direttamente dai dati di Retail and Commerce . Il pacchetto di contenuto Cost Management è progettato per i COO e i CFO e offre informazioni dettagliate sulle prestazioni operative.

Connettersi al pacchetto di contenuto Microsoft Dynamics AX [Retail Channel Performance](https://app.powerbi.com/getdata/services/dynamics-ax-retail-channel-performance), [Financial Performance](https://app.powerbi.com/getdata/services/dynamics-ax-financial-performance) o [Cost Management](https://app.powerbi.com/getdata/services/dynamics-ax-cost-management) per Power BI.

## <a name="how-to-connect"></a>Come connettersi
1. Selezionare **Recupera dati** nella parte inferiore del riquadro di spostamento sinistro.
   
   ![](media/service-connect-to-microsoft-dynamics-ax/getdata.png)
2. Nella casella **Servizi** selezionare **Recupera**.
   
   ![](media/service-connect-to-microsoft-dynamics-ax/services.png)
3. Selezionare uno dei pacchetti di contenuto di Dynamics AX e scegliere **Recupera**.
   
   ![](media/service-connect-to-microsoft-dynamics-ax/mdax.png)
4. Specificare l'URL dell'ambiente Dynamics AX 7 in uso. Per informazioni dettagliate su come [trovare questi parametri](#FindingParams), vedere più avanti.
   
   ![](media/service-connect-to-microsoft-dynamics-ax/params.png)
5. In **Metodo di autenticazione** selezionare **oAuth2** \> **Accedi**. Quando richiesto, immettere le credenziali di Dynamics AX.
   
    ![](media/service-connect-to-microsoft-dynamics-ax/creds.png)
   
    ![](media/service-connect-to-microsoft-dynamics-ax/creds2.png)
6. Dopo l'approvazione, il processo di importazione inizierà automaticamente. Al termine nel riquadro di spostamento verranno visualizzati un nuovo dashboard, un nuovo report e un nuovo set di dati. Selezionare il dashboard per visualizzare i dati importati.
   
     ![](media/service-connect-to-microsoft-dynamics-ax/dashboard.png)

**Altre operazioni**

* Provare a [porre una domanda nella casella Domande e risposte](power-bi-q-and-a.md) nella parte superiore del dashboard
* [Cambiare i riquadri](service-dashboard-edit-tile.md) nel dashboard.
* [Selezionare un riquadro](service-dashboard-tiles.md) per aprire il report sottostante.
* Anche se la pianificazione prevede che il set di dati venga aggiornato quotidianamente, è possibile modificare la frequenza di aggiornamento o provare ad aggiornarlo su richiesta usando **Aggiorna ora**

## <a name="whats-included"></a>Cosa è incluso
Il pacchetto di contenuto usa il feed OData Dynamics AX 7 per importare i dati correlati rispettivamente a Retail Channel, a Financial Performance e a Cost Management.

## <a name="system-requirements"></a>Requisiti di sistema
Questo pacchetto di contenuto richiede l'URL di un ambiente Dynamics AX 7. L'utente deve avere accesso al feed OData.

## <a name="finding-parameters"></a>Individuazione dei parametri
<a name="FindingParams"></a>

L'URL dell'ambiente Dynamics AX 7 è già presente nel browser quando l'utente effettua l'accesso. Copiare semplicemente l'URL dell'ambiente Dynamics AX radice nella finestra di dialogo di Power BI.

## <a name="troubleshooting"></a>Risoluzione dei problemi
A seconda della dimensione dell'istanza, il caricamento dei dati potrebbe richiedere tempo. Se all'interno di Power BI vengono visualizzati report vuoti, verificare di avere accesso alle tabelle OData necessarie per tali report.

## <a name="next-steps"></a>Passaggi successivi
[Introduzione a Power BI](service-get-started.md)

[Recuperare dati in Power BI](service-get-data.md)
