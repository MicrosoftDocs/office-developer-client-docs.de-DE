---
title: IMAPISessionCompareEntryIDs
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.CompareEntryIDs
api_type:
- COM
ms.assetid: 319f10e9-db8d-4d16-aa1f-6cf5fef493eb
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: df6347298aab5404ec69bd9ac876863e31b741d0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792321"
---
# <a name="imapisessioncompareentryids"></a><span data-ttu-id="4bd50-103">IMAPISession::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="4bd50-103">IMAPISession::CompareEntryIDs</span></span>

  
  
<span data-ttu-id="4bd50-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4bd50-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4bd50-105">Vergleicht zwei Eintragsbezeichner, um zu bestimmen, ob sie sich auf dasselbe Objekt verweisen.</span><span class="sxs-lookup"><span data-stu-id="4bd50-105">Compares two entry identifiers to determine whether they refer to the same object.</span></span> 
  
```cpp
HRESULT CompareEntryIDs(
  ULONG cbEntryID1,
  LPENTRYID lpEntryID1,
  ULONG cbEntryID2,
  LPENTRYID lpEntryID2,
  ULONG ulFlags,
  ULONG FAR * lpulResult
);
```

## <a name="parameters"></a><span data-ttu-id="4bd50-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4bd50-106">Parameters</span></span>

 <span data-ttu-id="4bd50-107">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="4bd50-107">_cbEntryID1_</span></span>
  
> <span data-ttu-id="4bd50-108">[in] Die Byteanzahl von in die Eintrags-ID auf den durch den Parameter _lpEntryID1_ verwiesen.</span><span class="sxs-lookup"><span data-stu-id="4bd50-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID1_ parameter.</span></span> 
    
 <span data-ttu-id="4bd50-109">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="4bd50-109">_lpEntryID1_</span></span>
  
> <span data-ttu-id="4bd50-110">[in] Ein Zeiger auf die erste Eintrags-ID, die verglichen werden.</span><span class="sxs-lookup"><span data-stu-id="4bd50-110">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="4bd50-111">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="4bd50-111">_cbEntryID2_</span></span>
  
> <span data-ttu-id="4bd50-112">[in] Die Byteanzahl von in die Eintrags-ID auf den durch den Parameter _lpEntryID2_ verwiesen.</span><span class="sxs-lookup"><span data-stu-id="4bd50-112">[in] The byte count in the entry identifier pointed to by the  _lpEntryID2_ parameter.</span></span> 
    
 <span data-ttu-id="4bd50-113">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="4bd50-113">_lpEntryID2_</span></span>
  
> <span data-ttu-id="4bd50-114">[in] Ein Zeiger auf die zweite Eintrags-ID, die verglichen werden.</span><span class="sxs-lookup"><span data-stu-id="4bd50-114">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="4bd50-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4bd50-115">_ulFlags_</span></span>
  
> <span data-ttu-id="4bd50-116">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="4bd50-116">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="4bd50-117">_lpulResult_</span><span class="sxs-lookup"><span data-stu-id="4bd50-117">_lpulResult_</span></span>
  
> <span data-ttu-id="4bd50-118">[out] Ein Zeiger auf das Ergebnis des Vergleichs.</span><span class="sxs-lookup"><span data-stu-id="4bd50-118">[out] A pointer to the result of the comparison.</span></span> <span data-ttu-id="4bd50-119">True, wenn die zwei-Eintragsbezeichner auf dasselbe Objekt verweisen. andernfalls, FALSE.</span><span class="sxs-lookup"><span data-stu-id="4bd50-119">TRUE if the two entry identifiers refer to the same object; otherwise, FALSE.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4bd50-120">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="4bd50-120">Return value</span></span>

<span data-ttu-id="4bd50-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="4bd50-121">S_OK</span></span> 
  
> <span data-ttu-id="4bd50-122">Der Vergleich war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="4bd50-122">The comparison was successful.</span></span>
    
<span data-ttu-id="4bd50-123">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="4bd50-123">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="4bd50-124">Eine oder beide der als Parameter angegebenen Eintrags-IDs verweisen für Objekte, möglicherweise nicht, da diese Objekte derzeit nicht geöffneten und nicht verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="4bd50-124">One or both of the entry identifiers specified as parameters do not refer to objects, possibly because these objects are currently unopened and unavailable.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4bd50-125">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4bd50-125">Remarks</span></span>

<span data-ttu-id="4bd50-126">Die **IMAPISession::CompareEntryIDs** -Methode vergleicht zwei Eintragsbezeichner, die mit einem einzelnen Dienstanbieter zu bestimmen, ob sie sich auf dasselbe Objekt verweisen gehören.</span><span class="sxs-lookup"><span data-stu-id="4bd50-126">The **IMAPISession::CompareEntryIDs** method compares two entry identifiers that belong to a single service provider to determine whether they refer to the same object.</span></span> <span data-ttu-id="4bd50-127">MAPI extrahiert den [MAPIUID](mapiuid.md) Teil aus der Eintragsbezeichner bestimmen den Dienstanbieter verantwortlich für die Objekte und ruft dann **die Anmeldung des Objekts-Eintragsbezeichner zum Durchführen des Vergleichs** .</span><span class="sxs-lookup"><span data-stu-id="4bd50-127">MAPI extracts the [MAPIUID](mapiuid.md) portion from the entry identifiers to determine the service provider responsible for the objects and then calls its logon object's **CompareEntryIDs** method to perform the comparison.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="4bd50-128">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="4bd50-128">Notes to callers</span></span>

<span data-ttu-id="4bd50-129">**CompareEntryIDs** -Methode ist nützlich, da ein Objekt mehr als eine gültige Eingabe Bezeichner haben kann.</span><span class="sxs-lookup"><span data-stu-id="4bd50-129">The **CompareEntryIDs** method is useful because an object can have more than one valid entry identifier.</span></span> <span data-ttu-id="4bd50-130">Dies kann beispielsweise vorkommen, nach der Installation einer neuen Version von einem Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="4bd50-130">This situation can occur, for example, after a new version of a service provider is installed.</span></span> 
  
<span data-ttu-id="4bd50-131">Wenn **CompareEntryIDs** einen Fehler zurückgibt, führen Sie keine Aktion basierend auf dem Ergebnis des Vergleichs.</span><span class="sxs-lookup"><span data-stu-id="4bd50-131">If **CompareEntryIDs** returns an error, do not take any action based on the result of the comparison.</span></span> <span data-ttu-id="4bd50-132">In diesem Fall sollten Sie am häufigsten konservative Methode möglich.</span><span class="sxs-lookup"><span data-stu-id="4bd50-132">Instead, take the most conservative approach possible.</span></span> <span data-ttu-id="4bd50-133">**CompareEntryIDs** können Fehler auftreten, wenn Sie beispielsweise eine oder beide der Eintragsbezeichner eine ungültige **MAPIUID**enthalten.</span><span class="sxs-lookup"><span data-stu-id="4bd50-133">**CompareEntryIDs** might fail if, for example, one or both of the entry identifiers contain an invalid **MAPIUID**.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="4bd50-134">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="4bd50-134">MFCMAPI reference</span></span>

<span data-ttu-id="4bd50-135">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="4bd50-135">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="4bd50-136">**Datei**</span><span class="sxs-lookup"><span data-stu-id="4bd50-136">**File**</span></span>|<span data-ttu-id="4bd50-137">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="4bd50-137">**Function**</span></span>|<span data-ttu-id="4bd50-138">**Comment**</span><span class="sxs-lookup"><span data-stu-id="4bd50-138">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4bd50-139">BaseDialog.cpp</span><span class="sxs-lookup"><span data-stu-id="4bd50-139">BaseDialog.cpp</span></span>  <br/> |<span data-ttu-id="4bd50-140">CbaseDialog::OnCompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="4bd50-140">CbaseDialog::OnCompareEntryIDs</span></span>  <br/> |<span data-ttu-id="4bd50-141">MFCMAPI (engl.) verwendet die **IMAPISession::CompareEntryIDs** -Methode zum Vergleichen von zwei Eintrags-ID, die ein Benutzer eingibt.</span><span class="sxs-lookup"><span data-stu-id="4bd50-141">MFCMAPI uses the **IMAPISession::CompareEntryIDs** method to compare two entry IDs that a user enters.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4bd50-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4bd50-142">See also</span></span>



[<span data-ttu-id="4bd50-143">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="4bd50-143">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="4bd50-144">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="4bd50-144">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="4bd50-145">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="4bd50-145">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
