---
title: UPMOV
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 098743a5-f265-639a-8ba6-1412705bee0a
description: 'Letzte �nderung: Donnerstag, 5. Juli 2012'
ms.openlocfilehash: 43fd56932409861db86679eea6f1405dc4c37e62
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795810"
---
# <a name="upmov"></a><span data-ttu-id="6881d-103">UPMOV</span><span class="sxs-lookup"><span data-stu-id="6881d-103">UPMOV</span></span>
 
<span data-ttu-id="6881d-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6881d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6881d-105">Informationen zum Hochladen von Elementen, die verschoben wurden.</span><span class="sxs-lookup"><span data-stu-id="6881d-105">Information for uploading items that have been moved.</span></span> <span data-ttu-id="6881d-106">Diese Informationen werden während der [Upload löschen Status Zustand](upload-delete-status-state.md) und [Status Tabelle hochladen](upload-table-state.md)verwendet.</span><span class="sxs-lookup"><span data-stu-id="6881d-106">This information is used during the [upload delete status state](upload-delete-status-state.md) and [upload table state](upload-table-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="6881d-107">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="6881d-107">Quick info</span></span>

```cpp
struct UPMOV 
{ 
      ULONG          ulFlags; 
      LPVOID         pReserved; 
      LPSTREAM       pstmReserved; 
      LPSTR          pszName; 
      FEID           feid; 
      LPMAPIFOLDER   pfld; 
      PXICC          pxicc; 
      DWORD          dwReserved; 
      PUPMOV         pupmovNext; 
      UINT           cEntMov; 
};
```

## <a name="members"></a><span data-ttu-id="6881d-108">Members</span><span class="sxs-lookup"><span data-stu-id="6881d-108">Members</span></span>

<span data-ttu-id="6881d-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6881d-109">_ulFlags_</span></span>
  
> <span data-ttu-id="6881d-110">[in] Kennzeichen, die um das entsprechende Verhalten beim Hochladen zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="6881d-110">[in] Flags to determine the appropriate behavior during the upload.</span></span>
    
  - <span data-ttu-id="6881d-111">UPV_ERROR</span><span class="sxs-lookup"><span data-stu-id="6881d-111">UPV_ERROR</span></span>
    
    - <span data-ttu-id="6881d-112">[in] Problem beim Öffnen von Serverordner.</span><span class="sxs-lookup"><span data-stu-id="6881d-112">[in] Problem opening server folder.</span></span>
    
  - <span data-ttu-id="6881d-113">UPV_DIRTY</span><span class="sxs-lookup"><span data-stu-id="6881d-113">UPV_DIRTY</span></span>
    
    - <span data-ttu-id="6881d-114">[in] Der Upload-Status hat sich geändert.</span><span class="sxs-lookup"><span data-stu-id="6881d-114">[in] The upload state has changed.</span></span> <span data-ttu-id="6881d-115">Dies wird vom Client verwendet, um die Änderung im Zustand für den lokalen Speicher zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="6881d-115">This is used by the client to track the change in state for the local store.</span></span>
    
  - <span data-ttu-id="6881d-116">UPV_COMMIT</span><span class="sxs-lookup"><span data-stu-id="6881d-116">UPV_COMMIT</span></span>
    
    - <span data-ttu-id="6881d-117">[in] Commit Upload Zustand.</span><span class="sxs-lookup"><span data-stu-id="6881d-117">[in] Commit upload state.</span></span>
    
<span data-ttu-id="6881d-118">_Beibehalten_</span><span class="sxs-lookup"><span data-stu-id="6881d-118">_pReserved_</span></span>
  
>  <span data-ttu-id="6881d-119">[out] Dieser Member wird für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6881d-119">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="6881d-120">_pstmReserved_</span><span class="sxs-lookup"><span data-stu-id="6881d-120">_pstmReserved_</span></span>
  
>  <span data-ttu-id="6881d-121">[out] Dieser Member wird für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6881d-121">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="6881d-122">_pszName_</span><span class="sxs-lookup"><span data-stu-id="6881d-122">_pszName_</span></span>
  
>  <span data-ttu-id="6881d-123">[out] Name des Zielordners.</span><span class="sxs-lookup"><span data-stu-id="6881d-123">[out] Name of the destination folder.</span></span> 
    
  > [!NOTE]
  > <span data-ttu-id="6881d-124">Dieser Member wird UNICODE nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6881d-124">This member does not support UNICODE.</span></span> 
  
<span data-ttu-id="6881d-125">_feid_</span><span class="sxs-lookup"><span data-stu-id="6881d-125">_feid_</span></span>
  
>  <span data-ttu-id="6881d-126">[out] Eintrags-ID der Zielordner.</span><span class="sxs-lookup"><span data-stu-id="6881d-126">[out] Entry ID of destination folder.</span></span> 
    
<span data-ttu-id="6881d-127">_pfld_</span><span class="sxs-lookup"><span data-stu-id="6881d-127">_pfld_</span></span>
  
>  <span data-ttu-id="6881d-128">[in] Zeiger auf den Ordner auf dem Server.</span><span class="sxs-lookup"><span data-stu-id="6881d-128">[in] Pointer to server folder.</span></span> 
    
<span data-ttu-id="6881d-129">_pxicc_</span><span class="sxs-lookup"><span data-stu-id="6881d-129">_pxicc_</span></span>
  
>  <span data-ttu-id="6881d-130">[in] Zeiger auf die Schnittstelle der **IExchangeImportContentsChanges** -Inhalt, die Hochladen von Änderungen bei Verwendung von inkrementelle Änderung Synchronisierung (ICS) unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6881d-130">[in] Pointer to the **IExchangeImportContentsChanges** contents interface that supports uploading content changes when using Incremental Change Synchronization (ICS).</span></span> <span data-ttu-id="6881d-131">Weitere Informationen zu **IExchangeImportContentsChanges** und ICS finden Sie unter [ICS Bewertungskriterien](http://msdn.microsoft.com/de-de/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="6881d-131">For more information on **IExchangeImportContentsChanges** and ICS, see [ICS Evaluation Criteria](http://msdn.microsoft.com/de-de/library/aa579252%28EXCHG.80%29.aspx).</span></span>
    
<span data-ttu-id="6881d-132">_dwReserved_</span><span class="sxs-lookup"><span data-stu-id="6881d-132">_dwReserved_</span></span>
  
>  <span data-ttu-id="6881d-133">[out] Dieser Member wird für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6881d-133">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="6881d-134">_pupmovNext_</span><span class="sxs-lookup"><span data-stu-id="6881d-134">_pupmovNext_</span></span>
  
>  <span data-ttu-id="6881d-135">[out] Als Nächstes Kontext zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="6881d-135">[out] Next move context.</span></span> 
    
<span data-ttu-id="6881d-136">_cEntMov_</span><span class="sxs-lookup"><span data-stu-id="6881d-136">_cEntMov_</span></span>
  
>  <span data-ttu-id="6881d-137">[in] Anzahl der Elemente hier verschoben.</span><span class="sxs-lookup"><span data-stu-id="6881d-137">[in] Number of items moved here.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="6881d-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6881d-138">See also</span></span>

- [<span data-ttu-id="6881d-139">Über die API-Replikation</span><span class="sxs-lookup"><span data-stu-id="6881d-139">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="6881d-140">Informationen zu den Replikationsstatus Computer</span><span class="sxs-lookup"><span data-stu-id="6881d-140">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="6881d-141">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="6881d-141">MAPI Constants</span></span>](mapi-constants.md)
- [<span data-ttu-id="6881d-142">FEID</span><span class="sxs-lookup"><span data-stu-id="6881d-142">FEID</span></span>](feid.md)
