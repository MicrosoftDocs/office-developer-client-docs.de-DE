---
title: Unterst�tzung von mehreren den Clientzugriff auf Nachrichten in Nachrichtenspeicher
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 31885c64-edb2-4a87-8730-09f163dedd40
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 40bed9ccbe8073c8e9ea5176c9d4be8fe642b52d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439863"
---
# <a name="supporting-multiple-client-access-to-messages-in-message-stores"></a><span data-ttu-id="71bc1-103">Unterst�tzung von mehreren den Clientzugriff auf Nachrichten in Nachrichtenspeicher</span><span class="sxs-lookup"><span data-stu-id="71bc1-103">Supporting Multiple Client Access to Messages in Message Stores</span></span>

  
  
<span data-ttu-id="71bc1-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="71bc1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="71bc1-p101">Es ist m�glich, dass mehrere Clientanwendungen, eine bestimmte Nachricht gleichzeitig zu �ffnen. Nachricht-Anbieter m�ssen keine f�hren bestimmten Regeln f�r diesen Zugriff steuern. Wenn die Client-Anwendungen �ndern Sie die Nachricht und ihre �nderungen zu speichern, sollten jedoch Speicheranbieter die folgenden Regeln entsprechen:</span><span class="sxs-lookup"><span data-stu-id="71bc1-p101">It is possible for multiple client applications to open a given message simultaneously. Message store providers do not have to follow any particular rules for governing such access. However, if the client applications modify the message and save their changes, the store provider should comply with the following rules:</span></span>
  
- <span data-ttu-id="71bc1-108">Zulassen der erste Aufruf der [IMAPIProp::SaveChanges](imapiprop-savechanges.md) -Methode, um fortzufahren, als w�re es der einzige Client, der die Nachricht ge�ffnet hat.</span><span class="sxs-lookup"><span data-stu-id="71bc1-108">Allow the first call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to proceed as if it were the only client that has the message open.</span></span> 
    
- <span data-ttu-id="71bc1-109">Die nachfolgenden **SaveChanges** Anrufe von anderen Clients sollte der Nachricht Speicheranbieter �nderungen ignorieren und MAPI_E_OBJECT_CHANGED zur�ck.</span><span class="sxs-lookup"><span data-stu-id="71bc1-109">On the subsequent **SaveChanges** calls by other clients, the message store provider should ignore the changes and return MAPI_E_OBJECT_CHANGED.</span></span> 
    
- <span data-ttu-id="71bc1-p102">Erm�glichen Sie Clientanwendungen Reaktion auf einen MAPI_E_OBJECT_CHANGED R�ckgabecode durch den aufrufenden **SaveChanges** erneut mit dem FORCE_SAVE-Flag. Wenn eine Clientanwendung dies der Fall ist, sollten vom Informationsdienst Nachricht die vorherigen �nderungen mit den neuen zu ersetzen.</span><span class="sxs-lookup"><span data-stu-id="71bc1-p102">Allow client applications to respond to a MAPI_E_OBJECT_CHANGED return code by calling **SaveChanges** again with the FORCE_SAVE flag. If a client application does this, the message store provider should replace the previous changes with the new ones.</span></span> 
    
<span data-ttu-id="71bc1-112">Alternativ kann die Nachrichtenanbieter den Konflikt zu erkennen und pr�sentieren eine Schnittstelle, die erm�glicht dem Benutzer das ausw�hlen, ob die urspr�ngliche Nachricht beibehalten, die urspr�ngliche Nachricht mit den neuen �nderungen �berschreiben oder speichern Sie die neuen �nderungen an einen anderen Speicherort.</span><span class="sxs-lookup"><span data-stu-id="71bc1-112">Alternatively, the message store provider can detect the conflict and present an interface that enables the user to choose whether to keep the original message, overwrite the original message with the new changes, or save the new changes to another location.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="71bc1-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="71bc1-113">See also</span></span>



[<span data-ttu-id="71bc1-114">Implementieren von Nachrichten in Nachrichtenspeichern</span><span class="sxs-lookup"><span data-stu-id="71bc1-114">Implementing Messages in Message Stores</span></span>](implementing-messages-in-message-stores.md)

