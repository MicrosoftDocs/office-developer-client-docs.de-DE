---
title: IMAPIContainerGetHierarchyTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIContainer.GetHierarchyTable
api_type:
- COM
ms.assetid: d0c54092-86a3-47e0-8133-72e119e74b65
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: efc7f7a2fa703004afe361d766e0209ba40ffe46
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426198"
---
# <a name="imapicontainergethierarchytable"></a><span data-ttu-id="c083f-103">IMAPIContainer::GetHierarchyTable</span><span class="sxs-lookup"><span data-stu-id="c083f-103">IMAPIContainer::GetHierarchyTable</span></span>

  
  
<span data-ttu-id="c083f-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c083f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c083f-105">Gibt einen Zeiger auf die Hierarchietabelle des Containers zurück.</span><span class="sxs-lookup"><span data-stu-id="c083f-105">Returns a pointer to the container's hierarchy table.</span></span>
  
```cpp
HRESULT GetHierarchyTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="c083f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c083f-106">Parameters</span></span>

 <span data-ttu-id="c083f-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c083f-107">_ulFlags_</span></span>
  
> <span data-ttu-id="c083f-108">[in] Eine Bitmaske mit Flags, die steuert, wie Informationen in der Tabelle zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c083f-108">[in] A bitmask of flags that controls how information is returned in the table.</span></span> <span data-ttu-id="c083f-109">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="c083f-109">The following flags can be set:</span></span>
    
<span data-ttu-id="c083f-110">CONVENIENT_DEPTH</span><span class="sxs-lookup"><span data-stu-id="c083f-110">CONVENIENT_DEPTH</span></span> 
  
> <span data-ttu-id="c083f-111">Füllt die Hierarchietabelle mit Containern aus mehreren Ebenen.</span><span class="sxs-lookup"><span data-stu-id="c083f-111">Fills the hierarchy table with containers from multiple levels.</span></span> <span data-ttu-id="c083f-112">Wenn CONVENIENT_DEPTH festgelegt ist, enthält die Hierarchietabelle nur die unmittelbar untergeordneten Container des Containers.</span><span class="sxs-lookup"><span data-stu-id="c083f-112">If CONVENIENT_DEPTH is not set, the hierarchy table contains only the container's immediate child containers.</span></span>
    
<span data-ttu-id="c083f-113">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="c083f-113">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="c083f-114">**GetHierarchyTable** kann erfolgreich zurückgeben, möglicherweise bevor die Tabelle dem Aufrufer zur Verfügung steht.</span><span class="sxs-lookup"><span data-stu-id="c083f-114">**GetHierarchyTable** can return successfully, possibly before the table is made available to the caller.</span></span> <span data-ttu-id="c083f-115">Wenn die Tabelle nicht verfügbar ist, kann durch einen nachfolgenden Tabellenaufruf ein Fehler verursacht werden.</span><span class="sxs-lookup"><span data-stu-id="c083f-115">If the table is not available, making a subsequent table call can raise an error.</span></span> 
    
<span data-ttu-id="c083f-116">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c083f-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="c083f-117">Fordert an, dass die Spalten, die Zeichenfolgendaten enthalten, im Unicode-Format zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c083f-117">Requests that the columns that contain string data be returned in Unicode format.</span></span> <span data-ttu-id="c083f-118">Wenn das MAPI_UNICODE nicht festgelegt ist, sollten die Zeichenfolgen im ANSI-Format zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c083f-118">If the MAPI_UNICODE flag is not set, the strings should be returned in ANSI format.</span></span> 
    
<span data-ttu-id="c083f-119">SHOW_SOFT_DELETES</span><span class="sxs-lookup"><span data-stu-id="c083f-119">SHOW_SOFT_DELETES</span></span>
  
> <span data-ttu-id="c083f-120">Zeigt Elemente an, die derzeit als "soft deleted" gekennzeichnet sind, d. h. sie befinden sich in der Aufbewahrungszeit für gelöschte Elemente.</span><span class="sxs-lookup"><span data-stu-id="c083f-120">Shows items that are currently marked as soft deleted—that is, they are in the deleted item retention time phase.</span></span>
    
 <span data-ttu-id="c083f-121">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="c083f-121">_lppTable_</span></span>
  
> <span data-ttu-id="c083f-122">[out] Ein Zeiger auf einen Zeiger auf die Hierarchietabelle.</span><span class="sxs-lookup"><span data-stu-id="c083f-122">[out] A pointer to a pointer to the hierarchy table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c083f-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c083f-123">Return value</span></span>

<span data-ttu-id="c083f-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="c083f-124">S_OK</span></span> 
  
> <span data-ttu-id="c083f-125">Die Hierarchietabelle wurde erfolgreich abgerufen.</span><span class="sxs-lookup"><span data-stu-id="c083f-125">The hierarchy table was successfully retrieved.</span></span>
    
<span data-ttu-id="c083f-126">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="c083f-126">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="c083f-127">Entweder wurde MAPI_UNICODE-Flag festgelegt, und die Implementierung unterstützt unicode nicht, oder MAPI_UNICODE wurde nicht festgelegt, und die Implementierung unterstützt nur Unicode.</span><span class="sxs-lookup"><span data-stu-id="c083f-127">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="c083f-128">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="c083f-128">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="c083f-129">Der Container verfügt über keine untergeordneten Container und kann keine Hierarchietabelle bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="c083f-129">The container has no child containers and cannot provide a hierarchy table.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c083f-130">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c083f-130">Remarks</span></span>

<span data-ttu-id="c083f-131">Die **IMAPIContainer::GetHierarchyTable-Methode** gibt einen Zeiger auf die Hierarchietabelle eines Containers zurück.</span><span class="sxs-lookup"><span data-stu-id="c083f-131">The **IMAPIContainer::GetHierarchyTable** method returns a pointer to the hierarchy table of a container.</span></span> <span data-ttu-id="c083f-132">Eine Hierarchietabelle enthält Zusammenfassende Informationen zu den untergeordneten Containern im Container.</span><span class="sxs-lookup"><span data-stu-id="c083f-132">A hierarchy table holds summary information about the child containers in the container.</span></span> <span data-ttu-id="c083f-133">Ordnerhierarchietabellen enthalten Informationen zu Unterordnern. Adressbuchhierarchietabellen enthalten Informationen zu untergeordneten Adressbuchcontainern und Verteilerlisten.</span><span class="sxs-lookup"><span data-stu-id="c083f-133">Folder hierarchy tables hold information about subfolders; address book hierarchy tables hold information about child address book containers and distribution lists.</span></span> 
  
<span data-ttu-id="c083f-134">Es ist möglich, dass einige Container keine untergeordneten Container haben.</span><span class="sxs-lookup"><span data-stu-id="c083f-134">It is possible for some containers to have no child containers.</span></span> <span data-ttu-id="c083f-135">Diese Container geben MAPI_E_NO_SUPPORT aus ihren Implementierungen von **GetHierarchyTable zurück.**</span><span class="sxs-lookup"><span data-stu-id="c083f-135">These containers return MAPI_E_NO_SUPPORT from their implementations of **GetHierarchyTable**.</span></span>
  
<span data-ttu-id="c083f-136">Wenn das CONVENIENT_DEPTH festgelegt ist, enthält jede Zeile in der Hierarchietabelle auch die **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) -Eigenschaft als Spalte.</span><span class="sxs-lookup"><span data-stu-id="c083f-136">When the CONVENIENT_DEPTH flag is set, each row in the hierarchy table also includes the **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) property as a column.</span></span> <span data-ttu-id="c083f-137">**PR_DEPTH** gibt die Ebene der einzelnen Container relativ zum Container an, der die Tabelle implementiert.</span><span class="sxs-lookup"><span data-stu-id="c083f-137">**PR_DEPTH** indicates the level of each container relative to the container that implements the table.</span></span> <span data-ttu-id="c083f-138">Die unmittelbaren untergeordneten Container des implementierende Containers befinden sich in der Tiefe Null, untergeordnete Container in den Containern mit null Tiefe befinden sich in der ersten Tiefe und so weiter.</span><span class="sxs-lookup"><span data-stu-id="c083f-138">The implementing container's immediate child containers are at depth zero, child containers in the zero depth containers are at depth one, and so on.</span></span> <span data-ttu-id="c083f-139">Die Werte der **PR_DEPTH** werden sequentiell erhöht, wenn sich die Hierarchie der Ebenen erhöht.</span><span class="sxs-lookup"><span data-stu-id="c083f-139">The values of **PR_DEPTH** increase sequentially as the hierarchy of levels deepens.</span></span> 
  
<span data-ttu-id="c083f-140">Eine vollständige Liste der erforderlichen und optionalen Spalten in Hierarchietabellen finden Sie unter [Hierarchietabellen](hierarchy-tables.md).</span><span class="sxs-lookup"><span data-stu-id="c083f-140">For a complete list of required and optional columns in hierarchy tables, see [Hierarchy Tables](hierarchy-tables.md).</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="c083f-141">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="c083f-141">Notes to implementers</span></span>

<span data-ttu-id="c083f-142">Wenn Sie eine Hierarchietabelle für Ihren Container unterstützen, müssen Sie auch die folgenden Schritte tun:</span><span class="sxs-lookup"><span data-stu-id="c083f-142">If you support a hierarchy table for your container, you must also do the following:</span></span>
  
- <span data-ttu-id="c083f-143">Unterstützen Sie einen Aufruf der [IMAPIProp::OpenProperty-Methode](imapiprop-openproperty.md) des **Containers,** um die PR_CONTAINER_HIERARCHY ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) -Eigenschaft zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="c083f-143">Support a call to the container's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) property.</span></span>
    
- <span data-ttu-id="c083f-144">Geben **PR_CONTAINER_HIERARCHY** von einem Aufruf der [METHODEN IMAPIProp::GetPropList](imapiprop-getproplist.md) oder [IMAPIProp::GetProps](imapiprop-getprops.md) des Containers zurück.</span><span class="sxs-lookup"><span data-stu-id="c083f-144">Return **PR_CONTAINER_HIERARCHY** from a call to the container's [IMAPIProp::GetPropList](imapiprop-getproplist.md) or [IMAPIProp::GetProps](imapiprop-getprops.md) methods.</span></span> 
    
## <a name="notes-to-callers"></a><span data-ttu-id="c083f-145">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="c083f-145">Notes to callers</span></span>

<span data-ttu-id="c083f-146">Tabellenspalten mit Zeichenfolgen und binären Inhalten können abgeschnitten werden.</span><span class="sxs-lookup"><span data-stu-id="c083f-146">String and binary contents table columns can be truncated.</span></span> <span data-ttu-id="c083f-147">In der Regel geben Anbieter 255 Zeichen zurück.</span><span class="sxs-lookup"><span data-stu-id="c083f-147">Typically, providers return 255 characters.</span></span> <span data-ttu-id="c083f-148">Da Sie vorher nicht wissen können, ob eine Tabelle abgeschnittene Spalten enthält, nehmen Sie an, dass eine Spalte abgeschnitten wird, wenn die Länge der Spalte entweder 255 oder 510 Byte beträgt.</span><span class="sxs-lookup"><span data-stu-id="c083f-148">Because you cannot know beforehand whether a table includes truncated columns, assume that a column is truncated if the length of the column is either 255 or 510 bytes.</span></span> <span data-ttu-id="c083f-149">Sie können jederzeit den vollständigen Wert einer abgeschnittenen Spalte bei Bedarf direkt aus dem Objekt abrufen, indem Sie den Eintragsbezeichner zum Öffnen verwenden und dann die [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="c083f-149">You can always retrieve the full value of a truncated column, if necessary, directly from the object by using its entry identifier to open it and then calling the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> 
  
<span data-ttu-id="c083f-150">Abhängig von der Implementierung des Anbieters können Einschränkungen und Sortiervorgänge auf die gesamte Zeichenfolge oder die gekürzte Version dieser Zeichenfolge angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="c083f-150">Depending on the provider's implementation, restrictions and sorting operations can apply to the whole string or to the truncated version of that string.</span></span> <span data-ttu-id="c083f-151">Darüber hinaus ist es nicht garantiert, dass Speicheranbieter den für Hierarchietabellen angegebenen [Sortierreihenfolgensatz SSortOrderSet](ssortorderset.md) berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="c083f-151">Moreover, store providers are not guaranteed to honor the sort order set [SSortOrderSet](ssortorderset.md) specified for hierarchy tables.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="c083f-152">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="c083f-152">MFCMAPI reference</span></span>

<span data-ttu-id="c083f-153">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="c083f-153">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="c083f-154">**Datei**</span><span class="sxs-lookup"><span data-stu-id="c083f-154">**File**</span></span>|<span data-ttu-id="c083f-155">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="c083f-155">**Function**</span></span>|<span data-ttu-id="c083f-156">**Comment**</span><span class="sxs-lookup"><span data-stu-id="c083f-156">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c083f-157">HierarchyTableTreeCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="c083f-157">HierarchyTableTreeCtrl.cpp</span></span>  <br/> |<span data-ttu-id="c083f-158">CHierarchyTableTreeCtrl::GetHierarchyTable</span><span class="sxs-lookup"><span data-stu-id="c083f-158">CHierarchyTableTreeCtrl::GetHierarchyTable</span></span>  <br/> |<span data-ttu-id="c083f-159">Die CHierarchyTableTreeCtrl-Klasse verwendet **GetHierarchyTable,** um Hierarchietabellen zum Anzeigen in einem Strukturansichtssteuerelement zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="c083f-159">The CHierarchyTableTreeCtrl class uses **GetHierarchyTable** to obtain hierarchy tables to display in a tree view control.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c083f-160">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c083f-160">See also</span></span>



[<span data-ttu-id="c083f-161">IMAPIProp::GetPropList</span><span class="sxs-lookup"><span data-stu-id="c083f-161">IMAPIProp::GetPropList</span></span>](imapiprop-getproplist.md)
  
[<span data-ttu-id="c083f-162">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="c083f-162">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="c083f-163">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c083f-163">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="c083f-164">PidTagContainerHierarchy (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="c083f-164">PidTagContainerHierarchy Canonical Property</span></span>](pidtagcontainerhierarchy-canonical-property.md)
  
[<span data-ttu-id="c083f-165">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="c083f-165">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)


[<span data-ttu-id="c083f-166">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="c083f-166">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

