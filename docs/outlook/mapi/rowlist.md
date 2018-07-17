---
title: ROWLIST
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ROWLIST
api_type:
- COM
ms.assetid: ce0be0d5-4962-4d53-828f-c93d1c5aae32
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: d0427e36d07d1cdc4f88e471f9ca006e737b73f2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795410"
---
# <a name="rowlist"></a><span data-ttu-id="63c8d-103">ROWLIST</span><span class="sxs-lookup"><span data-stu-id="63c8d-103">ROWLIST</span></span>

  
  
<span data-ttu-id="63c8d-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="63c8d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="63c8d-105">Enthält ein Array von [ROWENTRY](rowentry.md) -Strukturen, darstellen, Zeilen und die Vorgänge, die für die Zeilen in einer Tabelle über die Schnittstelle [IExchangeModifyTable](iexchangemodifytableiunknown.md) ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="63c8d-105">Contains an array of [ROWENTRY](rowentry.md) structures representing rows and the operations that are performed on those rows in a table through the [IExchangeModifyTable](iexchangemodifytableiunknown.md) interface.</span></span> 
  
```cpp
typedef struct
{
  ULONG     cEntries;
  ROWENTRY  aEntries[MAPI_DIM];
}  ROWLIST, FAR * LPROWLIST;

```

## <a name="members"></a><span data-ttu-id="63c8d-106">Members</span><span class="sxs-lookup"><span data-stu-id="63c8d-106">Members</span></span>

 <span data-ttu-id="63c8d-107">**cEntries**</span><span class="sxs-lookup"><span data-stu-id="63c8d-107">**cEntries**</span></span>
  
> <span data-ttu-id="63c8d-108">Anzahl der Einträge im Array vom **aEntries** Member angegeben.</span><span class="sxs-lookup"><span data-stu-id="63c8d-108">Count of entries in the array specified by the **aEntries** member.</span></span> 
    
 <span data-ttu-id="63c8d-109">**aEntries [MAPI_DIM]**</span><span class="sxs-lookup"><span data-stu-id="63c8d-109">**aEntries[MAPI_DIM]**</span></span>
  
> <span data-ttu-id="63c8d-110">Array von **ROWENTRY** -Strukturen, enthält die Zeilen und die Vorgänge, die für die Zeilen in der Tabelle ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="63c8d-110">Array of **ROWENTRY** structures that contains the rows and the operations that are performed on those rows in the table.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="63c8d-111">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="63c8d-111">MFCMAPI reference</span></span>

<span data-ttu-id="63c8d-112">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="63c8d-112">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="63c8d-113">**Datei**</span><span class="sxs-lookup"><span data-stu-id="63c8d-113">**File**</span></span>|<span data-ttu-id="63c8d-114">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="63c8d-114">**Function**</span></span>|<span data-ttu-id="63c8d-115">**Comment**</span><span class="sxs-lookup"><span data-stu-id="63c8d-115">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="63c8d-116">RulesDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="63c8d-116">RulesDlg.cpp</span></span>  <br/> |<span data-ttu-id="63c8d-117">CRulesDlg::GetSelectedItems</span><span class="sxs-lookup"><span data-stu-id="63c8d-117">CRulesDlg::GetSelectedItems</span></span>  <br/> |<span data-ttu-id="63c8d-118">Verwendet, um eine Liste der ausgewählten Regeln für nachfolgende **ModifyTable** Aktionen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="63c8d-118">Used to build a list of selected rules for subsequent **ModifyTable** actions.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="63c8d-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="63c8d-119">See also</span></span>



[<span data-ttu-id="63c8d-120">ROWENTRY</span><span class="sxs-lookup"><span data-stu-id="63c8d-120">ROWENTRY</span></span>](rowentry.md)
  
[<span data-ttu-id="63c8d-121">IExchangeModifyTable: IUnknown</span><span class="sxs-lookup"><span data-stu-id="63c8d-121">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)


[<span data-ttu-id="63c8d-122">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="63c8d-122">MAPI Structures</span></span>](mapi-structures.md)
