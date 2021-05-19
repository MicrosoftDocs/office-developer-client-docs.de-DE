---
title: FBadProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FBadProp
api_type:
- HeaderDef
ms.assetid: 929330c8-e6f2-4adf-a36e-fba18fa055d4
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: d899c8af541da231b015f6178eb7bc8f0ffd86e0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426716"
---
# <a name="fbadprop"></a><span data-ttu-id="1ef76-103">FBadProp</span><span class="sxs-lookup"><span data-stu-id="1ef76-103">FBadProp</span></span>

  
  
<span data-ttu-id="1ef76-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1ef76-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1ef76-105">Überprüft eine angegebene Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="1ef76-105">Validates a specified property.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1ef76-106">Headerdatei:</span><span class="sxs-lookup"><span data-stu-id="1ef76-106">Header file:</span></span>  <br/> |<span data-ttu-id="1ef76-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="1ef76-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="1ef76-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="1ef76-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="1ef76-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="1ef76-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="1ef76-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="1ef76-110">Called by:</span></span>  <br/> |<span data-ttu-id="1ef76-111">Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="1ef76-111">Service providers</span></span>  <br/> |
   
```cpp
ULONG FBadProp(
  LPSPropValue lpprop
);
```

## <a name="parameters"></a><span data-ttu-id="1ef76-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="1ef76-112">Parameters</span></span>

 <span data-ttu-id="1ef76-113">_lpprop_</span><span class="sxs-lookup"><span data-stu-id="1ef76-113">_lpprop_</span></span>
  
> <span data-ttu-id="1ef76-114">[in] Eine [SPropValue](spropvalue.md)-Struktur definiert die zu überprüfende Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="1ef76-114">[in] An [SPropValue](spropvalue.md) structure defining the property to be validated.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="1ef76-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1ef76-115">Return value</span></span>

<span data-ttu-id="1ef76-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="1ef76-116">TRUE</span></span> 
  
> <span data-ttu-id="1ef76-117">Die angegebene Eigenschaft ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="1ef76-117">The specified property is invalid.</span></span> 
    
<span data-ttu-id="1ef76-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="1ef76-118">FALSE</span></span> 
  
> <span data-ttu-id="1ef76-119">Die angegebene Eigenschaft ist gültig.</span><span class="sxs-lookup"><span data-stu-id="1ef76-119">The specified property is valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1ef76-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1ef76-120">Remarks</span></span>

<span data-ttu-id="1ef76-121">Ein Dienstanbieter kann die **FBadProp**-Funktion aus mehreren Gründen aufrufen, z. B. zur Vorbereitung auf einen Aufruf der [IMAPIProp::SetProps](imapiprop-setprops.md)-Methode, die eine Eigenschaft festlegt.</span><span class="sxs-lookup"><span data-stu-id="1ef76-121">A service provider can call the **FBadProp** function for several reasons, for example to prepare for a call to the [IMAPIProp::SetProps](imapiprop-setprops.md) method setting a property.</span></span> <span data-ttu-id="1ef76-122">**FBadProp** überprüft die angegebene Eigenschaft in Abhängigkeit vom Eigenschaftentyp.</span><span class="sxs-lookup"><span data-stu-id="1ef76-122">**FBadProp** validates the specified property depending on the property type.</span></span> <span data-ttu-id="1ef76-123">Wenn die Eigenschaft beispielsweise „Boolean“ ist, wird durch **FBadProp** sichergestellt, dass der Wert entweder TRUE oder FALSE ist.</span><span class="sxs-lookup"><span data-stu-id="1ef76-123">For example, if the property is Boolean, **FBadProp** make sures that its value is either TRUE or FALSE.</span></span> <span data-ttu-id="1ef76-124">Wenn die Eigenschaft „binary“ ist, überprüft **FBadProp** Zeiger und Größe und stellt sicher, dass sie korrekt zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="1ef76-124">If the property is binary, **FBadProp** checks its pointer and size and makes sure that it is allocated correctly.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1ef76-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1ef76-125">See also</span></span>



[<span data-ttu-id="1ef76-126">FBadPropTag</span><span class="sxs-lookup"><span data-stu-id="1ef76-126">FBadPropTag</span></span>](fbadproptag.md)

