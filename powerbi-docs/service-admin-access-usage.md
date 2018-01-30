---
title: Ricerca di utenti Power BI che hanno eseguito l'accesso
description: "Se si è un amministratore tenant e si desidera vedere chi ha effettuato l'accesso a Power BI, è possibile usare i report d'uso e di accesso di Azure Active Directory per ottenere informazioni."
services: powerbi
documentationcenter: 
author: guyinacube
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
ms.date: 08/10/2017
ms.author: asaxton
ms.openlocfilehash: 55caee3b289f187d6b955c216098313b483956f5
ms.sourcegitcommit: b3ee37e1587f1269ee7dd9daf1685a06dea3b50c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/23/2017
---
# <a name="find-power-bi-users-that-have-signed-in"></a>Ricerca di utenti Power BI che hanno eseguito l'accesso
Se si è un amministratore tenant e si desidera vedere chi ha effettuato l'accesso a Power BI, è possibile usare i report d'uso e di accesso di Azure Active Directory per ottenere informazioni.

<iframe width="640" height="360" src="https://www.youtube.com/embed/1AVgh9w9VM8?showinfo=0" frameborder="0" allowfullscreen></iframe>

È possibile accedere al report di attività all'interno dei portali [nuovo](https://docs.microsoft.com/azure/active-directory/active-directory-reporting-activity-sign-ins) e [classico](https://docs.microsoft.com/azure/active-directory/active-directory-view-access-usage-reports) di Azure Active Directory (Azure AD). Mentre il video precedente usa il portale classico come esempio, in questo articolo verrà messo in evidenza il nuovo portale.

> [!NOTE]
> Questo report di attività include utenti sia Power BI (gratuito) che Pro, ma non li identifica in base al tipo di licenza.
> 
> 

## <a name="requirements"></a>Requisiti
Di seguito sono indicati i requisiti per visualizzare il report delle attività di accesso.

* Possono accedere ai dati gli utenti con il ruolo Amministratore globale, Amministratore della sicurezza o Ruolo con autorizzazioni di lettura per la sicurezza.
* Ogni altro utente (non amministratore) può visualizzare i propri accessi.
* Il tenant deve disporre di una licenza Azure AD Premium a esso associata per visualizzare il report con le attività di accesso.

## <a name="using-the-azure-portal-to-view-sign-ins"></a>Uso del portale di Azure per visualizzare gli accessi
Per visualizzare l'attività di accesso è possibile usare il portale di Azure AD.

1. Individuare il **portale di Azure** e selezionare **Azure Active Directory**.
2. In **Attività**, selezionare **Accessi**.
   
    ![](media/service-admin-access-usage/azure-portal-sign-ins.png)
3. Filtrare l'applicazione tramite **Microsoft Power BI** o **Power BI Gateway** e selezionare **Applica**.
   
    **Microsoft Power BI** indica le attività di accesso relative al servizio, mentre **Power BI Gateway** indica gli accessi specifici per il gateway dati locale.
   
    ![](media/service-admin-access-usage/sign-in-filter.png)

## <a name="export-the-data"></a>Esportazione dei dati
Per esportare i dati di accesso sono disponibili due opzioni. Questa operazione può essere eseguita scaricando un file csv o tramite PowerShell.

### <a name="download-csv"></a>Download del file csv
All'interno della schermata Attività è possibile selezionare **Download** nella barra degli strumenti. Così facendo si scaricherà un file csv per i dati attualmente filtrati.

![](media/service-admin-access-usage/download-sign-in-data-csv.png)

### <a name="powershell"></a>PowerShell
È possibile usare PowerShell per esportare i dati di accesso. Un [esempio](https://docs.microsoft.com/azure/active-directory/active-directory-reporting-api-sign-in-activity-samples#powershell-script) è disponibile all'interno della documentazione di Azure AD.

> [!NOTE]
> Perché l'esempio di PowerShell funzioni, assicurarsi di rispettare i [prerequisiti per accedere all'API di creazione report di Azure AD](https://docs.microsoft.com/en-us/azure/active-directory/active-directory-reporting-api-prerequisites).
> 
> 

## <a name="data-retention"></a>Conservazione dei dati
I dati di accesso rimangono disponibili per un massimo di 30 giorni. Per altre informazioni, vedere [Azure Active Directory report retention policies](https://docs.microsoft.com/azure/active-directory/active-directory-reporting-retention) (Criteri di conservazione dei report di Azure Active Directory).

## <a name="next-steps"></a>Passaggi successivi
[Sign-in activity reports in the Azure Active Directory portal (New Portal)](https://docs.microsoft.com/azure/active-directory/active-directory-reporting-activity-sign-ins) (Report sulle attività di accesso al portale di Azure Active Directory (nuovo portale))  
[View your access and usage reports (Classic Portal)](https://docs.microsoft.com/azure/active-directory/active-directory-view-access-usage-reports#view-or-download-a-report) (Visualizzare i report di uso e di accesso (portale classico))  
[Sign-in sample PowerShell script](https://docs.microsoft.com/azure/active-directory/active-directory-reporting-api-sign-in-activity-samples#powershell-script) (esempio di accesso di uno script di PowerShell)  
[Azure Active Directory report retention policies](https://docs.microsoft.com/azure/active-directory/active-directory-reporting-retention) (Criteri di conservazione dei report di Azure Active Directory)  
[Uso del controllo nell'organizzazione](service-admin-auditing.md)  
[Extended Pro Trial activation](service-extended-pro-trial.md) (Attivazione della versione di valutazione Pro estesa)

Altre domande? [Provare a rivolgersi alla community di Power BI](https://community.powerbi.com/)
