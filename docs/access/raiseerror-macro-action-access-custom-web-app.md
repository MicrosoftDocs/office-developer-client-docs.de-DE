---
title: RaiseError-Makroaktion (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 5e29bf64-300a-4094-82ff-664e79782d86
description: Die RaiseError-Aktion zeigt ein Popupfenster an, das eine angegebene Fehlermeldung enthält.
ms.openlocfilehash: 49e544d2234759709c19052b5540d42e88070849
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408243"
---
# <a name="raiseerror-macro-action-access-custom-web-app"></a><span data-ttu-id="14031-103">RaiseError-Makroaktion (benutzerdefinierte Access-Web-App)</span><span class="sxs-lookup"><span data-stu-id="14031-103">RaiseError Macro Action (Access custom web app)</span></span>

<span data-ttu-id="14031-104">Die **RaiseError-Aktion** zeigt ein Popupfenster an, das eine angegebene Fehlermeldung enthält.</span><span class="sxs-lookup"><span data-stu-id="14031-104">The **RaiseError** action displays a popup window that contains a specified error message.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="14031-p101">Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen.</span><span class="sxs-lookup"><span data-stu-id="14031-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="14031-107">Die **AuslösenFehler**-Aktion ist nur in Datenmakros verfügbar.</span><span class="sxs-lookup"><span data-stu-id="14031-107">The **RaiseError** action is available only in Data Macros.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="14031-108">Setting</span><span class="sxs-lookup"><span data-stu-id="14031-108">Setting</span></span>

<span data-ttu-id="14031-109">Die **RaiseError-Aktion** hat das folgende Argument.</span><span class="sxs-lookup"><span data-stu-id="14031-109">The **RaiseError** action has the following argument.</span></span> 
  
|<span data-ttu-id="14031-110">**Argument**</span><span class="sxs-lookup"><span data-stu-id="14031-110">**Argument**</span></span>|<span data-ttu-id="14031-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="14031-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="14031-112">_Fehlerbeschreibung_</span><span class="sxs-lookup"><span data-stu-id="14031-112">_Error Description_</span></span> <br/> |<span data-ttu-id="14031-113">Ein Zeichenfolgenausdruck, der den Fehler beschreibt.</span><span class="sxs-lookup"><span data-stu-id="14031-113">A string expression that describes the error.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="14031-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="14031-114">Remarks</span></span>

<span data-ttu-id="14031-115">Wenn die **RaiseError-Aktion** aufgerufen wird, werden alle Vorgänge in der aktuellen Transaktion zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="14031-115">When the **RaiseError** action is called, all of the operations in the current transaction are rolled back.</span></span> 
  

