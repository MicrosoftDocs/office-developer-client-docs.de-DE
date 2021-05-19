---
title: UPREADE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d146ee74-0c3a-5fdd-b1aa-af6498550801
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 1df2c665f8e9d7a0bd6d47ec59b2adf706bead75
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434144"
---
# <a name="upreade"></a><span data-ttu-id="f5723-103">UPREADE</span><span class="sxs-lookup"><span data-stu-id="f5723-103">UPREADE</span></span>

<span data-ttu-id="f5723-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f5723-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f5723-105">Erweiterte Informationen zum Hochladen des Lesestatus eines Elements während des [Status des Upload-Lesestatus](upload-read-status-state.md).</span><span class="sxs-lookup"><span data-stu-id="f5723-105">Extended information for uploading the read state of an item during the [upload read status state](upload-read-status-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="f5723-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="f5723-106">Quick info</span></span>

```cpp
struct UPREADE 
{ 
    ULONG ulFlags; 
    SKEY skey; 
};
```

## <a name="members"></a><span data-ttu-id="f5723-107">Elemente</span><span class="sxs-lookup"><span data-stu-id="f5723-107">Members</span></span>

<span data-ttu-id="f5723-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f5723-108">_ulFlags_</span></span>
  
>  <span data-ttu-id="f5723-109">[out]/[in] Flags, um das entsprechende Verhalten während des Uploads zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="f5723-109">[out]/[in] Flags to determine the appropriate behavior during the upload.</span></span> 
    
  - <span data-ttu-id="f5723-110">UPR_ASSOC</span><span class="sxs-lookup"><span data-stu-id="f5723-110">UPR_ASSOC</span></span>
    
    - <span data-ttu-id="f5723-111">[out] Element ist ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="f5723-111">[out] Item is hidden.</span></span>
    
  - <span data-ttu-id="f5723-112">UPR_READ</span><span class="sxs-lookup"><span data-stu-id="f5723-112">UPR_READ</span></span>
    
    - <span data-ttu-id="f5723-113">[out] Der Lesestatus des Elements wurde geändert.</span><span class="sxs-lookup"><span data-stu-id="f5723-113">[out] The read status of the item has been changed.</span></span>
    
  - <span data-ttu-id="f5723-114">UPR_OK</span><span class="sxs-lookup"><span data-stu-id="f5723-114">UPR_OK</span></span>
    
    - <span data-ttu-id="f5723-115">[in] Hochladen war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="f5723-115">[in] Upload was successful.</span></span> <span data-ttu-id="f5723-116">Der Client legt dies nach dem Hochladen von Informationen auf den Server fest.</span><span class="sxs-lookup"><span data-stu-id="f5723-116">The client sets this after uploading information to the server.</span></span>
    
  - <span data-ttu-id="f5723-117">UPR_COMMIT</span><span class="sxs-lookup"><span data-stu-id="f5723-117">UPR_COMMIT</span></span>
    
    - <span data-ttu-id="f5723-118">[in] Hochladen den Lesestatus des Elements jetzt anstatt bis zum [](upload-table-state.md) Ende des Status der Uploadtabelle zu warten, um mehrere Elemente zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="f5723-118">[in] Upload the read status of the item now, instead of waiting to the end of the [upload table state](upload-table-state.md) to batch-process more than one item.</span></span> 
    
<span data-ttu-id="f5723-119">_skey_</span><span class="sxs-lookup"><span data-stu-id="f5723-119">_skey_</span></span>
  
> <span data-ttu-id="f5723-120">[out] Quellschlüssel des Elements.</span><span class="sxs-lookup"><span data-stu-id="f5723-120">[out] Source key of the item.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f5723-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f5723-121">See also</span></span>

- [<span data-ttu-id="f5723-122">Informationen über die Replikations-API</span><span class="sxs-lookup"><span data-stu-id="f5723-122">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="f5723-123">Informationen über den Replikationszustandsautomaten</span><span class="sxs-lookup"><span data-stu-id="f5723-123">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="f5723-124">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="f5723-124">MAPI Constants</span></span>](mapi-constants.md)
- [<span data-ttu-id="f5723-125">UPREAD</span><span class="sxs-lookup"><span data-stu-id="f5723-125">UPREAD</span></span>](upread.md)

