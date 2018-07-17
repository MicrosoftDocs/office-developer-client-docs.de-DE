---
title: STnefProblemArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.STnefProblemArray
api_type:
- COM
ms.assetid: 115d845b-4168-4d49-b880-219ee28baa9a
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: baa2ac2e859b42234fcb07dd2bf521424ef9b465
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795658"
---
# <a name="stnefproblemarray"></a><span data-ttu-id="b1735-103">STnefProblemArray</span><span class="sxs-lookup"><span data-stu-id="b1735-103">STnefProblemArray</span></span>

  
  
<span data-ttu-id="b1735-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b1735-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b1735-105">Enthält ein Array von **STnefProblem** -Strukturen, die eine oder mehrere Verarbeitung von Problemen, die bei der Codierung aufgetreten oder Decodierung eines Streams Transport Neutral Encapsulation Format (TNEF) beschreiben.</span><span class="sxs-lookup"><span data-stu-id="b1735-105">Contains an array of **STnefProblem** structures describing one or more processing problems that occurred during the encoding or decoding of a Transport Neutral Encapsulation Format (TNEF) stream.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b1735-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="b1735-106">Header file:</span></span>  <br/> |<span data-ttu-id="b1735-107">TNEF.h</span><span class="sxs-lookup"><span data-stu-id="b1735-107">Tnef.h</span></span>  <br/> |
   
```cpp
typedef struct _STnefProblemArray
{
  ULONG cProblem;
  STnefProblem aProblem[MAPI_DIM];
}STnefProblemArray, FAR * LPSTnefProblemArray

```

## <a name="members"></a><span data-ttu-id="b1735-108">Members</span><span class="sxs-lookup"><span data-stu-id="b1735-108">Members</span></span>

 <span data-ttu-id="b1735-109">**cProblem**</span><span class="sxs-lookup"><span data-stu-id="b1735-109">**cProblem**</span></span>
  
> <span data-ttu-id="b1735-110">Anzahl der Elemente im Array im **aProblem** -Member angegeben.</span><span class="sxs-lookup"><span data-stu-id="b1735-110">Count of elements in the array specified in the **aProblem** member.</span></span> 
    
 <span data-ttu-id="b1735-111">**aProblem**</span><span class="sxs-lookup"><span data-stu-id="b1735-111">**aProblem**</span></span>
  
> <span data-ttu-id="b1735-112">Array von Strukturen [STnefProblem](stnefproblem.md) .</span><span class="sxs-lookup"><span data-stu-id="b1735-112">Array of [STnefProblem](stnefproblem.md) structures.</span></span> <span data-ttu-id="b1735-113">Jede Struktur enthält Informationen zu einer Eigenschaft oder ein Problem bei der Verarbeitung.</span><span class="sxs-lookup"><span data-stu-id="b1735-113">Each structure contains information about a property or attribute processing problem.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="b1735-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b1735-114">Remarks</span></span>

<span data-ttu-id="b1735-115">Wenn Attribut oder Eigenschaft Verarbeitung ein Problem auftritt, wird ein Output-Parameter in der [ITnef::ExtractProps](itnef-extractprops.md) -Methode und in der [ITnef::Finish](itnef-finish.md) -Methode jedes einen Zeiger auf eine **STnefProblemArray** Struktur und **ExtractProps **und der Wert MAPI_W_ERRORS_RETURNED **Ende** jeder zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b1735-115">If a problem occurs during attribute or property processing, an output parameter in the [ITnef::ExtractProps](itnef-extractprops.md) method and in the [ITnef::Finish](itnef-finish.md) method each receive a pointer to an **STnefProblemArray** structure and **ExtractProps** and **Finish** each return the value MAPI_W_ERRORS_RETURNED.</span></span> <span data-ttu-id="b1735-116">Dieser Fehlerwert gibt an, dass ein Problem aufgetreten, während der Verarbeitung ist und eine **STnefProblemArray** -Struktur generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="b1735-116">This error value indicates that a problem arose during processing and an **STnefProblemArray** structure was generated.</span></span> 
  
<span data-ttu-id="b1735-117">Wenn eine Struktur **STnefProblem** während der Verarbeitung eines Attribut oder Eigenschaft nicht generiert wird, kann die Client-Anwendung unter der Annahme weiterhin, die die Verarbeitung dieses Attribut oder Eigenschaft erfolgreich waren.</span><span class="sxs-lookup"><span data-stu-id="b1735-117">If an **STnefProblem** structure is not generated during the processing of an attribute or property, the client application can continue under the assumption that the processing of that attribute or property succeeded.</span></span> <span data-ttu-id="b1735-118">Die einzige Ausnahme tritt auf, wenn das Problem aufgetreten ist, während der Decodierung eines Blocks Kapselung.</span><span class="sxs-lookup"><span data-stu-id="b1735-118">The only exception occurs when the problem arose during decoding of an encapsulation block.</span></span> <span data-ttu-id="b1735-119">Wenn der Fehler aufgetreten ist, während diese Decodierung, kann als die [SCODE](scode.md) in der Struktur MAPI_E_UNABLE_TO_COMPLETE zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="b1735-119">If the error occurred during this decoding, MAPI_E_UNABLE_TO_COMPLETE can be returned as the [SCODE](scode.md) in the structure.</span></span> <span data-ttu-id="b1735-120">In diesem Fall die Decodierung der die entsprechende Komponente für den Block wird angehalten und der Decodierung in einer anderen Komponente fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="b1735-120">In this case, the decoding of the component corresponding to the block is stopped and decoding is continued in another component.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b1735-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b1735-121">See also</span></span>



[<span data-ttu-id="b1735-122">STnefProblem</span><span class="sxs-lookup"><span data-stu-id="b1735-122">STnefProblem</span></span>](stnefproblem.md)
  
[<span data-ttu-id="b1735-123">SCODE</span><span class="sxs-lookup"><span data-stu-id="b1735-123">SCODE</span></span>](scode.md)


[<span data-ttu-id="b1735-124">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="b1735-124">MAPI Structures</span></span>](mapi-structures.md)
