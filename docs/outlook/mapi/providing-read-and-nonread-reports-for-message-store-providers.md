---
title: Bereitstellen von Lese- und Ungelesenberichten für Store-Anbieter
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9644b8c5-ecc0-4ea3-972a-2169c78b99e5
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 96546d3d766af398ff7acb50f4fc3a479b5668b2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432338"
---
# <a name="providing-read-and-nonread-reports-for-message-store-providers"></a><span data-ttu-id="2fab7-103">Bereitstellen von Lese- und Ungelesenberichten für Store-Anbieter</span><span class="sxs-lookup"><span data-stu-id="2fab7-103">Providing Read and Nonread Reports for Message Store Providers</span></span>

  
  
<span data-ttu-id="2fab7-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2fab7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2fab7-105">Wenn ein Nachrichtenspeicheranbieter Nachrichten empfangen kann, muss er Leseberichte und nicht gelesene Berichte von Nachrichten unterstützen, die vom Nachrichtenspeicheranbieter empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="2fab7-105">If a message store provider can receive messages, it is required to support read reports and nonread reports of messages received by the message store provider.</span></span> <span data-ttu-id="2fab7-106">Wenn eine empfangene Nachricht die **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md))-Eigenschaft enthält und der Wert dieser Eigenschaft TRUE ist, sollte der Nachrichtenspeicher eine Benachrichtigung an den Absender senden, wenn der Benutzer die Nachricht öffnet, was angibt, dass die Nachricht gelesen wurde.</span><span class="sxs-lookup"><span data-stu-id="2fab7-106">If a received message contains the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property and that property's value is TRUE, the message store should send a notification message to the sender when the user opens the message, indicating that the message has been read.</span></span> <span data-ttu-id="2fab7-107">Wenn der Benutzer die Nachricht vor dem Öffnen löscht, sollte der Nachrichtenspeicher eine Antwort an den Absender senden, die angibt, dass die Nachricht nicht gelesen wurde.</span><span class="sxs-lookup"><span data-stu-id="2fab7-107">Similarly, if the user deletes the message before opening it, the message store should issue a reply to the sender indicating that the message was not read.</span></span>
  
<span data-ttu-id="2fab7-108">Das Ausgeben dieser Berichte besteht in der Erstellung eines [IMessage : IMAPIProp-Objekts,](imessageimapiprop.md) dem Ausfüllen der relevanten Eigenschaften für die Nachricht und dem Übermitteln an den MAPI-Spooler, als ob die Nachricht mit dem Benutzer erstellt worden wäre.</span><span class="sxs-lookup"><span data-stu-id="2fab7-108">Issuing these reports is a matter of creating an [IMessage : IMAPIProp](imessageimapiprop.md) object, filling out the relevant properties on the message, and submitting it to the MAPI spooler as if the message had originated with the user.</span></span> <span data-ttu-id="2fab7-109">Dazu [kann die IMAPISupport::ReadReceipt-Methode](imapisupport-readreceipt.md) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2fab7-109">The [IMAPISupport::ReadReceipt](imapisupport-readreceipt.md) method can be used for this.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="2fab7-110">Besondere Vorsicht ist zu finden, wenn ein Nachrichtenspeicher Kopien einer ungelesenen Nachricht mit ausstehenden lese- oder nicht gelesenen Berichten macht.</span><span class="sxs-lookup"><span data-stu-id="2fab7-110">Special care must be taken when a message store makes copies of an unread message with pending read or nonread reports.</span></span> <span data-ttu-id="2fab7-111">Solche Berichte sollten nicht generiert werden, wenn Benutzer Kopien einer Nachricht lesen, für die Berichte angefordert wurden.</span><span class="sxs-lookup"><span data-stu-id="2fab7-111">Such reports should not be generated when users read any copies of a message for which reports have been requested.</span></span> <span data-ttu-id="2fab7-112">Beim Erstellen einer Kopie einer solchen Nachricht sollte der Nachrichtenspeicheranbieter die CLEAR_RN_PENDING- und CLEAR_NRN_PENDING-Flags in seine Aufrufe an [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md) und [IMessage::SetReadFlag einfügen.](imessage-setreadflag.md)</span><span class="sxs-lookup"><span data-stu-id="2fab7-112">When making a copy of such a message, the message store provider should include the CLEAR_RN_PENDING and CLEAR_NRN_PENDING flags in its calls to [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md) and [IMessage::SetReadFlag](imessage-setreadflag.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2fab7-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2fab7-113">See also</span></span>



[<span data-ttu-id="2fab7-114">Nachrichtenspeicher-Features</span><span class="sxs-lookup"><span data-stu-id="2fab7-114">Message Store Features</span></span>](message-store-features.md)

