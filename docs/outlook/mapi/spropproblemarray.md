---
title: SPropProblemArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SPropProblemArray
api_type:
- COM
ms.assetid: 3fbaa77a-be43-4fce-af67-1826ee101799
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f78e0ed939e190a9855ea4b040d18c01cfecc91d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406857"
---
# <a name="spropproblemarray"></a><span data-ttu-id="4dadd-103">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="4dadd-103">SPropProblemArray</span></span>

  
  
<span data-ttu-id="4dadd-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4dadd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4dadd-105">Enthält ein Array aus einer oder mehreren [SPropProblem-Strukturen.](spropproblem.md)</span><span class="sxs-lookup"><span data-stu-id="4dadd-105">Contains an array of one or more [SPropProblem](spropproblem.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4dadd-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="4dadd-106">Header file:</span></span>  <br/> |<span data-ttu-id="4dadd-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4dadd-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="4dadd-108">Verwandte Makros:</span><span class="sxs-lookup"><span data-stu-id="4dadd-108">Related macros:</span></span>  <br/> |[<span data-ttu-id="4dadd-109">CbNewSPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="4dadd-109">CbNewSPropProblemArray</span></span>](cbnewspropproblemarray.md) <br/> [<span data-ttu-id="4dadd-110">CbSPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="4dadd-110">CbSPropProblemArray</span></span>](cbspropproblemarray.md) <br/> [<span data-ttu-id="4dadd-111">SizedSPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="4dadd-111">SizedSPropProblemArray</span></span>](sizedspropproblemarray.md) <br/> |
   
```cpp
typedef struct _SPropProblemArray
{
  ULONG cProblem;
  SPropProblem aProblem[MAPI_DIM];
} SPropProblemArray, FAR *LPSPropProblemArray;

```

## <a name="members"></a><span data-ttu-id="4dadd-112">Elemente</span><span class="sxs-lookup"><span data-stu-id="4dadd-112">Members</span></span>

 <span data-ttu-id="4dadd-113">**cProblem**</span><span class="sxs-lookup"><span data-stu-id="4dadd-113">**cProblem**</span></span>
  
> <span data-ttu-id="4dadd-114">Anzahl der [SPropProblem-Strukturen](spropproblem.md) im Vom **aProblem-Element** angegebenen Array.</span><span class="sxs-lookup"><span data-stu-id="4dadd-114">Count of [SPropProblem](spropproblem.md) structures in the array indicated by the **aProblem** member.</span></span> 
    
 <span data-ttu-id="4dadd-115">**aProblem**</span><span class="sxs-lookup"><span data-stu-id="4dadd-115">**aProblem**</span></span>
  
> <span data-ttu-id="4dadd-116">Array von **SPropProblem-Strukturen,** die jeweils einen Eigenschaftsfehler beschreiben.</span><span class="sxs-lookup"><span data-stu-id="4dadd-116">Array of **SPropProblem** structures, each describing a property error.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="4dadd-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4dadd-117">Remarks</span></span>

<span data-ttu-id="4dadd-118">Weitere Informationen zur Funktionsweise der **Strukturen SPropProblem** und **SPropProblemArray** mit Eigenschaftenfehlern finden Sie unter [MAPI Named Properties](mapi-named-properties.md).</span><span class="sxs-lookup"><span data-stu-id="4dadd-118">For more information about how the **SPropProblem** and **SPropProblemArray** structures work with errors related to properties, see [MAPI Named Properties](mapi-named-properties.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4dadd-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4dadd-119">See also</span></span>



[<span data-ttu-id="4dadd-120">SCODE</span><span class="sxs-lookup"><span data-stu-id="4dadd-120">SCODE</span></span>](scode.md)
  
[<span data-ttu-id="4dadd-121">SPropProblem</span><span class="sxs-lookup"><span data-stu-id="4dadd-121">SPropProblem</span></span>](spropproblem.md)


[<span data-ttu-id="4dadd-122">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="4dadd-122">MAPI Structures</span></span>](mapi-structures.md)

