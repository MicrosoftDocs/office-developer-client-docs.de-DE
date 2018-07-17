---
title: Unterstützung für Suchvorgänge in Nachrichtenspeicher Anbietern
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 30a3fe28-31ca-4eb8-9353-f75f6d339dc7
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 0cd8bbe14e6af020ec5c93cd46a24853d1c8401c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795679"
---
# <a name="supporting-searches-in-message-store-providers"></a><span data-ttu-id="1fc98-103">Unterstützung für Suchvorgänge in Nachrichtenspeicher Anbietern</span><span class="sxs-lookup"><span data-stu-id="1fc98-103">Supporting Searches in Message Store Providers</span></span>

  
  
<span data-ttu-id="1fc98-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1fc98-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1fc98-105">Clientanwendungen weisen häufig einige Benutzeroberflächenkomponenten für die Suche nach Nachrichten in einem Nachrichtenspeicher.</span><span class="sxs-lookup"><span data-stu-id="1fc98-105">Client applications frequently have some user interface components devoted to searching for messages in a message store.</span></span> <span data-ttu-id="1fc98-106">Suchkriterien in angegeben sind die [IMAPIContainer: IMAPIProp](imapicontainerimapiprop.md) Schnittstelle mithilfe der Methoden [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) und [IMAPIContainer::GetSearchCriteria](imapicontainer-getsearchcriteria.md) .</span><span class="sxs-lookup"><span data-stu-id="1fc98-106">Search criteria are specified in the [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md) interface by means of the [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) and [IMAPIContainer::GetSearchCriteria](imapicontainer-getsearchcriteria.md) methods.</span></span> 
  
<span data-ttu-id="1fc98-107">Clients verwenden die Nachricht Store-Objekt **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md))-Eigenschaft, um den Stammordner des Nachrichtenspeichers zu identifizieren, die Ordnern für die Suchergebnisse.</span><span class="sxs-lookup"><span data-stu-id="1fc98-107">Clients use the message store object's **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)) property to identify the root folder in the message store that contains folders for search results.</span></span> <span data-ttu-id="1fc98-108">Der Suchergebnisse Ordner ist häufig ein Ordner auf der obersten Ebene des Nachrichtenspeichers, die nicht Teil der Ordnerstruktur IPM und daher ausgeblendet ist.</span><span class="sxs-lookup"><span data-stu-id="1fc98-108">The search-results folder is often a folder at the top level of the message store that is not part of the IPM folder tree and is, therefore, hidden.</span></span>
  
<span data-ttu-id="1fc98-109">Ob Ihre Nachricht Speicheranbieter einen permanenten Suchergebnisse Ordner verwendet oder einen, erstellt Wenn ein Client die Eintrags-ID in der Eigenschaft **PR_FINDER_ENTRYID** gespeicherten öffnet ist ein Implementierungsdetail.</span><span class="sxs-lookup"><span data-stu-id="1fc98-109">Whether your message store provider uses a permanent search-results folder or creates one when a client opens the entry identifier stored in the **PR_FINDER_ENTRYID** property is an implementation detail.</span></span> <span data-ttu-id="1fc98-110">Es ist leichter für Ihre Nachricht Speicheranbieter, einen permanenten Ordner zu verwenden, die erstellt wird, wenn der Nachrichtenspeicher erstellt wurde, da dadurch so vermieden wird, überprüfen Sie die Eintrags-ID, sobald ein beliebiger Ordner geöffnet wird, um festzustellen, ob erstellt die Schwierigkeit ein Suchergebnisse Ordner.</span><span class="sxs-lookup"><span data-stu-id="1fc98-110">It is somewhat easier for your message store provider to use a permanent folder that is created when the message store is created, because doing so avoids the complication of checking the entry identifier whenever any folder is opened to see whether to create a search-results folder.</span></span> <span data-ttu-id="1fc98-111">Nachricht nicht alle Anbieter können, die jedoch tun. insbesondere, schreibgeschützten Nachrichtenspeicher Speicher, die über einen MAPI-Schnittstelle mit einer Vorversion Datenbank häufig bereitgestellt sind nicht zulässig oder können nicht auf einen Ordner permanent Suchergebnisse in die zugrunde liegende Speichermechanismus zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="1fc98-111">However, not all message store providers can do that; notably, read-only message stores or stores that provide a MAPI interface to a legacy database often are not allowed or are unable to create a permanent search-results folder in the underlying storage mechanism.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1fc98-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1fc98-112">See also</span></span>



[<span data-ttu-id="1fc98-113">Nachrichtenspeicher-Features</span><span class="sxs-lookup"><span data-stu-id="1fc98-113">Message Store Features</span></span>](message-store-features.md)
