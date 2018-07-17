---
title: SGuidArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SGuidArray
api_type:
- COM
ms.assetid: 2091e5fc-75c8-4ea4-87e9-a9bf508e9c58
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 553ec17e9caf9bf93278ff139eb94e02e6b48554
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/15/2018
ms.locfileid: "19795528"
---
# <a name="sguidarray"></a><span data-ttu-id="3b9cf-103">SGuidArray</span><span class="sxs-lookup"><span data-stu-id="3b9cf-103">SGuidArray</span></span>

  
  
<span data-ttu-id="3b9cf-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3b9cf-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3b9cf-105">Enthält ein Array von [GUID](guid.md) -Strukturen, die verwendet werden, um eine Eigenschaft vom Typ PT_MV_CLSID beschrieben.</span><span class="sxs-lookup"><span data-stu-id="3b9cf-105">Contains an array of [GUID](guid.md) structures that are used to describe a property of type PT_MV_CLSID.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3b9cf-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="3b9cf-106">Header file:</span></span>  <br/> |<span data-ttu-id="3b9cf-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3b9cf-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SGuidArray
{
  ULONG cValues;
  GUID FAR *lpguid;
} SGuidArray;

```

## <a name="members"></a><span data-ttu-id="3b9cf-108">Members</span><span class="sxs-lookup"><span data-stu-id="3b9cf-108">Members</span></span>

 <span data-ttu-id="3b9cf-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="3b9cf-109">**cValues**</span></span>
  
> <span data-ttu-id="3b9cf-110">Anzahl der Werte im Array auf den Member **x Lpguid** zeigt.</span><span class="sxs-lookup"><span data-stu-id="3b9cf-110">Count of values in the array pointed to by the **lpguid** member.</span></span> 
    
 <span data-ttu-id="3b9cf-111">**x lpguid**</span><span class="sxs-lookup"><span data-stu-id="3b9cf-111">**lpguid**</span></span>
  
> <span data-ttu-id="3b9cf-112">Zeiger auf ein Array von **GUID** -Strukturen, die die Klasse ID-Werte enthält.</span><span class="sxs-lookup"><span data-stu-id="3b9cf-112">Pointer to an array of **GUID** structures that contains the class identifier values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="3b9cf-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3b9cf-113">Remarks</span></span>

<span data-ttu-id="3b9cf-114">Weitere Informationen zu PT_MV_CLSID finden Sie unter [Liste der Eigenschaftentypen](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="3b9cf-114">For more information about PT_MV_CLSID, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3b9cf-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3b9cf-115">See also</span></span>



[<span data-ttu-id="3b9cf-116">GUID</span><span class="sxs-lookup"><span data-stu-id="3b9cf-116">GUID</span></span>](guid.md)
  
[<span data-ttu-id="3b9cf-117">SPropValue</span><span class="sxs-lookup"><span data-stu-id="3b9cf-117">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="3b9cf-118">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="3b9cf-118">MAPI Structures</span></span>](mapi-structures.md)
