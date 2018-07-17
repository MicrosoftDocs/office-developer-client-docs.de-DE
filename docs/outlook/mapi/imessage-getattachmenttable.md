---
title: IMessageGetAttachmentTable
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMessage.GetAttachmentTable
api_type:
- COM
ms.assetid: e568917e-6085-4094-8728-89ba90a78c40
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 275dc17a141f1c002f62a43824174458e591d4de
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792512"
---
# <a name="imessagegetattachmenttable"></a><span data-ttu-id="9f71f-103">IMessage::GetAttachmentTable</span><span class="sxs-lookup"><span data-stu-id="9f71f-103">IMessage::GetAttachmentTable</span></span>

  
  
<span data-ttu-id="9f71f-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9f71f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9f71f-105">Gibt die Nachricht Anlagentabelle zurück.</span><span class="sxs-lookup"><span data-stu-id="9f71f-105">Returns the message's attachment table.</span></span>
  
```cpp
HRESULT GetAttachmentTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="9f71f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9f71f-106">Parameters</span></span>

 <span data-ttu-id="9f71f-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9f71f-107">_ulFlags_</span></span>
  
> <span data-ttu-id="9f71f-108">[in] Bitmaske aus Flags, die zur Erstellung der Tabelle beziehen.</span><span class="sxs-lookup"><span data-stu-id="9f71f-108">[in] Bitmask of flags that relate to the creation of the table.</span></span> <span data-ttu-id="9f71f-109">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="9f71f-109">The following flag can be set:</span></span> 
    
<span data-ttu-id="9f71f-110">PARAMETER MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="9f71f-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="9f71f-111">Die Zeichenfolgenspalten sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="9f71f-111">The string columns are in Unicode format.</span></span> <span data-ttu-id="9f71f-112">Wenn die Option MAPI_UNICODE nicht festgelegt ist, werden die Zeichenfolgenspalten im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="9f71f-112">If the MAPI_UNICODE flag is not set, the string columns are in ANSI format.</span></span>
    
<span data-ttu-id="9f71f-113">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="9f71f-113">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="9f71f-114">Ermöglicht **GetAttachmentTable** erfolgreich, möglicherweise beendet, bevor die Tabelle vollständig an den aufrufenden Client verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="9f71f-114">Allows **GetAttachmentTable** to return successfully, possibly before the table is fully available to the calling client.</span></span> <span data-ttu-id="9f71f-115">Wenn die Tabelle nicht verfügbar ist, kann nachfolgende anrufen darauf verursacht einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="9f71f-115">If the table is not available, making a subsequent call to it can cause an error.</span></span> 
    
 <span data-ttu-id="9f71f-116">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="9f71f-116">_lppTable_</span></span>
  
> <span data-ttu-id="9f71f-117">[out] Zeiger auf einen Zeiger auf die Anlagentabelle.</span><span class="sxs-lookup"><span data-stu-id="9f71f-117">[out] Pointer to a pointer to the attachment table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9f71f-118">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="9f71f-118">Return value</span></span>

<span data-ttu-id="9f71f-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="9f71f-119">S_OK</span></span> 
  
> <span data-ttu-id="9f71f-120">Die Anlagentabelle wurde erfolgreich abgerufen.</span><span class="sxs-lookup"><span data-stu-id="9f71f-120">The attachment table was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9f71f-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9f71f-121">Remarks</span></span>

<span data-ttu-id="9f71f-122">Die **IMessage::GetAttachmentTable** -Methode gibt einen Zeiger auf die Nachricht Anlagentabelle, die Informationen zu allen Anlagen in der Nachricht enthält.</span><span class="sxs-lookup"><span data-stu-id="9f71f-122">The **IMessage::GetAttachmentTable** method returns a pointer to the message's attachment table, which includes information about all of the attachments in the message.</span></span> <span data-ttu-id="9f71f-123">Clients erhalten Zugriff auf eine Anlage nur über die Anlagentabelle.</span><span class="sxs-lookup"><span data-stu-id="9f71f-123">Clients can get access to an attachment only through the attachment table.</span></span> <span data-ttu-id="9f71f-124">Durch Abrufen einer Anlage Anzahl seiner **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md))-Eigenschaft ein Client verschiedenen **IMessage** -Methoden können Sie die Anlage entwickelt.</span><span class="sxs-lookup"><span data-stu-id="9f71f-124">By retrieving an attachment's number its **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property a client can use several of the **IMessage** methods to work with the attachment.</span></span> 
  
<span data-ttu-id="9f71f-125">Es wird eine Zeile für jede Anlage.</span><span class="sxs-lookup"><span data-stu-id="9f71f-125">There is one row for each attachment.</span></span> <span data-ttu-id="9f71f-126">Eine vollständige Liste der Spalten in einer Anlagentabelle finden Sie unter [Anhang Tabellen](attachment-tables.md).</span><span class="sxs-lookup"><span data-stu-id="9f71f-126">For a complete list of the columns in an attachment table, see [Attachment Tables](attachment-tables.md).</span></span>
  
<span data-ttu-id="9f71f-127">Eine Anlage wird in der Anlagentabelle in der Regel nicht angezeigt, bis die Anlage und die Nachricht mit einem Aufruf von [IMAPIProp::SaveChanges](imapiprop-savechanges.md)gespeichert wurden.</span><span class="sxs-lookup"><span data-stu-id="9f71f-127">An attachment usually does not appear in the attachment table until both the attachment and the message have been saved with a call to [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span></span> <span data-ttu-id="9f71f-128">Anlagentabellen sind dynamisch.</span><span class="sxs-lookup"><span data-stu-id="9f71f-128">Attachment tables are dynamic.</span></span> <span data-ttu-id="9f71f-129">Wenn ein Client eine neue Anlage erstellt, eine vorhandene Anlage löscht oder eine oder mehrere Eigenschaften geändert, sobald die **SaveChanges** -Ruft die Anlage der Nachricht vorgenommen wurden, wird die Anlagentabelle, um die neuen Informationen aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="9f71f-129">If a client creates a new attachment, deletes an existing attachment, or changes one or more properties once the **SaveChanges** calls have been made on the attachment on the message, the attachment table will be updated to reflect the new information.</span></span> 
  
<span data-ttu-id="9f71f-130">Einige Anlagentabellen unterstützt eine Vielzahl von Einschränkungen. andere nicht.</span><span class="sxs-lookup"><span data-stu-id="9f71f-130">Some attachment tables support a wide variety of restrictions; others do not.</span></span> <span data-ttu-id="9f71f-131">Unterstützung für Einschränkungen hängt von der Nachricht Informationsdienst Implementierung ab.</span><span class="sxs-lookup"><span data-stu-id="9f71f-131">Support for restrictions depends on the message store provider's implementation.</span></span> 
  
<span data-ttu-id="9f71f-132">Beim ersten Öffnen, werden die Anlagentabellen nicht unbedingt in einer bestimmten Reihenfolge sortiert.</span><span class="sxs-lookup"><span data-stu-id="9f71f-132">When initially opened, attachment tables are not necessarily sorted in any particular order.</span></span> 
  
<span data-ttu-id="9f71f-133">Festlegen der Option MAPI_UNICODE im Parameter _UlFlags_ wirkt sich auf die folgenden Aufrufe an die Anlagentabelle aus:</span><span class="sxs-lookup"><span data-stu-id="9f71f-133">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the following calls to the attachment table:</span></span> 
  
- <span data-ttu-id="9f71f-134">[IMAPITable::QueryColumns](imapitable-querycolumns.md) zum Abrufen der Spalte festlegen.</span><span class="sxs-lookup"><span data-stu-id="9f71f-134">[IMAPITable::QueryColumns](imapitable-querycolumns.md) to retrieve the column set.</span></span> 
    
- <span data-ttu-id="9f71f-135">[IMAPITable::QueryRows](imapitable-queryrows.md) abzurufenden Zeilen.</span><span class="sxs-lookup"><span data-stu-id="9f71f-135">[IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve rows.</span></span> 
    
- <span data-ttu-id="9f71f-136">[IMAPITable::QuerySortOrder](imapitable-querysortorder.md) , um die Sortierreihenfolge abzurufen.</span><span class="sxs-lookup"><span data-stu-id="9f71f-136">[IMAPITable::QuerySortOrder](imapitable-querysortorder.md) to retrieve the sort order.</span></span> 
    
<span data-ttu-id="9f71f-137">Durch Festlegen der Unicode-Flag-Anforderungen, die die Informationen für alle diese aufrufen zurückgegebenen Zeichenfolgenspalten im Unicode-Format sein.</span><span class="sxs-lookup"><span data-stu-id="9f71f-137">Setting the Unicode flag requests that the information for any string columns returned from these calls be in Unicode format.</span></span> <span data-ttu-id="9f71f-138">Da nicht alle Nachricht Anbieter Unicode unterstützen, ist jedoch festlegen dieses Flag nur eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="9f71f-138">However, because not all message store providers support Unicode, setting this flag is only a request.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9f71f-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9f71f-139">See also</span></span>



[<span data-ttu-id="9f71f-140">IMessage::CreateAttach</span><span class="sxs-lookup"><span data-stu-id="9f71f-140">IMessage::CreateAttach</span></span>](imessage-createattach.md)
  
[<span data-ttu-id="9f71f-141">IMessage::DeleteAttach</span><span class="sxs-lookup"><span data-stu-id="9f71f-141">IMessage::DeleteAttach</span></span>](imessage-deleteattach.md)
  
[<span data-ttu-id="9f71f-142">IMessage::OpenAttach</span><span class="sxs-lookup"><span data-stu-id="9f71f-142">IMessage::OpenAttach</span></span>](imessage-openattach.md)
  
[<span data-ttu-id="9f71f-143">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="9f71f-143">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)
