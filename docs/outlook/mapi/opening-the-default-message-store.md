---
title: Öffnen die Standard-Informationsspeicher
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 670fb896-9aaf-4a96-83f7-76237409e956
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 1eb4e150be68ea01060c7afaed489c8759b576db
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793294"
---
# <a name="opening-the-default-message-store"></a><span data-ttu-id="b6afa-103">Öffnen die Standard-Informationsspeicher</span><span class="sxs-lookup"><span data-stu-id="b6afa-103">Opening the default message store</span></span>

<span data-ttu-id="b6afa-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b6afa-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b6afa-105">In einer bestimmten Sitzung verhält sich eine Nachrichtenspeicher als Standard-Informationsspeicher.</span><span class="sxs-lookup"><span data-stu-id="b6afa-105">In any particular session, one message store acts as the default message store.</span></span> <span data-ttu-id="b6afa-106">Ein Standardnachrichtenspeicher weist folgende Merkmale auf:</span><span class="sxs-lookup"><span data-stu-id="b6afa-106">A default message store has the following characteristics:</span></span>
  
- <span data-ttu-id="b6afa-107">Die **PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md))-Eigenschaft ist auf TRUE festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b6afa-107">The **PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md)) property is set to TRUE.</span></span>
    
- <span data-ttu-id="b6afa-108">Das Flag STATUS_DEFAULT_STORE ist in der Eigenschaft **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b6afa-108">The STATUS_DEFAULT_STORE flag is set in the **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) property.</span></span>
    
- <span data-ttu-id="b6afa-109">MAPI erstellt automatisch IPM-Unterstruktur und den Stammordner für Suchergebnisse, allgemeine und persönliche Ansichten, wenn der Nachrichtenspeicher geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="b6afa-109">MAPI automatically creates the IPM subtree and the root folders for search-results, common views and personal views when the message store is opened.</span></span> <span data-ttu-id="b6afa-110">Weitere Informationen zu diesen Ordnern finden Sie unter [IPM-Unterstruktur](ipm-subtree.md) und [MAPI-Spezialordner](mapi-special-folders.md).</span><span class="sxs-lookup"><span data-stu-id="b6afa-110">For more information about these folders, see [IPM Subtree](ipm-subtree.md) and [MAPI Special Folders](mapi-special-folders.md).</span></span> 
    
<span data-ttu-id="b6afa-111">Um die Eintrags-ID für den standardmäßigen Nachrichtenspeicher abzurufen, müssen Sie [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) zum Öffnen Sie die Nachricht Store Tabelle und anwenden eine angemessene Einschränkung in einem Aufruf von [HrQueryAllRows](hrqueryallrows.md)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="b6afa-111">To retrieve the entry identifier for the default message store, you must call [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) to open the message store table and apply an appropriate restriction in a call to [HrQueryAllRows](hrqueryallrows.md).</span></span> <span data-ttu-id="b6afa-112">**HrQueryAllRows** gibt ein Rowset mit der eine Zeile, die Standard-Informationsspeicher darstellt, zurück.</span><span class="sxs-lookup"><span data-stu-id="b6afa-112">**HrQueryAllRows** will return a row set with the one row that represents the default message store.</span></span> <span data-ttu-id="b6afa-113">Die Einschränkung, die an **HrQueryAllRows** übergeben kann eine der folgenden Formen annehmen:</span><span class="sxs-lookup"><span data-stu-id="b6afa-113">The restriction that you pass to **HrQueryAllRows** can take on one of the following forms:</span></span> 
  
1. <span data-ttu-id="b6afa-114">Eine **AND** -Einschränkung, die eine **SAndRestriction** Struktur verwendet, um zu kombinieren:</span><span class="sxs-lookup"><span data-stu-id="b6afa-114">An **AND** restriction that uses an **SAndRestriction** structure to combine:</span></span> 
    
   - <span data-ttu-id="b6afa-115">Eine Einschränkung, die eine **SExistRestriction** -Struktur So testen Sie das Vorhandensein der **PR_DEFAULT_STORE** -Eigenschaft verwendet vorhanden.</span><span class="sxs-lookup"><span data-stu-id="b6afa-115">An exists restriction that uses an **SExistRestriction** structure to test for the existence of the **PR_DEFAULT_STORE** property.</span></span> 
    
   - <span data-ttu-id="b6afa-116">Eine eigenschaftseinschränkung, die eine [SPropertyRestriction](spropertyrestriction.md) -Struktur zum Überprüfen der Wert "TRUE" in der **PR_DEFAULT_STORE** -Eigenschaft verwendet.</span><span class="sxs-lookup"><span data-stu-id="b6afa-116">A property restriction that uses an [SPropertyRestriction](spropertyrestriction.md) structure to check for the TRUE value in the **PR_DEFAULT_STORE** property.</span></span> 
    
2. <span data-ttu-id="b6afa-117">Eine Bitmaske Einschränkung, die eine [SBitMaskRestriction](sbitmaskrestriction.md) -Struktur für die Anwendung STATUS_DEFAULT_STORE als Maske gegen die **PR_RESOURCE_FLAGS** -Eigenschaft verwendet.</span><span class="sxs-lookup"><span data-stu-id="b6afa-117">A bitmask restriction that uses an [SBitMaskRestriction](sbitmaskrestriction.md) structure for applying STATUS_DEFAULT_STORE as a mask against the **PR_RESOURCE_FLAGS** property.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="b6afa-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b6afa-118">See also</span></span>

- [<span data-ttu-id="b6afa-119">SExistRestriction</span><span class="sxs-lookup"><span data-stu-id="b6afa-119">SExistRestriction</span></span>](sexistrestriction.md)
- [<span data-ttu-id="b6afa-120">SAndRestriction</span><span class="sxs-lookup"><span data-stu-id="b6afa-120">SAndRestriction</span></span>](sandrestriction.md)
