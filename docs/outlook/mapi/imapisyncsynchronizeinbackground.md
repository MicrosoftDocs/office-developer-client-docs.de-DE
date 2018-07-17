---
title: IMAPISync SynchronizeInBackground
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISync.SynchronizeInBackground
api_type:
- COM
ms.assetid: c4aaca65-d553-476c-8c6d-5f880b6efdc1
description: 'Zuletzt geändert: 26 Juni 2012'
ms.openlocfilehash: fd35d38cbb70431ab7fadbab3850a1585f9c6459
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792442"
---
# <a name="imapisync--synchronizeinbackground"></a><span data-ttu-id="3bf73-103">IMAPISync: SynchronizeInBackground</span><span class="sxs-lookup"><span data-stu-id="3bf73-103">IMAPISync : SynchronizeInBackground</span></span>

 
  
<span data-ttu-id="3bf73-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3bf73-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="3bf73-105">Initiiert eine Synchronisierung.</span><span class="sxs-lookup"><span data-stu-id="3bf73-105">Initiates a synchronization.</span></span> <span data-ttu-id="3bf73-106">Diese Methode wird von Microsoft Outlook 2010 und Microsoft Outlook 2013 aufgerufen und Zeichenfolgeneigenschaften Nachricht implementiert.</span><span class="sxs-lookup"><span data-stu-id="3bf73-106">This method is called by Microsoft Outlook 2010 and Microsoft Outlook 2013 and implemented by message store providers.</span></span> 
  
```cpp
HRESULT SynchronizeInBackground (
  PMAPISIB psibpb
);
```

## <a name="parameters"></a><span data-ttu-id="3bf73-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="3bf73-107">Parameters</span></span>

 <span data-ttu-id="3bf73-108">_psibpb_</span><span class="sxs-lookup"><span data-stu-id="3bf73-108">_psibpb_</span></span>
  
> <span data-ttu-id="3bf73-109">Informiert den Anbieter von Was synchronisiert werden soll, und ermöglicht den Zugriff auf Schnittstellen, die während der Synchronisierung verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="3bf73-109">Informs the provider of what will be synchronized and gives access to interfaces that can be used during the synchronization.</span></span> <span data-ttu-id="3bf73-110">Es ist eine [MAPISIB](mapisib.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="3bf73-110">It is a [MAPISIB](mapisib.md) structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="3bf73-111">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="3bf73-111">Return value</span></span>

<span data-ttu-id="3bf73-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="3bf73-112">S_OK</span></span> 
  
> <span data-ttu-id="3bf73-113">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="3bf73-113">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3bf73-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3bf73-114">See also</span></span>



[<span data-ttu-id="3bf73-115">IMAPISync: IUnknown</span><span class="sxs-lookup"><span data-stu-id="3bf73-115">IMAPISync : IUnknown</span></span>](imapisynciunknown.md)
  
[<span data-ttu-id="3bf73-116">MAPISIB</span><span class="sxs-lookup"><span data-stu-id="3bf73-116">MAPISIB</span></span>](mapisib.md)
