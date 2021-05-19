---
title: SYNC
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3f07fddf-4c42-6ea7-162d-57022166a83f
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: e856044a1b6345c4e495a75dfb7ca0defa52ceec
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433808"
---
# <a name="sync"></a><span data-ttu-id="9414f-103">SYNC</span><span class="sxs-lookup"><span data-stu-id="9414f-103">SYNC</span></span>

  
  
<span data-ttu-id="9414f-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9414f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9414f-105">Informationen zum Starten der Synchronisierung zwischen einem lokalen Speicher und einem Server.</span><span class="sxs-lookup"><span data-stu-id="9414f-105">Information for starting synchronization between a local store and a server.</span></span> <span data-ttu-id="9414f-106">Diese Informationen werden während des [Synchronisierungsstatus verwendet.](synchronize-state.md)</span><span class="sxs-lookup"><span data-stu-id="9414f-106">This information is used during the [synchronize state](synchronize-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="9414f-107">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="9414f-107">Quick info</span></span>

```cpp
struct SYNC 
{ 
    ULONG ulFlags; 
    LPWSTR pwzPath; 
    FEID Reserved1; 
    MEID Reserved2; 
    LPENTRYLIST pel; 
    ULONG const * pulFolderOptions; 
};
```

## <a name="members"></a><span data-ttu-id="9414f-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="9414f-108">Members</span></span>

 <span data-ttu-id="9414f-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9414f-109">_ulFlags_</span></span>
  
- <span data-ttu-id="9414f-110">[out]/[in] Eine Bitmaske der folgenden Flags, die das Verhalten während der Synchronisierung ändern:</span><span class="sxs-lookup"><span data-stu-id="9414f-110">[out]/[in] A bitmask of the following flags that modifies the behavior during synchronization:</span></span>
    
- <span data-ttu-id="9414f-111">UPS_UPLOAD_ONLY</span><span class="sxs-lookup"><span data-stu-id="9414f-111">UPS_UPLOAD_ONLY</span></span>
    
  - <span data-ttu-id="9414f-112">[in] Der Client wird nur hochladen.</span><span class="sxs-lookup"><span data-stu-id="9414f-112">[in] The client will be performing only upload.</span></span> <span data-ttu-id="9414f-113">Outlook gibt nur lokal geänderte Ordner zurück.</span><span class="sxs-lookup"><span data-stu-id="9414f-113">Outlook only returns locally modified folders.</span></span>
    
- <span data-ttu-id="9414f-114">UPS_DNLOAD_ONLY</span><span class="sxs-lookup"><span data-stu-id="9414f-114">UPS_DNLOAD_ONLY</span></span>
    
  - <span data-ttu-id="9414f-115">[in] Der Client wird nur herunterladen ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9414f-115">[in] The client will be performing only download.</span></span> <span data-ttu-id="9414f-116">Outlook sollten keine Uploadbits für Ordner löschen.</span><span class="sxs-lookup"><span data-stu-id="9414f-116">Outlook should not clear upload bits for folders.</span></span>
    
- <span data-ttu-id="9414f-117">UPS_THESE_FOLDERS</span><span class="sxs-lookup"><span data-stu-id="9414f-117">UPS_THESE_FOLDERS</span></span>
    
  - <span data-ttu-id="9414f-118">[in] Der Client synchronisiert einen angegebenen Satz von Ordnern mit den bereitgestellten Eintrags-IDs.</span><span class="sxs-lookup"><span data-stu-id="9414f-118">[in] The client will be synchronizing a specified set of folders with the provided entry IDs.</span></span> <span data-ttu-id="9414f-119">Dieses Flag kann entweder mit dem UPS_UPLOAD_ONLY **oder** **UPS_DNLOAD_ONLY** kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="9414f-119">This flag can be combined with either the **UPS_UPLOAD_ONLY** or **UPS_DNLOAD_ONLY** flag.</span></span> 
    
- <span data-ttu-id="9414f-120">UPS_OK</span><span class="sxs-lookup"><span data-stu-id="9414f-120">UPS_OK</span></span>
    
  - <span data-ttu-id="9414f-121">[out] Die Synchronisierung war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="9414f-121">[out] Synchronization was successful.</span></span> <span data-ttu-id="9414f-122">Der Client legt dies nach dem Hochladen fest, oder eine vollständige Synchronisierung ist abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="9414f-122">The client sets this after uploading or a full synchronization completes.</span></span>
    
- 
    
    > [!NOTE]
    > <span data-ttu-id="9414f-123">Auch wenn der Client Ordner und Elemente entweder mit der Replikations-API hochladen oder vollständig mit der Replikations-API synchronisieren (hochladen und dann herunterladen) kann, gibt der Client *ulFlags* mit nur einer Richtung der Replikation gleichzeitig an – entweder das **flag UPS_UPLOAD_ONLY** oder **UPS_DNLOAD_ONLY.**</span><span class="sxs-lookup"><span data-stu-id="9414f-123">Even though the client can either upload or fully synchronize (upload then download) folders and items with the Replication API, the client specifies  *ulFlags*  with only one direction of the replication at a time — either the **UPS_UPLOAD_ONLY** or **UPS_DNLOAD_ONLY** flag.</span></span> <span data-ttu-id="9414f-124">Bei einer vollständigen Synchronisierung führt der Client  zunächst einen Upload mit dem UPS_UPLOAD_ONLY und dann einen Download mit dem UPS_DNLOAD_ONLY **aus.**</span><span class="sxs-lookup"><span data-stu-id="9414f-124">In the case of a full synchronization, the client first does an upload with the **UPS_UPLOAD_ONLY** flag, and then a download with the **UPS_DNLOAD_ONLY** flag.</span></span> 
  
 <span data-ttu-id="9414f-125">_pwzPath_</span><span class="sxs-lookup"><span data-stu-id="9414f-125">_pwzPath_</span></span>
  
- <span data-ttu-id="9414f-126">[out] Pfad zum lokalen Speicher.</span><span class="sxs-lookup"><span data-stu-id="9414f-126">[out] Path to the local store.</span></span>
    
 <span data-ttu-id="9414f-127">_Reserved1_</span><span class="sxs-lookup"><span data-stu-id="9414f-127">_Reserved1_</span></span>
  
- <span data-ttu-id="9414f-128">Dieses Mitglied ist für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9414f-128">This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
 <span data-ttu-id="9414f-129">_Reserved2_</span><span class="sxs-lookup"><span data-stu-id="9414f-129">_Reserved2_</span></span>
  
- <span data-ttu-id="9414f-130">Dieses Mitglied ist für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9414f-130">This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
 <span data-ttu-id="9414f-131">*pel*</span><span class="sxs-lookup"><span data-stu-id="9414f-131">*pel*</span></span> 
  
- <span data-ttu-id="9414f-132">[in] Dies ist die Liste der Eintrags-IDs der Ordner, die synchronisiert werden sollen, **UPS_THESE_FOLDERS** festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="9414f-132">[in] This is the list of entry IDs of the folders to synchronize if **UPS_THESE_FOLDERS** has been set.</span></span> <span data-ttu-id="9414f-133">Die Typdefinition von **LPENTRYLIST** finden Sie unter mapidefs.h.</span><span class="sxs-lookup"><span data-stu-id="9414f-133">See mapidefs.h for the type definition of **LPENTRYLIST**.</span></span> 
    
 <span data-ttu-id="9414f-134">_pulFolderOptions_</span><span class="sxs-lookup"><span data-stu-id="9414f-134">_pulFolderOptions_</span></span>
  
- <span data-ttu-id="9414f-135">[in] Dies ist ein Array von Ordneroptionen für entsprechende Ordner in  *Pel,* **wenn UPS_THESE_FOLDERS** festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="9414f-135">[in] This is an array of folder options for corresponding folders in  *pel*  if **UPS_THESE_FOLDERS** has been set.</span></span> <span data-ttu-id="9414f-136">Diese Ordneroptionen werden beim Hochladen der einzelnen Ordner verwendet, die in *pel* während des [Status des Uploadordners aufgeführt sind.](upload-folder-state.md)</span><span class="sxs-lookup"><span data-stu-id="9414f-136">These folder options are used when uploading each of the folders listed in  *pel*  during the [upload folder state](upload-folder-state.md).</span></span> <span data-ttu-id="9414f-137">Weitere Informationen zu Ordneroptionen finden Sie unter **[UPFLD](upfld.md)**.</span><span class="sxs-lookup"><span data-stu-id="9414f-137">For more information about folder options, see **[UPFLD](upfld.md)**.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="9414f-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9414f-138">See also</span></span>



[<span data-ttu-id="9414f-139">Informationen über die Replikations-API</span><span class="sxs-lookup"><span data-stu-id="9414f-139">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="9414f-140">Informationen über den Replikationszustandsautomaten</span><span class="sxs-lookup"><span data-stu-id="9414f-140">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="9414f-141">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="9414f-141">MAPI Constants</span></span>](mapi-constants.md)

