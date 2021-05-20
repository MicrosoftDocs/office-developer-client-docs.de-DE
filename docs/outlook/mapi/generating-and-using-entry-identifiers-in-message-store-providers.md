---
title: Generieren und Verwenden von Eintragsbezeichnern für Nachrichtenspeicheranbieter
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0c43546a-4788-4852-bc89-d6baa4f33c94
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 005742eaaba81600be249d52e5d8098e9f286f17
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437679"
---
# <a name="generating-and-using-entry-identifiers-in-message-store-providers"></a><span data-ttu-id="f63fc-103">Generieren und Verwenden von Eintragsbezeichnern für Nachrichtenspeicheranbieter</span><span class="sxs-lookup"><span data-stu-id="f63fc-103">Generating and using entry identifiers in message store providers</span></span>

<span data-ttu-id="f63fc-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f63fc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f63fc-105">Wenn ein neuer Ordner oder eine neue Nachricht in einem Nachrichtenspeicher erstellt wird, muss der Nachrichtenspeicheranbieter diesem Objekt einen Eintragsbezeichner zuweisen, damit Clientanwendungen darauf verweisen können.</span><span class="sxs-lookup"><span data-stu-id="f63fc-105">When a new folder or message is created in a message store, the message store provider has to assign that object an entry identifier so that client applications can refer to it.</span></span> <span data-ttu-id="f63fc-106">Nachrichtenspeicheranbieter können entweder die nicht mehr vorhandenen langfristigen Eintragsbezeichner gelöschter Objekte wiederverwenden oder neue Bezeichner erstellen.</span><span class="sxs-lookup"><span data-stu-id="f63fc-106">Message store providers can either reuse the defunct long-term entry identifiers of deleted objects or create new identifiers.</span></span> <span data-ttu-id="f63fc-107">Für Nachrichtenspeicheranbieter gibt es keine Anforderung. Wenn dies jedoch möglich ist, sollte ein Nachrichtenspeicheranbieter immer neue langfristige Eintragsbezeichner für neue Objekte generieren, anstatt alte wieder zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="f63fc-107">There is no requirement one way or the other for message store providers; however, if it is feasible, a message store provider should always generate new long-term entry identifiers for new objects rather than reusing old ones.</span></span> <span data-ttu-id="f63fc-108">Es ist in Ordnung, kurzfristige Eintragsbezeichner wiederzuverwenden, wenn die Objekte, auf die sie verweisen, gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="f63fc-108">It is fine to reuse short-term entry identifiers when the objects they refer to are deleted.</span></span>
  
<span data-ttu-id="f63fc-109">Der Grund für diesen Löschvorgang ist, dass Clients Eintragsbezeichner zwischenspeichern können, manchmal über einen längeren Zeitraum.</span><span class="sxs-lookup"><span data-stu-id="f63fc-109">The reason for this deletion is that clients can cache entry identifiers, sometimes for long periods of time.</span></span> <span data-ttu-id="f63fc-110">Wenn dies der Fall ist und der Nachrichtenspeicheranbieter eintragsbezeichner wiederverwendet, kann der Eintragsbezeichner auf ein anderes Objekt verweisen, wenn der Client den Eintragsbezeichner öffnet als beim ersten Erhalten der Eintrags-ID.</span><span class="sxs-lookup"><span data-stu-id="f63fc-110">If that happens and the message store provider does reuse entry identifiers, it is possible for the entry identifier to refer to a different object when the client opens the entry identifier than when it first obtained the entry identifier.</span></span> <span data-ttu-id="f63fc-111">Wenn der Nachrichtenspeicheranbieter keine Eintragsbezeichner wiederverwendet oder zumindest ein Schema zur Generierung von Eintragsbezeichnern verwendet, das sich nicht sehr lange wiederholt, kann dieses Problem nicht auftreten.</span><span class="sxs-lookup"><span data-stu-id="f63fc-111">If the message store provider does not reuse entry identifiers — or at least uses an entry identifier generation scheme that does not repeat for a very long time — this problem cannot occur.</span></span>
  
<span data-ttu-id="f63fc-112">Auf ähnliche Weise sollten Nachrichtenspeicheranbieter versuchen, die Eintragsbezeichner für Ordner und Nachrichten zu erhalten, wenn sie im Nachrichtenspeicher verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="f63fc-112">Similarly, message store providers should attempt to preserve entry identifiers for folders and messages when they are moved in the message store.</span></span> <span data-ttu-id="f63fc-113">Wenn der Nachrichtenspeicheranbieter dies tun kann, werden Verweise auf Objekte im Speicher nicht ungültig, wenn das Objekt an einen anderen Speicherort im Speicher verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="f63fc-113">If the message store provider can do that, references to objects in the store will not become invalid when the object is moved to a different location in the store.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f63fc-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f63fc-114">See also</span></span>

- [<span data-ttu-id="f63fc-115">Nachrichtenspeicher-Features</span><span class="sxs-lookup"><span data-stu-id="f63fc-115">Message Store Features</span></span>](message-store-features.md)

