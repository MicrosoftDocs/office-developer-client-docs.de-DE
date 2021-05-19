---
title: IMAPISyncProgressCallbackError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISyncProgressCallback.Error
api_type:
- COM
ms.assetid: 4860992d-65d7-4cb0-a874-ceccb153dbac
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 80010ca19999ba519f051e914f02f240abb524e2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424931"
---
# <a name="imapisyncprogresscallbackerror"></a><span data-ttu-id="b23eb-103">IMAPISyncProgressCallback::Error</span><span class="sxs-lookup"><span data-stu-id="b23eb-103">IMAPISyncProgressCallback::Error</span></span>

  
  
<span data-ttu-id="b23eb-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b23eb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b23eb-105">Enthält Details, die im Dialogfeld Senden/Empfangen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="b23eb-105">Provides details that are displayed in the Send/Receive dialog.</span></span> <span data-ttu-id="b23eb-106">Wenn während der Synchronisierung Fehler auftreten, ruft der Speicheranbieter diese Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="b23eb-106">If errors are encountered during synchronization, the store provider calls this function.</span></span>
  
```cpp
HRESULT Error(
  HRESULT hResult,
  const WCHAR *pwcszErrorStr
);
```

## <a name="parameters"></a><span data-ttu-id="b23eb-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="b23eb-107">Parameters</span></span>

 <span data-ttu-id="b23eb-108">**hResult**</span><span class="sxs-lookup"><span data-stu-id="b23eb-108">**hResult**</span></span>
  
> <span data-ttu-id="b23eb-109">Das HRESULT des Fehlers oder der Warnung.</span><span class="sxs-lookup"><span data-stu-id="b23eb-109">The HRESULT of the error or warning.</span></span>
    
 <span data-ttu-id="b23eb-110">**pwcszErrorStr**</span><span class="sxs-lookup"><span data-stu-id="b23eb-110">**pwcszErrorStr**</span></span>
  
> <span data-ttu-id="b23eb-111">Ein Zeiger auf die Zeichenfolge, die dem angezeigten Fehler zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="b23eb-111">A pointer to the string associated with the error to be displayed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b23eb-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b23eb-112">Return value</span></span>

<span data-ttu-id="b23eb-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="b23eb-113">S_OK</span></span> 
  
> <span data-ttu-id="b23eb-114">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="b23eb-114">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b23eb-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b23eb-115">See also</span></span>



[<span data-ttu-id="b23eb-116">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b23eb-116">IMAPISyncProgressCallback : IUnknown</span></span>](imapisyncprogresscallbackiunknown.md)

