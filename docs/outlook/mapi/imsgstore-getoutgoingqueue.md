---
title: IMsgStoreGetOutgoingQueue
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.GetOutgoingQueue
api_type:
- COM
ms.assetid: 8316ff89-104d-43fd-902b-476fe567e23b
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 8ccb732dd587b2e5107290b2db7c48e85d0145d4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434151"
---
# <a name="imsgstoregetoutgoingqueue"></a><span data-ttu-id="08ea2-103">IMsgStore::GetOutgoingQueue</span><span class="sxs-lookup"><span data-stu-id="08ea2-103">IMsgStore::GetOutgoingQueue</span></span>

  
  
<span data-ttu-id="08ea2-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="08ea2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="08ea2-105">Bietet Zugriff auf die Tabelle für ausgehende Warteschlangen, eine Tabelle mit Informationen zu allen Nachrichten in der ausgehenden Warteschlange des Nachrichtenspeichers.</span><span class="sxs-lookup"><span data-stu-id="08ea2-105">Provides access to the outgoing queue table, a table that has information about all of the messages in the message store's outgoing queue.</span></span> <span data-ttu-id="08ea2-106">Diese Methode ist nur durch die MAPI-Warteschlange aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="08ea2-106">This method is called only by the MAPI spooler.</span></span>
  
```cpp
HRESULT GetOutgoingQueue(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="08ea2-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="08ea2-107">Parameters</span></span>

 <span data-ttu-id="08ea2-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="08ea2-108">_ulFlags_</span></span>
  
> <span data-ttu-id="08ea2-109">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="08ea2-109">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="08ea2-110">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="08ea2-110">_lppTable_</span></span>
  
> <span data-ttu-id="08ea2-111">[out] Ein Zeiger auf einen Zeiger auf die ausgehende Warteschlangentabelle.</span><span class="sxs-lookup"><span data-stu-id="08ea2-111">[out] A pointer to a pointer to the outgoing queue table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="08ea2-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="08ea2-112">Return value</span></span>

<span data-ttu-id="08ea2-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="08ea2-113">S_OK</span></span> 
  
> <span data-ttu-id="08ea2-114">Die Tabelle für ausgehende Warteschlangen wurde erfolgreich zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="08ea2-114">The outgoing queue table was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="08ea2-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="08ea2-115">Remarks</span></span>

<span data-ttu-id="08ea2-116">Die **IMsgStore::GetOutgoingQueue-Methode** bietet dem MAPI-Spooler Zugriff auf die Tabelle, die die Warteschlange des Nachrichtenspeichers mit ausgehenden Nachrichten zeigt.</span><span class="sxs-lookup"><span data-stu-id="08ea2-116">The **IMsgStore::GetOutgoingQueue** method provides the MAPI spooler with access to the table that shows the message store's queue of outgoing messages.</span></span> <span data-ttu-id="08ea2-117">In der Regel werden Nachrichten in der Ausgehenden Warteschlangentabelle platziert, nachdem ihre [IMessage::SubmitMessage-Methode](imessage-submitmessage.md) aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="08ea2-117">Typically, messages are placed in the outgoing queue table after their [IMessage::SubmitMessage](imessage-submitmessage.md) method is called.</span></span> <span data-ttu-id="08ea2-118">Da sich die Reihenfolge der Übermittlung jedoch auf die Reihenfolge der Vorverarbeitung und Übermittlung an den Transportanbieter auswirkt, werden einige Nachrichten, die für das Senden markiert wurden, möglicherweise nicht sofort in der Tabelle für ausgehende Warteschlangen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="08ea2-118">However, because the order of submission affects the order of preprocessing and submission to the transport provider, some messages that have been marked for sending might not appear in the outgoing queue table immediately.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="08ea2-119">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="08ea2-119">Notes to implementers</span></span>

<span data-ttu-id="08ea2-120">Eine Liste der Eigenschaften, die als Spalten in der Tabelle für ausgehende Warteschlangen enthalten sein müssen, finden Sie unter [Outgoing Queue Tables](outgoing-queue-tables.md).</span><span class="sxs-lookup"><span data-stu-id="08ea2-120">For a list of the properties that must be included as columns in your outgoing queue table, see [Outgoing Queue Tables](outgoing-queue-tables.md).</span></span> 
  
<span data-ttu-id="08ea2-121">Da der MAPI-Spooler so konzipiert ist, dass Nachrichten aus einem Nachrichtenspeicher in aufsteigender Reihenfolge der Übermittlungszeit akzeptiert werden, können Sie entweder zulassen, dass der MAPI-Spooler die ausgehende Warteschlangentabelle so sortiert, dass sie mit dieser Reihenfolge übereinstimmen kann, oder legen Sie sie als Standardsortierreihenfolge fest.</span><span class="sxs-lookup"><span data-stu-id="08ea2-121">Because the MAPI spooler is designed to accept messages from a message store in ascending order of submission time, either allow the MAPI spooler to sort the outgoing queue table to match this order or establish it as the default sort order.</span></span>
  
<span data-ttu-id="08ea2-122">Sie müssen Benachrichtigungen für die Warteschlangentabelle für ausgehende Nachrichten unterstützen, um sicherzustellen, dass der MAPI-Spooler benachrichtigt wird, wenn sich der Inhalt der Warteschlange ändert.</span><span class="sxs-lookup"><span data-stu-id="08ea2-122">You must support notifications for the outgoing message queue table, ensuring that the MAPI spooler is notified when the contents of the queue change.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="08ea2-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="08ea2-123">See also</span></span>



[<span data-ttu-id="08ea2-124">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="08ea2-124">IMessage::SubmitMessage</span></span>](imessage-submitmessage.md)
  
[<span data-ttu-id="08ea2-125">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="08ea2-125">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)

