---
title: SMAPIFormInfoArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SMAPIFormInfoArray
api_type:
- COM
ms.assetid: f5eeb75d-debb-4ac1-b239-e8e852460ce0
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 6389bbf2094f51711d80896db0db9862059826cc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795587"
---
# <a name="smapiforminfoarray"></a><span data-ttu-id="d8be1-103">SMAPIFormInfoArray</span><span class="sxs-lookup"><span data-stu-id="d8be1-103">SMAPIFormInfoArray</span></span>

  
  
<span data-ttu-id="d8be1-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d8be1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d8be1-105">Enthält ein Array von Zeigern auf Formular Informationen Objekte.</span><span class="sxs-lookup"><span data-stu-id="d8be1-105">Contains an array of pointers to form information objects.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d8be1-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="d8be1-106">Header file:</span></span>  <br/> |<span data-ttu-id="d8be1-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="d8be1-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="d8be1-108">Verwandte Makro:</span><span class="sxs-lookup"><span data-stu-id="d8be1-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="d8be1-109">CbMAPIFormInfoArray</span><span class="sxs-lookup"><span data-stu-id="d8be1-109">CbMAPIFormInfoArray</span></span>](cbmapiforminfoarray.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cForms;
  LPMAPIFORMINFO aFormInfo[MAPI_DIM];
} SMAPIFormInfoArray, FAR * LPSMAPIFORMINFOARRAY;

```

## <a name="members"></a><span data-ttu-id="d8be1-110">Members</span><span class="sxs-lookup"><span data-stu-id="d8be1-110">Members</span></span>

 <span data-ttu-id="d8be1-111">**cForms**</span><span class="sxs-lookup"><span data-stu-id="d8be1-111">**cForms**</span></span>
  
> <span data-ttu-id="d8be1-112">Anzahl von Zeigern im Array, auf das Element **aFormInfo** zeigt.</span><span class="sxs-lookup"><span data-stu-id="d8be1-112">Count of pointers in the array pointed to by the **aFormInfo** member.</span></span> 
    
 <span data-ttu-id="d8be1-113">**aFormInfo**</span><span class="sxs-lookup"><span data-stu-id="d8be1-113">**aFormInfo**</span></span>
  
> <span data-ttu-id="d8be1-114">Zeiger auf ein Array von Zeigern auf Formular Informationen Objekte.</span><span class="sxs-lookup"><span data-stu-id="d8be1-114">Pointer to an array of pointers to form information objects.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d8be1-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d8be1-115">Remarks</span></span>

<span data-ttu-id="d8be1-116">Die Struktur **SMAPIFormInfoArray** wird als Parameter in der folgenden Methoden übergeben:</span><span class="sxs-lookup"><span data-stu-id="d8be1-116">The **SMAPIFormInfoArray** structure is passed as a parameter in the following methods:</span></span> 
  
- [<span data-ttu-id="d8be1-117">IMAPIFormMgr::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="d8be1-117">IMAPIFormMgr::ResolveMultipleMessageClasses</span></span>](imapiformmgr-resolvemultiplemessageclasses.md)
    
- [<span data-ttu-id="d8be1-118">IMAPIFormMgr::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="d8be1-118">IMAPIFormMgr::CalcFormPropSet</span></span>](imapiformmgr-calcformpropset.md)
    
- [<span data-ttu-id="d8be1-119">IMAPIFormMgr::SelectMultipleForms</span><span class="sxs-lookup"><span data-stu-id="d8be1-119">IMAPIFormMgr::SelectMultipleForms</span></span>](imapiformmgr-selectmultipleforms.md)
    
- [<span data-ttu-id="d8be1-120">IMAPIFormContainer::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="d8be1-120">IMAPIFormContainer::ResolveMultipleMessageClasses</span></span>](imapiformcontainer-resolvemultiplemessageclasses.md)
    
## <a name="see-also"></a><span data-ttu-id="d8be1-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d8be1-121">See also</span></span>



[<span data-ttu-id="d8be1-122">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="d8be1-122">MAPI Structures</span></span>](mapi-structures.md)
