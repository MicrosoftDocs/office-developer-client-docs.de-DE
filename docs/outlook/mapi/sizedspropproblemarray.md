---
title: SizedSPropProblemArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedSPropProblemArray
api_type:
- COM
ms.assetid: 2fc3febb-8c69-4315-a112-a28eee98013d
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: b8521172b441bd26a6562aa28f836d453544928f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795550"
---
# <a name="sizedspropproblemarray"></a><span data-ttu-id="67d8f-103">SizedSPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="67d8f-103">SizedSPropProblemArray</span></span>

<span data-ttu-id="67d8f-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="67d8f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="67d8f-105">Erstellt eine benannte [SPropProblemArray](spropproblemarray.md) -Struktur, die eine angegebene Anzahl von [SPropProblem](spropproblem.md) Strukturen enthält.</span><span class="sxs-lookup"><span data-stu-id="67d8f-105">Creates a named [SPropProblemArray](spropproblemarray.md) structure that contains a specified number of [SPropProblem](spropproblem.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="67d8f-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="67d8f-106">Header file:</span></span>  <br/> |<span data-ttu-id="67d8f-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="67d8f-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="67d8f-108">Verwandte Struktur:</span><span class="sxs-lookup"><span data-stu-id="67d8f-108">Related structure:</span></span>  <br/> |<span data-ttu-id="67d8f-109">**SPropProblemArray**</span><span class="sxs-lookup"><span data-stu-id="67d8f-109">**SPropProblemArray**</span></span> <br/> |
   
```cpp
SizedSPropProblemArray(_cprob, _name)
```

## <a name="parameters"></a><span data-ttu-id="67d8f-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="67d8f-110">Parameters</span></span>

<span data-ttu-id="67d8f-111">__cprob_</span><span class="sxs-lookup"><span data-stu-id="67d8f-111">__cprob_</span></span>
  
> <span data-ttu-id="67d8f-112">Anzahl der **SPropProblem** Strukturen, die in die neue Struktur eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="67d8f-112">Count of **SPropProblem** structures to be included in the new structure.</span></span> 
    
<span data-ttu-id="67d8f-113">__Namen_</span><span class="sxs-lookup"><span data-stu-id="67d8f-113">__name_</span></span>
  
> <span data-ttu-id="67d8f-114">Der Name für die neue Struktur.</span><span class="sxs-lookup"><span data-stu-id="67d8f-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="67d8f-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="67d8f-115">Remarks</span></span>

<span data-ttu-id="67d8f-116">Verwenden Sie das Makro **SizedSPropProblemArray** , um ein Problem Array-Eigenschaft mit expliziten Grenzen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="67d8f-116">Use the **SizedSPropProblemArray** macro to create a property problem array with explicit bounds.</span></span> <span data-ttu-id="67d8f-117">Um die neue Struktur verwenden, die als Zeiger auf eine **SPropProblemArray** -Struktur aus dem Makro **SizedSPropProblemArray** erzeugt, führen Sie die folgende Umwandlung:</span><span class="sxs-lookup"><span data-stu-id="67d8f-117">To use the new structure that results from the **SizedSPropProblemArray** macro as a pointer to an **SPropProblemArray** structure, perform the following cast:</span></span> 
  
```cpp
lpPropProbArray = (LPSPropProblemArray) &SizedSPropProblemArray;
```

## <a name="see-also"></a><span data-ttu-id="67d8f-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="67d8f-118">See also</span></span>

- [<span data-ttu-id="67d8f-119">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="67d8f-119">SPropProblemArray</span></span>](spropproblemarray.md)
- [<span data-ttu-id="67d8f-120">SPropProblem</span><span class="sxs-lookup"><span data-stu-id="67d8f-120">SPropProblem</span></span>](spropproblem.md)
- [<span data-ttu-id="67d8f-121">Makros im Zusammenhang mit Strukturen</span><span class="sxs-lookup"><span data-stu-id="67d8f-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)
