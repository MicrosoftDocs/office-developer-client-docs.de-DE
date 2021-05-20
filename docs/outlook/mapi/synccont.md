---
title: SYNCCONT
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 7b4307a3-5a8c-89bf-1113-2549556a7fe7
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: afba7fa718a35d33966d45289461313e349ef2e2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430406"
---
# <a name="synccont"></a><span data-ttu-id="f8d4f-103">SYNCCONT</span><span class="sxs-lookup"><span data-stu-id="f8d4f-103">SYNCCONT</span></span>

<span data-ttu-id="f8d4f-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f8d4f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f8d4f-105">Informationen zum Synchronisieren des Inhalts der angegebenen Ordner in einem lokalen Speicher mit dem Server während des [Synchronisierungsinhaltsstatus](synchronize-contents-state.md).</span><span class="sxs-lookup"><span data-stu-id="f8d4f-105">Information for synchronizing the contents of specified folders in a local store with the server during the [synchronize contents state](synchronize-contents-state.md).</span></span> <span data-ttu-id="f8d4f-106">Dies umfasst lediglich das Hochladen oder eine vollständige Synchronisierung, die einen Upload und dann einen Download umfasst.</span><span class="sxs-lookup"><span data-stu-id="f8d4f-106">This involves just uploading, or a full synchronization involving an upload and then a download.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="f8d4f-107">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="f8d4f-107">Quick info</span></span>

```cpp
struct SYNCCONT 
{ 
   ULONG   ulFlags; 
   UINT   iEnt; 
   UINT   cEnt; 
   LPVOID    pvReserved; 
   LPSPropTagArray   ptagaReserved; 
   LPSSortOrderSet   psosReserved; 
};
```

## <a name="members"></a><span data-ttu-id="f8d4f-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="f8d4f-108">Members</span></span>

<span data-ttu-id="f8d4f-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f8d4f-109">_ulFlags_</span></span>
  
> <span data-ttu-id="f8d4f-110">[in] Flags, um das entsprechende Verhalten während der Synchronisierung zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="f8d4f-110">[in] Flags to determine the appropriate behavior during synchronization.</span></span>
    
  - <span data-ttu-id="f8d4f-111">UPC_OK</span><span class="sxs-lookup"><span data-stu-id="f8d4f-111">UPC_OK</span></span>
    
  - <span data-ttu-id="f8d4f-112">[in] Hochladen oder vollständige Synchronisierung war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="f8d4f-112">[in] Upload or full synchronization was successful.</span></span> <span data-ttu-id="f8d4f-113">Der Client legt dies nach der Synchronisierung von Informationen mit dem Server fest.</span><span class="sxs-lookup"><span data-stu-id="f8d4f-113">The client sets this after synchronizing information with the server.</span></span>
    
<span data-ttu-id="f8d4f-114">_iEnt_</span><span class="sxs-lookup"><span data-stu-id="f8d4f-114">_iEnt_</span></span>
  
> <span data-ttu-id="f8d4f-115">[out] Index, um die Synchronisierung der Inhalte in der anzahl der von _cEnt angegebenen Ordner nachverfolgt zu werden._</span><span class="sxs-lookup"><span data-stu-id="f8d4f-115">[out] Index to track synchronizing the contents in the number of folders specified by  _cEnt_.</span></span>
    
<span data-ttu-id="f8d4f-116">_cEnt_</span><span class="sxs-lookup"><span data-stu-id="f8d4f-116">_cEnt_</span></span>
  
> <span data-ttu-id="f8d4f-117">[out] Anzahl der zu replizierenden Ordner.</span><span class="sxs-lookup"><span data-stu-id="f8d4f-117">[out] Number of folders to be replicated.</span></span>
    
<span data-ttu-id="f8d4f-118">_pvReserved_</span><span class="sxs-lookup"><span data-stu-id="f8d4f-118">_pvReserved_</span></span>
  
> <span data-ttu-id="f8d4f-119">Dieses Mitglied ist für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f8d4f-119">This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="f8d4f-120">_ptagaReserved_</span><span class="sxs-lookup"><span data-stu-id="f8d4f-120">_ptagaReserved_</span></span>
  
> <span data-ttu-id="f8d4f-121">Dieses Mitglied ist für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f8d4f-121">This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="f8d4f-122">_psosReserved_</span><span class="sxs-lookup"><span data-stu-id="f8d4f-122">_psosReserved_</span></span>
  
> <span data-ttu-id="f8d4f-123">Dieses Mitglied ist für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f8d4f-123">This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="f8d4f-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f8d4f-124">See also</span></span>

- [<span data-ttu-id="f8d4f-125">Informationen über die Replikations-API</span><span class="sxs-lookup"><span data-stu-id="f8d4f-125">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="f8d4f-126">Informationen über den Replikationszustandsautomaten</span><span class="sxs-lookup"><span data-stu-id="f8d4f-126">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="f8d4f-127">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="f8d4f-127">MAPI Constants</span></span>](mapi-constants.md)

