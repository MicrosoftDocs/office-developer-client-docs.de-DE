---
title: IMAPIContainerGetSearchCriteria
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIContainer.GetSearchCriteria
api_type:
- COM
ms.assetid: 41b6c162-9984-43a3-b38e-44f0afae67de
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 13c151a134e4334e8ed2e75e031a6fc9dddbf941
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792075"
---
# <a name="imapicontainergetsearchcriteria"></a><span data-ttu-id="09848-103">IMAPIContainer::GetSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="09848-103">IMAPIContainer::GetSearchCriteria</span></span>

  
  
<span data-ttu-id="09848-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="09848-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="09848-105">Ruft die Suchkriterien für den Container an.</span><span class="sxs-lookup"><span data-stu-id="09848-105">Obtains the search criteria for the container.</span></span>
  
```cpp
HRESULT GetSearchCriteria(
  ULONG ulFlags,
  LPSRestriction FAR * lppRestriction,
  LPENTRYLIST FAR * lppContainerList,
  ULONG FAR * lpulSearchState
);
```

## <a name="parameters"></a><span data-ttu-id="09848-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="09848-106">Parameters</span></span>

 <span data-ttu-id="09848-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="09848-107">_ulFlags_</span></span>
  
> <span data-ttu-id="09848-108">[in] Eine Bitmaske aus Flags, die den Typ der übergebenen Zeichenfolgen steuert.</span><span class="sxs-lookup"><span data-stu-id="09848-108">[in] A bitmask of flags that controls the type of the passed-in strings.</span></span> <span data-ttu-id="09848-109">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="09848-109">The following flag can be set:</span></span>
    
<span data-ttu-id="09848-110">PARAMETER MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="09848-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="09848-111">Die übergebenen Zeichenfolgen sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="09848-111">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="09848-112">Wenn die Option MAPI_UNICODE nicht festgelegt ist, sind die Zeichenfolgen in ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="09848-112">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="09848-113">_lppRestriction_</span><span class="sxs-lookup"><span data-stu-id="09848-113">_lppRestriction_</span></span>
  
> <span data-ttu-id="09848-114">[out] Ein Zeiger auf einen Zeiger auf eine [SRestriction](srestriction.md) -Struktur, die die Suchkriterien definiert.</span><span class="sxs-lookup"><span data-stu-id="09848-114">[out] A pointer to a pointer to an [SRestriction](srestriction.md) structure that defines the search criteria.</span></span> <span data-ttu-id="09848-115">Wenn eine Clientanwendung NULL im Parameter _LppRestriction_ erfolgreich ist, gibt **GetSearchCriteria** keine **SRestriction** -Struktur zurück.</span><span class="sxs-lookup"><span data-stu-id="09848-115">If a client application passes NULL in the  _lppRestriction_ parameter, **GetSearchCriteria** does not return an **SRestriction** structure.</span></span> 
    
 <span data-ttu-id="09848-116">_lppContainerList_</span><span class="sxs-lookup"><span data-stu-id="09848-116">_lppContainerList_</span></span>
  
> <span data-ttu-id="09848-117">[out] Ein Zeiger auf einen Zeiger auf ein Array von Eintragsbezeichner, die Container, in die Suche einbezogen werden darstellen.</span><span class="sxs-lookup"><span data-stu-id="09848-117">[out] A pointer to a pointer to an array of entry identifiers that represent containers to be included in the search.</span></span> <span data-ttu-id="09848-118">Wenn ein Client NULL im Parameter _LppContainerList_ übergibt, gibt **GetSearchCriteria** ein Array von Eintragsbezeichner keine zurück.</span><span class="sxs-lookup"><span data-stu-id="09848-118">If a client passes NULL in the  _lppContainerList_ parameter, **GetSearchCriteria** does not return an array of entry identifiers.</span></span> 
    
 <span data-ttu-id="09848-119">_lpulSearchState_</span><span class="sxs-lookup"><span data-stu-id="09848-119">_lpulSearchState_</span></span>
  
> <span data-ttu-id="09848-120">[out] Ein Zeiger auf eine Bitmaske aus Flags verwendet, um den aktuellen Status der Suche anzugeben.</span><span class="sxs-lookup"><span data-stu-id="09848-120">[out] A pointer to a bitmask of flags used to indicate the current state of the search.</span></span> <span data-ttu-id="09848-121">Wenn ein Client NULL im Parameter _LpulSearchState_ übergibt, gibt **GetSearchCriteria** keine Flags zurück.</span><span class="sxs-lookup"><span data-stu-id="09848-121">If a client passes NULL in the  _lpulSearchState_ parameter, **GetSearchCriteria** returns no flags.</span></span> <span data-ttu-id="09848-122">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="09848-122">The following flags can be set:</span></span> 
    
<span data-ttu-id="09848-123">SEARCH_FOREGROUND</span><span class="sxs-lookup"><span data-stu-id="09848-123">SEARCH_FOREGROUND</span></span> 
  
> <span data-ttu-id="09848-124">Die Suche sollte mit hoher Priorität relativ zu anderen Suchvorgänge ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="09848-124">The search should run at high priority relative to other searches.</span></span> <span data-ttu-id="09848-125">Wenn dieses Flag nicht festgelegt ist, wird die Suche mit normaler Priorität relativ zu anderen Suchvorgänge ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="09848-125">If this flag is not set, the search runs at normal priority relative to other searches.</span></span>
    
<span data-ttu-id="09848-126">SEARCH_REBUILD</span><span class="sxs-lookup"><span data-stu-id="09848-126">SEARCH_REBUILD</span></span> 
  
> <span data-ttu-id="09848-127">Die Suche ist im Modus CPU-intensiver ihren Funktionen, die versuchen, Nachrichten zu suchen, die den Kriterien entsprechen.</span><span class="sxs-lookup"><span data-stu-id="09848-127">The search is in the CPU-intensive mode of its operation, trying to locate messages that match the criteria.</span></span> <span data-ttu-id="09848-128">Wenn dieses Flag nicht festgelegt ist, gehört die CPU-intensiver Vorgang für die Suche über.</span><span class="sxs-lookup"><span data-stu-id="09848-128">If this flag is not set, the CPU-intensive part of the search's operation is over.</span></span> <span data-ttu-id="09848-129">Dieses Kennzeichen wirkt sich nur, wenn die Suche aktiviert ist (d. h., wenn das Flag SEARCH_RUNNING festgelegt ist).</span><span class="sxs-lookup"><span data-stu-id="09848-129">This flag has meaning only if the search is active (that is, if the SEARCH_RUNNING flag is set).</span></span>
    
<span data-ttu-id="09848-130">SEARCH_RECURSIVE</span><span class="sxs-lookup"><span data-stu-id="09848-130">SEARCH_RECURSIVE</span></span> 
  
> <span data-ttu-id="09848-131">Die Suche wird in den angegebenen Container und deren untergeordnete Container für übereinstimmende Einträge suchen.</span><span class="sxs-lookup"><span data-stu-id="09848-131">The search is looking in specified containers and all their child containers for matching entries.</span></span> <span data-ttu-id="09848-132">Wenn dieses Flag nicht festgelegt ist, werden nur die explizit in den letzten Aufruf der [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) -Methode einbezogen Container durchsucht wird.</span><span class="sxs-lookup"><span data-stu-id="09848-132">If this flag is not set, only the containers explicitly included in the last call to the [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) method are being searched.</span></span> 
    
<span data-ttu-id="09848-133">SEARCH_RUNNING</span><span class="sxs-lookup"><span data-stu-id="09848-133">SEARCH_RUNNING</span></span> 
  
> <span data-ttu-id="09848-134">Die Suche ist aktiv und Inhaltstabelle des Containers wird aktualisiert, um die Änderungen im Nachrichtenspeicher oder -Adressbuch.</span><span class="sxs-lookup"><span data-stu-id="09848-134">The search is active and the container's contents table is being updated to reflect changes in the message store or address book.</span></span> <span data-ttu-id="09848-135">Wenn dieses Flag nicht festgelegt ist, wird die Suche ist deaktiviert, und der Inhaltstabelle ist statische.</span><span class="sxs-lookup"><span data-stu-id="09848-135">If this flag is not set, the search is inactive and the contents table is static.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="09848-136">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="09848-136">Return value</span></span>

<span data-ttu-id="09848-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="09848-137">S_OK</span></span> 
  
> <span data-ttu-id="09848-138">Die Suchkriterien erfolgreich abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="09848-138">The search criteria was successfully obtained.</span></span>
    
<span data-ttu-id="09848-139">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="09848-139">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="09848-140">Entweder die Option MAPI_UNICODE festgelegt wurde und die Implementierung unterstützt keine Unicode oder Parameter MAPI_UNICODE nicht festgelegt wurde und die Implementierung unterstützt nur Unicode.</span><span class="sxs-lookup"><span data-stu-id="09848-140">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="09848-141">MAPI_E_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="09848-141">MAPI_E_NOT_INITIALIZED</span></span> 
  
> <span data-ttu-id="09848-142">Nie wurden die Suchkriterien für den Container festgelegt.</span><span class="sxs-lookup"><span data-stu-id="09848-142">Search criteria were never established for the container.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="09848-143">Hinweise</span><span class="sxs-lookup"><span data-stu-id="09848-143">Remarks</span></span>

<span data-ttu-id="09848-144">Die **IMAPIContainer::GetSearchCriteria** -Methode ruft die Suchkriterien für einen Container, der sucht, in der Regel in einem Suchergebnisse Ordner unterstützt.</span><span class="sxs-lookup"><span data-stu-id="09848-144">The **IMAPIContainer::GetSearchCriteria** method obtains the search criteria for a container that supports searches, typically a search-results folder.</span></span> <span data-ttu-id="09848-145">Erstellen Sie Suchkriterien durch Aufrufen des Containers **IMAPIContainer::SetSearchCriteria** -Methode.</span><span class="sxs-lookup"><span data-stu-id="09848-145">You create search criteria by calling a container's **IMAPIContainer::SetSearchCriteria** method.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="09848-146">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="09848-146">Notes to implementers</span></span>

<span data-ttu-id="09848-147">Address Book Containern müssen möglicherweise **GetSearchCriteria** unterstützen nur, wenn die erweiterte Suche-Funktionen der Eigenschaft **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)) zugeordnet bieten.</span><span class="sxs-lookup"><span data-stu-id="09848-147">Address book containers may need to support **GetSearchCriteria** only if they provide the advanced search capabilities associated with the **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)) property.</span></span> <span data-ttu-id="09848-148">Weitere Informationen zum Implementieren die erweiterten Suchfunktion für Address Book Container, finden Sie unter [Implementieren der erweiterten Suche](implementing-advanced-searching.md).</span><span class="sxs-lookup"><span data-stu-id="09848-148">For more information about how to implement the advanced search feature for address book containers, see [Implementing Advanced Searching](implementing-advanced-searching.md).</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="09848-149">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="09848-149">Notes to callers</span></span>

<span data-ttu-id="09848-150">Wenn Sie mit den Datenstrukturen auf das durch die Parameter _LppRestriction_ und _LppContainerList_ abgeschlossen haben, rufen Sie [MAPIFreeBuffer](mapifreebuffer.md) einmal für jede Struktur freigegeben werden muss.</span><span class="sxs-lookup"><span data-stu-id="09848-150">When you are finished with the data structures pointed to by the  _lppRestriction_ and  _lppContainerList_ parameters, call [MAPIFreeBuffer](mapifreebuffer.md) once for each structure to be released.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="09848-151">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="09848-151">MFCMAPI reference</span></span>

<span data-ttu-id="09848-152">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="09848-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="09848-153">**Datei**</span><span class="sxs-lookup"><span data-stu-id="09848-153">**File**</span></span>|<span data-ttu-id="09848-154">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="09848-154">**Function**</span></span>|<span data-ttu-id="09848-155">**Comment**</span><span class="sxs-lookup"><span data-stu-id="09848-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="09848-156">HierarchyTableDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="09848-156">HierarchyTableDlg.cpp</span></span>  <br/> |<span data-ttu-id="09848-157">CHierarchyTableDlg::OnEditSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="09848-157">CHierarchyTableDlg::OnEditSearchCriteria</span></span>  <br/> |<span data-ttu-id="09848-158">MFCMAPI (engl.) verwendet die **IMAPIContainer::GetSearchCriteria** -Methode, um Suchkriterien aus einem Ordner anzuzeigenden abzurufen.</span><span class="sxs-lookup"><span data-stu-id="09848-158">MFCMAPI uses the **IMAPIContainer::GetSearchCriteria** method to obtain search criteria from a folder to display.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="09848-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="09848-159">See also</span></span>



[<span data-ttu-id="09848-160">IMAPIContainer::SetSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="09848-160">IMAPIContainer::SetSearchCriteria</span></span>](imapicontainer-setsearchcriteria.md)
  
[<span data-ttu-id="09848-161">IMAPIFolder::CreateFolder</span><span class="sxs-lookup"><span data-stu-id="09848-161">IMAPIFolder::CreateFolder</span></span>](imapifolder-createfolder.md)
  
[<span data-ttu-id="09848-162">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="09848-162">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="09848-163">Kanonische PidTagSearch-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="09848-163">PidTagSearch Canonical Property</span></span>](pidtagsearch-canonical-property.md)
  
[<span data-ttu-id="09848-164">IMAPIContainer: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="09848-164">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)


[<span data-ttu-id="09848-165">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="09848-165">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
