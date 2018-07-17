---
title: Unterst�tzung f�r benannte Eigenschaften im Nachrichtenspeicher
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a1c73bb5-b44a-4ec6-89e4-0e2228572b2d
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: b1aa0228cdc8cf6f0b2bb321e62e40127775a6de
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795666"
---
# <a name="supporting-named-properties-in-message-stores"></a><span data-ttu-id="76045-103">Unterst�tzung f�r benannte Eigenschaften im Nachrichtenspeicher</span><span class="sxs-lookup"><span data-stu-id="76045-103">Supporting Named Properties in Message Stores</span></span>

  
  
<span data-ttu-id="76045-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="76045-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="76045-p101">Message objects can have properties in them that are not in the set of properties defined by MAPI. Such properties can be unnamed or named. Unnamed properties must reside in a range of property identifiers defined by MAPI. Named custom properties reside in a different range of property identifiers defined by MAPI. They are typically used by custom message types. Your message store provider must support named properties if it is to be used as the default message store. Supporting named properties means implementing the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) and [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) methods, and implementing one or more mapping signatures that identify what names go with what property identifiers. For more information, see [Definieren von neuen MAPI-Eigenschaften](defining-new-mapi-properties.md) and [Unterst�tzung f�r benannte Eigenschaften](supporting-named-properties.md).</span><span class="sxs-lookup"><span data-stu-id="76045-p101">Message objects can have properties in them that are not in the set of properties defined by MAPI. Such properties can be unnamed or named. Unnamed properties must reside in a range of property identifiers defined by MAPI. Named custom properties reside in a different range of property identifiers defined by MAPI. They are typically used by custom message types. Your message store provider must support named properties if it is to be used as the default message store. Supporting named properties means implementing the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) and [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) methods, and implementing one or more mapping signatures that identify what names go with what property identifiers. For more information, see [Defining New MAPI Properties](defining-new-mapi-properties.md) and [Supporting Named Properties](supporting-named-properties.md).</span></span>
  
<span data-ttu-id="76045-p102">Die meisten Nachrichtenspeichers Anbieter, unterst�tzen, mit dem Namen Eigenschaften verwenden eine einzelne Zuordnung Signatur f�r alle Objekte in der Nachrichtenspeicher. Dies bietet zwei Vorteile. Erstens ist es einfacher, Zuordnung Signaturen implementieren, wenn es nur eine ist zu verfolgen. Zweitens Wenn alle Objekte in der Nachrichtenspeicher die gleiche Zuordnung Signatur verwenden, k�nnen Clientanwendungen sicher sein, dass alle Eigenschaftenbezeichner f�r Nachrichten im Nachrichtenspeicher tats�chlich auf dieselbe benannte Eigenschaft zu verweisen. Auf diese Weise k�nnen die Client-Anwendungen in ihrer Ordneransicht Spalten f�r benannte Eigenschaften anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="76045-p102">Most message store providers that support named properties use a single mapping signature for all objects in the message store. This has two benefits. First, it is simpler to implement mapping signatures if there is only one to keep track of. Second, if all objects in the message store use the same mapping signature, client applications are assured that all property identifiers on messages in the message store actually refer to the same named property. This enables client applications to display columns for named properties in their folder view interface.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="76045-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="76045-118">See also</span></span>



[<span data-ttu-id="76045-119">Implementieren von Nachrichten in Nachrichtenspeicher</span><span class="sxs-lookup"><span data-stu-id="76045-119">Implementing Messages in Message Stores</span></span>](implementing-messages-in-message-stores.md)
