---
title: Implementieren von Nachrichten in Nachrichtenspeicher
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: df5003d5-cbfe-40b2-a481-e2e11dce4b3e
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: c21fea9b0c8de96f427c4bcdfabfde3a0032f0c9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792565"
---
# <a name="implementing-messages-in-message-stores"></a><span data-ttu-id="6d6d2-103">Implementieren von Nachrichten in Nachrichtenspeicher</span><span class="sxs-lookup"><span data-stu-id="6d6d2-103">Implementing Messages in Message Stores</span></span>

  
  
<span data-ttu-id="6d6d2-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6d6d2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6d6d2-p101">The [IMessage: IMAPIProp](imessageimapiprop.md) interface is similar to the [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md) interface in that both interfaces derive from the [IMAPIProp: IUnknown](imapipropiunknown.md) interface. Clients use the **IMAPIProp** methods to access the contents of a message. The **IMessage** interface supplies additional methods for manipulating messages (for example, adding attachments or modifying the recipients of a message). The methods in the **IMessage** interface modify attributes of messages that are not stored directly in the message's properties.</span><span class="sxs-lookup"><span data-stu-id="6d6d2-p101">The [IMessage : IMAPIProp](imessageimapiprop.md) interface is similar to the [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md) interface in that both interfaces derive from the [IMAPIProp : IUnknown](imapipropiunknown.md) interface. Clients use the **IMAPIProp** methods to access the contents of a message. The **IMessage** interface supplies additional methods for manipulating messages (for example, adding attachments or modifying the recipients of a message). The methods in the **IMessage** interface modify attributes of messages that are not stored directly in the message's properties.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6d6d2-109">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6d6d2-109">See also</span></span>



[<span data-ttu-id="6d6d2-110">Nachrichtenspeicher-Features</span><span class="sxs-lookup"><span data-stu-id="6d6d2-110">Message Store Features</span></span>](message-store-features.md)
