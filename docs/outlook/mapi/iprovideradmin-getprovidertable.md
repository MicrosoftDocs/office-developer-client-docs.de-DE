---
title: IProviderAdminGetProviderTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProviderAdmin.GetProviderTable
api_type:
- COM
ms.assetid: e9deaa7c-430b-4e97-8ed6-f7c615956e0f
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 2ad57b91a1b9d06ab8284fa53c283d17e4eb5613
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792790"
---
# <a name="iprovideradmingetprovidertable"></a><span data-ttu-id="237f3-103">IProviderAdmin::GetProviderTable</span><span class="sxs-lookup"><span data-stu-id="237f3-103">IProviderAdmin::GetProviderTable</span></span>

  
  
<span data-ttu-id="237f3-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="237f3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="237f3-105">Bietet Zugriff auf den Dienst Anbieter Tabelle, eine Liste der Dienstanbieter in der Nachrichtendienst.</span><span class="sxs-lookup"><span data-stu-id="237f3-105">Provides access to the message service's provider table, a list of the service providers in the message service.</span></span>
  
```cpp
HRESULT GetProviderTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="237f3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="237f3-106">Parameters</span></span>

 <span data-ttu-id="237f3-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="237f3-107">_ulFlags_</span></span>
  
> <span data-ttu-id="237f3-108">[in] Eine Bitmaske aus Flags, die den Typ der Zeichenfolgen in der Anbieter Tabellenspalten zurückgegeben steuert.</span><span class="sxs-lookup"><span data-stu-id="237f3-108">[in] A bitmask of flags that controls the type of the strings returned in the provider table's columns.</span></span> <span data-ttu-id="237f3-109">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="237f3-109">The following flag can be set:</span></span>
    
<span data-ttu-id="237f3-110">PARAMETER MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="237f3-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="237f3-111">Die Zeichenfolgenspalten sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="237f3-111">The string columns are in Unicode format.</span></span> <span data-ttu-id="237f3-112">Wenn die Option MAPI_UNICODE nicht festgelegt ist, werden die Spalten im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="237f3-112">If the MAPI_UNICODE flag is not set, the columns are in ANSI format.</span></span>
    
 <span data-ttu-id="237f3-113">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="237f3-113">_lppTable_</span></span>
  
> <span data-ttu-id="237f3-114">[out] Ein Zeiger auf einen Zeiger auf den Anbieter-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="237f3-114">[out] A pointer to a pointer to the provider table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="237f3-115">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="237f3-115">Return value</span></span>

<span data-ttu-id="237f3-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="237f3-116">S_OK</span></span> 
  
> <span data-ttu-id="237f3-117">Die Anbieter Tabelle wurde erfolgreich zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="237f3-117">The provider table was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="237f3-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="237f3-118">Remarks</span></span>

<span data-ttu-id="237f3-119">Die **IProviderAdmin::GetProviderTable** -Methode ruft einen Zeiger auf den Dienst Anbieter Tabelle, einer Tabelle, die MAPI verwaltet, die Informationen zu jeder Dienstanbieter im Nachrichtendienst enthält.</span><span class="sxs-lookup"><span data-stu-id="237f3-119">The **IProviderAdmin::GetProviderTable** method retrieves a pointer to the message service's provider table, a table that MAPI maintains that contains information about each service provider in the message service.</span></span> 
  
<span data-ttu-id="237f3-120">Im Gegensatz zu der Provider-Tabelle zurückgegeben, die von der [IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md) -Methode kann die Provider-Tabelle **IProviderAdmin::GetProviderTable** zurückgegebene zusätzliche Zeilen enthalten, die Informationen im Zusammenhang mit mindestens einem darstellen der Dienstanbieter in der Nachrichtendienst.</span><span class="sxs-lookup"><span data-stu-id="237f3-120">Unlike the provider table returned by the [IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md) method, the provider table returned by **IProviderAdmin::GetProviderTable** may include additional rows that represent information associated with one or more of the service providers in the message service.</span></span> <span data-ttu-id="237f3-121">Diese zusätzlichen Informationen wird das Profil mit dem Schlüsselwort "Abschnitte", der die Datei "Mapisvc.inf" hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="237f3-121">This extra information is added to the profile with the "Sections" keyword of the Mapisvc.inf file.</span></span> <span data-ttu-id="237f3-122">Wenn ein Anbieter zusätzliche Profil hat, werden die **MAPIUID** Strukturen für diese Abschnitte in der Eigenschaft **PR_SERVICE_EXTRA_UIDS** ([PidTagServiceExtraUids](pidtagserviceextrauids-canonical-property.md)) gespeichert.</span><span class="sxs-lookup"><span data-stu-id="237f3-122">When a provider has extra profile sections, it stores the **MAPIUID** structures for these sections in the **PR_SERVICE_EXTRA_UIDS** ([PidTagServiceExtraUids](pidtagserviceextrauids-canonical-property.md)) property.</span></span> <span data-ttu-id="237f3-123">**PR_SERVICE_EXTRA_UIDS** wird im Abschnitt Profile Service Nachricht gespeichert.</span><span class="sxs-lookup"><span data-stu-id="237f3-123">**PR_SERVICE_EXTRA_UIDS** is saved in the message service profile section.</span></span> 
  
<span data-ttu-id="237f3-124">Anbieter, die gelöscht wurden, oder verwendet werden, doch zum Löschen markiert wurden, sind nicht in der Provider-Tabelle enthalten.</span><span class="sxs-lookup"><span data-stu-id="237f3-124">Providers that have been deleted, or are in use but have been marked for deletion, are not included in the provider table.</span></span> <span data-ttu-id="237f3-125">Provider-Tabellen sind statisch, was bedeutet, dass nachfolgende Ergänzungen oder Löschvorgänge aus den Dienst in der Tabelle nicht wiedergegeben werden.</span><span class="sxs-lookup"><span data-stu-id="237f3-125">Provider tables are static, meaning that subsequent additions to or deletions from the message service are not reflected in the table.</span></span> 
  
<span data-ttu-id="237f3-126">Wenn der Nachrichtendienst keine Anbieter ist, gibt **IProviderAdmin::GetProviderTable** eine Tabelle mit 0 (null) Zeilen und der Wert S_OK zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="237f3-126">If the message service has no providers, **IProviderAdmin::GetProviderTable** returns a table with zero rows and the S_OK return value.</span></span> 
  
<span data-ttu-id="237f3-127">Festlegen der Option MAPI_UNICODE im Parameter _UlFlags_ wirkt sich auf das Format der von den Methoden [IMAPITable::QueryColumns](imapitable-querycolumns.md) und [IMAPITable::QueryRows](imapitable-queryrows.md) zurückgegebenen Spalten aus.</span><span class="sxs-lookup"><span data-stu-id="237f3-127">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the format of the columns returned from the [IMAPITable::QueryColumns](imapitable-querycolumns.md) and [IMAPITable::QueryRows](imapitable-queryrows.md) methods.</span></span> 
  
<span data-ttu-id="237f3-128">Dieses Kennzeichen steuert auch die Eigenschaftentypen in der Sortierreihenfolge, die von der [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) -Methode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="237f3-128">This flag also controls the property types in the sort order returned by the [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) method.</span></span> 
  
<span data-ttu-id="237f3-129">Eine vollständige Liste der Spalten in der Tabelle Anbieter finden Sie unter [Provider-Tabelle](provider-tables.md).</span><span class="sxs-lookup"><span data-stu-id="237f3-129">For a complete list of the columns in the provider table, see [Provider Table](provider-tables.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="237f3-130">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="237f3-130">Notes to callers</span></span>

<span data-ttu-id="237f3-131">Rufen Sie die Zeilen einer Tabelle Anbieter in der Reihenfolge der Transport sortieren Sie die Tabelle nach der Spalte **PR_PROVIDER_ORDINAL** ([PidTagProviderOrdinal](pidtagproviderordinal-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="237f3-131">To retrieve the rows of a provider table in transport order, sort the table by the **PR_PROVIDER_ORDINAL** ([PidTagProviderOrdinal](pidtagproviderordinal-canonical-property.md)) column.</span></span> 
  
<span data-ttu-id="237f3-132">Einschränken Sie, um nur die Zeilen abrufen, die Dienstanbieter darstellen (ohne zusätzlichen Zeilen), Ihre Abruf auf die Zeilen, die den Wert in der Spalte **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) PT_ERROR haben.</span><span class="sxs-lookup"><span data-stu-id="237f3-132">To retrieve only those rows that represent service providers (without including any extra rows), limit your retrieval to the rows that have a value of PT_ERROR in their **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) column.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="237f3-133">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="237f3-133">MFCMAPI reference</span></span>

<span data-ttu-id="237f3-134">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="237f3-134">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="237f3-135">**Datei**</span><span class="sxs-lookup"><span data-stu-id="237f3-135">**File**</span></span>|<span data-ttu-id="237f3-136">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="237f3-136">**Function**</span></span>|<span data-ttu-id="237f3-137">**Comment**</span><span class="sxs-lookup"><span data-stu-id="237f3-137">**Comment**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="237f3-138">MsgServiceTableDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="237f3-138">MsgServiceTableDlg.cpp</span></span>  <br/> |<span data-ttu-id="237f3-139">CMsgServiceTableDlg::OnDisplayItem</span><span class="sxs-lookup"><span data-stu-id="237f3-139">CMsgServiceTableDlg::OnDisplayItem</span></span>  <br/> |<span data-ttu-id="237f3-140">MFCMAPI (engl.) verwendet die **IProviderAdmin::GetProviderTable** -Methode zum Abrufen der Tabelle der Anbieter in ein neues Dialogfeld gerendert werden soll.</span><span class="sxs-lookup"><span data-stu-id="237f3-140">MFCMAPI uses the **IProviderAdmin::GetProviderTable** method to get the table of providers to render in a new dialog box.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="237f3-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="237f3-141">See also</span></span>



[<span data-ttu-id="237f3-142">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="237f3-142">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)
  
[<span data-ttu-id="237f3-143">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="237f3-143">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="237f3-144">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="237f3-144">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
  
[<span data-ttu-id="237f3-145">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="237f3-145">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="237f3-146">IMsgServiceAdmin::GetProviderTable</span><span class="sxs-lookup"><span data-stu-id="237f3-146">IMsgServiceAdmin::GetProviderTable</span></span>](imsgserviceadmin-getprovidertable.md)
  
[<span data-ttu-id="237f3-147">IProviderAdmin: IUnknown</span><span class="sxs-lookup"><span data-stu-id="237f3-147">IProviderAdmin : IUnknown</span></span>](iprovideradminiunknown.md)


[<span data-ttu-id="237f3-148">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="237f3-148">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
