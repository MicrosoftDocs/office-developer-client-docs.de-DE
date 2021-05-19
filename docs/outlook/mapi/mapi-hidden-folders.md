---
title: MAPI-ausgeblendet-Ordner
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8b3b9c80-f7f4-4f37-bd6b-323469d020f1
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 9f9daa2169a087cf962d09a7c135e2829c7cd1ee
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424245"
---
# <a name="mapi-hidden-folders"></a><span data-ttu-id="1a0e9-103">MAPI-ausgeblendet-Ordner</span><span class="sxs-lookup"><span data-stu-id="1a0e9-103">MAPI Hidden Folders</span></span>

  
  
<span data-ttu-id="1a0e9-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1a0e9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1a0e9-p101">Verborgene Ordner sind generische Ordner, die Clients im Stammordner des Nachrichtenspeichers, statt die Daten in den Stammordner einer Unterstruktur zwischen Personen Nachricht (IPM) erstellen. Da diese Ordner nicht in einer IPM-Unterstruktur platziert werden, werden sie in der Regel vom Anbieter Store Nachricht aus Sicht des Benutzers ausgeblendet. Verborgene Ordner enthalten in der Regel Informationen, die f�r den Nachrichtenspeicher relevant, aber f�r den Benutzer nicht relevant ist. Clients erstellen verborgene Ordner um beispielsweise das Speichern zus�tzlicher Informationen mit dem Rest der Ordnerhierarchie gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="1a0e9-p101">Hidden folders are generic folders that clients create in the root folder of the message store, rather than in the root folder of an interpersonal message (IPM) subtree. Because these folders are not placed in an IPM subtree, they are generally hidden from the user's view by the message store provider. Hidden folders typically contain information that is relevant to the message store but irrelevant to the user. Clients create hidden folders to store, for example, additional information to be saved with the rest of the folder hierarchy.</span></span>
  
<span data-ttu-id="1a0e9-p102">MAPI erwartet, dass alle Clients anzeigen, erstellen, �ndern und L�schen von Ordnern in einer IPM-Unterstruktur m�glich. Unterst�tzung f�r das Arbeiten mit Ordnern in anderen Strukturen optional gilt. Allerdings sollten alle Nachrichtenspeicher als Standardspeicher verwendet werden kann und mit senden und Empfangen von Nachrichten k�nnen verborgene Ordner vollst�ndig unterst�tzt.</span><span class="sxs-lookup"><span data-stu-id="1a0e9-p102">MAPI expects all clients to be able to display, create, modify, and delete folders in an IPM subtree. Support for working with folders in other trees is considered optional. However, all message stores that can be used as the default store and that can send and receive messages should fully support hidden folders.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1a0e9-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1a0e9-112">See also</span></span>



[<span data-ttu-id="1a0e9-113">MAPI-Ordner</span><span class="sxs-lookup"><span data-stu-id="1a0e9-113">MAPI Folders</span></span>](mapi-folders.md)

