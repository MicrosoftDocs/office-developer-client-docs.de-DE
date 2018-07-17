---
title: SExistRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SExistRestriction
api_type:
- COM
ms.assetid: 48d5ab42-ee70-4f6e-9184-18d22b08ea1b
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 62b5a42a540a4fb96761c45cd51c510f12225e9e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795524"
---
# <a name="sexistrestriction"></a><span data-ttu-id="b0a15-103">SExistRestriction</span><span class="sxs-lookup"><span data-stu-id="b0a15-103">SExistRestriction</span></span>

  
  
<span data-ttu-id="b0a15-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b0a15-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b0a15-105">Eine vorhanden Beschränkung der verwendet wird, um zu testen, ob eine bestimmte Eigenschaft als Spalte in der Tabelle vorhanden ist beschrieben.</span><span class="sxs-lookup"><span data-stu-id="b0a15-105">Describes an exist restriction which is used to test whether a particular property exists as a column in the table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b0a15-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="b0a15-106">Header file:</span></span>  <br/> |<span data-ttu-id="b0a15-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b0a15-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SExistRestriction
{
  ULONG ulReserved1;
  ULONG ulPropTag;
  ULONG ulReserved2;
} SExistRestriction;

```

## <a name="members"></a><span data-ttu-id="b0a15-108">Members</span><span class="sxs-lookup"><span data-stu-id="b0a15-108">Members</span></span>

 <span data-ttu-id="b0a15-109">**ulReserved1**</span><span class="sxs-lookup"><span data-stu-id="b0a15-109">**ulReserved1**</span></span>
  
> <span data-ttu-id="b0a15-110">Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="b0a15-110">Reserved; must be zero.</span></span> 
    
 <span data-ttu-id="b0a15-111">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="b0a15-111">**ulPropTag**</span></span>
  
> <span data-ttu-id="b0a15-112">Eigenschafts-Tag, identifiziert der Spalte auf Vorhandensein in jeder Zeile getestet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b0a15-112">Property tag identifying the column to be tested for existence in each row.</span></span>
    
 <span data-ttu-id="b0a15-113">**ulReserved2**</span><span class="sxs-lookup"><span data-stu-id="b0a15-113">**ulReserved2**</span></span>
  
> <span data-ttu-id="b0a15-114">Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="b0a15-114">Reserved; must be zero.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b0a15-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b0a15-115">Remarks</span></span>

<span data-ttu-id="b0a15-116">Die Einschränkung vorhanden wird verwendet, um sinnvolle Ergebnisse für andere Arten von Einschränkungen zu gewährleisten, die Eigenschaften wie-Eigenschaft und Inhalte Einschränkungen betreffen.</span><span class="sxs-lookup"><span data-stu-id="b0a15-116">The exist restriction is used to guarantee meaningful results for other types of restrictions that involve properties, such as property and content restrictions.</span></span> <span data-ttu-id="b0a15-117">Wenn eine Einschränkung, die eine Eigenschaft beinhaltet [Methode IMAPITable:: Restrict](imapitable-restrict.md) oder [IMAPITable](imapitable-findrow.md) übergeben wird, und die Eigenschaft ist nicht vorhanden, sind die Ergebnisse der Einschränkung nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="b0a15-117">When a restriction that involves a property is passed to [IMAPITable::Restrict](imapitable-restrict.md) or [IMAPITable::FindRow](imapitable-findrow.md) and the property does not exist, the results of the restriction are undefined.</span></span> <span data-ttu-id="b0a15-118">Durch das Erstellen einer **und** Einschränkung, die die eigenschaftseinschränkung mit einer Einschränkung vorhanden teilnimmt, kann ein Anrufer genaue Ergebnisse garantiert werden.</span><span class="sxs-lookup"><span data-stu-id="b0a15-118">By creating an **AND** restriction that joins the property restriction with an exist restriction, a caller can be guaranteed accurate results.</span></span> 
  
<span data-ttu-id="b0a15-119">Vorhanden Einschränkungen können nicht verwendet werden, mit der untergeordnete Objekteigenschaften, die-Typ PT_OBJECT verfügen.</span><span class="sxs-lookup"><span data-stu-id="b0a15-119">Exist restrictions cannot be used with sub-object properties that have type PT_OBJECT.</span></span> 
  
<span data-ttu-id="b0a15-120">Weitere Informationen zur Struktur **SExistRestriction** finden Sie unter [Informationen zu Einschränkungen](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="b0a15-120">For more information about the **SExistRestriction** structure, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b0a15-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b0a15-121">See also</span></span>



[<span data-ttu-id="b0a15-122">SRestriction</span><span class="sxs-lookup"><span data-stu-id="b0a15-122">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="b0a15-123">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="b0a15-123">MAPI Structures</span></span>](mapi-structures.md)
