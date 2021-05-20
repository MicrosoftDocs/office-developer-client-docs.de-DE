---
title: SBinaryArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SBinaryArray
api_type:
- COM
ms.assetid: 2d5b7302-cad2-4522-beb1-7c6c711f42e6
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 12fefbe15491837878608540006e5dd7dc3033ea
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438288"
---
# <a name="sbinaryarray"></a><span data-ttu-id="1170e-103">SBinaryArray</span><span class="sxs-lookup"><span data-stu-id="1170e-103">SBinaryArray</span></span>

  
  
<span data-ttu-id="1170e-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1170e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1170e-105">Enthält ein Array mit binären Werten.</span><span class="sxs-lookup"><span data-stu-id="1170e-105">Contains an array of binary values.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1170e-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="1170e-106">Header file:</span></span>  <br/> |<span data-ttu-id="1170e-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1170e-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SBinaryArray
{
  ULONG cValues;
  SBinary FAR *lpbin;
} SBinaryArray;

```

## <a name="members"></a><span data-ttu-id="1170e-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="1170e-108">Members</span></span>

 <span data-ttu-id="1170e-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="1170e-109">**cValues**</span></span>
  
> <span data-ttu-id="1170e-110">Anzahl der Werte im Array, auf die das **lpbin-Element** verweist.</span><span class="sxs-lookup"><span data-stu-id="1170e-110">Count of values in the array pointed to by the **lpbin** member.</span></span> 
    
 <span data-ttu-id="1170e-111">**lpbin**</span><span class="sxs-lookup"><span data-stu-id="1170e-111">**lpbin**</span></span>
  
> <span data-ttu-id="1170e-112">Zeiger auf ein Array von [SBinary-Strukturen,](sbinary.md) das die binären Werte enthält.</span><span class="sxs-lookup"><span data-stu-id="1170e-112">Pointer to an array of [SBinary](sbinary.md) structures that holds the binary values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="1170e-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1170e-113">Remarks</span></span>

<span data-ttu-id="1170e-114">Die **SBinaryArray-Struktur** wird verwendet, um Eigenschaften vom Typ PT_MV_BINARY.</span><span class="sxs-lookup"><span data-stu-id="1170e-114">The **SBinaryArray** structure is used to describe properties of type PT_MV_BINARY.</span></span> 
  
<span data-ttu-id="1170e-115">Weitere Informationen zu PT_MV_BINARY finden Sie unter [List of Property Types](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="1170e-115">For more information about PT_MV_BINARY, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1170e-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1170e-116">See also</span></span>



[<span data-ttu-id="1170e-117">SBinary</span><span class="sxs-lookup"><span data-stu-id="1170e-117">SBinary</span></span>](sbinary.md)
  
[<span data-ttu-id="1170e-118">SPropValue</span><span class="sxs-lookup"><span data-stu-id="1170e-118">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="1170e-119">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="1170e-119">MAPI Structures</span></span>](mapi-structures.md)

