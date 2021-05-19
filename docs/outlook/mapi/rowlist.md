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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c13b741b1e0ddfd964b9325d736a26dac4bff2af
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419184"
---
# <a name="rowlist"></a><span data-ttu-id="c5ccb-103">ROWLIST</span><span class="sxs-lookup"><span data-stu-id="c5ccb-103">ROWLIST</span></span>

  
  
<span data-ttu-id="c5ccb-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c5ccb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c5ccb-105">Enthält ein Array von [ROWENTRY-Strukturen,](rowentry.md) die Zeilen und die Vorgänge darstellen, die für diese Zeilen in einer Tabelle über die [IExchangeModifyTable-Schnittstelle ausgeführt](iexchangemodifytableiunknown.md) werden.</span><span class="sxs-lookup"><span data-stu-id="c5ccb-105">Contains an array of [ROWENTRY](rowentry.md) structures representing rows and the operations that are performed on those rows in a table through the [IExchangeModifyTable](iexchangemodifytableiunknown.md) interface.</span></span> 
  
```cpp
typedef struct
{
  ULONG     cEntries;
  ROWENTRY  aEntries[MAPI_DIM];
}  ROWLIST, FAR * LPROWLIST;

```

## <a name="members"></a><span data-ttu-id="c5ccb-106">Elemente</span><span class="sxs-lookup"><span data-stu-id="c5ccb-106">Members</span></span>

 <span data-ttu-id="c5ccb-107">**cEntries**</span><span class="sxs-lookup"><span data-stu-id="c5ccb-107">**cEntries**</span></span>
  
> <span data-ttu-id="c5ccb-108">Anzahl der Einträge im vom **aEntries-Element angegebenen** Array.</span><span class="sxs-lookup"><span data-stu-id="c5ccb-108">Count of entries in the array specified by the **aEntries** member.</span></span> 
    
 <span data-ttu-id="c5ccb-109">**aEntries[MAPI_DIM]**</span><span class="sxs-lookup"><span data-stu-id="c5ccb-109">**aEntries[MAPI_DIM]**</span></span>
  
> <span data-ttu-id="c5ccb-110">Array von **ROWENTRY-Strukturen,** die die Zeilen und Vorgänge enthält, die für diese Zeilen in der Tabelle ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="c5ccb-110">Array of **ROWENTRY** structures that contains the rows and the operations that are performed on those rows in the table.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="c5ccb-111">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="c5ccb-111">MFCMAPI reference</span></span>

<span data-ttu-id="c5ccb-112">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="c5ccb-112">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="c5ccb-113">**Datei**</span><span class="sxs-lookup"><span data-stu-id="c5ccb-113">**File**</span></span>|<span data-ttu-id="c5ccb-114">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="c5ccb-114">**Function**</span></span>|<span data-ttu-id="c5ccb-115">**Comment**</span><span class="sxs-lookup"><span data-stu-id="c5ccb-115">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c5ccb-116">RulesDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="c5ccb-116">RulesDlg.cpp</span></span>  <br/> |<span data-ttu-id="c5ccb-117">CRulesDlg::GetSelectedItems</span><span class="sxs-lookup"><span data-stu-id="c5ccb-117">CRulesDlg::GetSelectedItems</span></span>  <br/> |<span data-ttu-id="c5ccb-118">Wird verwendet, um eine Liste ausgewählter Regeln für nachfolgende **ModifyTable-Aktionen zu** erstellen.</span><span class="sxs-lookup"><span data-stu-id="c5ccb-118">Used to build a list of selected rules for subsequent **ModifyTable** actions.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c5ccb-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c5ccb-119">See also</span></span>



[<span data-ttu-id="c5ccb-120">ROWENTRY</span><span class="sxs-lookup"><span data-stu-id="c5ccb-120">ROWENTRY</span></span>](rowentry.md)
  
[<span data-ttu-id="c5ccb-121">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c5ccb-121">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)


[<span data-ttu-id="c5ccb-122">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="c5ccb-122">MAPI Structures</span></span>](mapi-structures.md)

