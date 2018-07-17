---
title: IAttach IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAttach
api_type:
- COM
ms.assetid: f47e20e1-2a30-4c9e-8ca6-e8c5e72f44a1
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 66e318c3b7b772f2713b5c730590ce4a8ad5965b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792010"
---
# <a name="iattach--imapiprop"></a><span data-ttu-id="6756f-103">IAttach: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="6756f-103">IAttach : IMAPIProp</span></span>

  
  
<span data-ttu-id="6756f-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6756f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6756f-105">Verwaltet und bietet Zugriff auf die Eigenschaften von Nachrichtenanlagen.</span><span class="sxs-lookup"><span data-stu-id="6756f-105">Maintains and provides access to the properties of attachments in messages.</span></span> <span data-ttu-id="6756f-106">Die **IAttach** -Schnittstelle hat keine eindeutigen Methoden.</span><span class="sxs-lookup"><span data-stu-id="6756f-106">The **IAttach** interface has no unique methods of its own.</span></span> <span data-ttu-id="6756f-107">Weitere Informationen zur Verwendung von Anlagen finden Sie unter [MAPI-Anlagen](mapi-attachments.md) und [Anlagentabellen](attachment-tables.md).</span><span class="sxs-lookup"><span data-stu-id="6756f-107">For more information about how to use attachments, see [MAPI Attachments](mapi-attachments.md) and [Attachment Tables](attachment-tables.md).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6756f-108">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="6756f-108">Header file:</span></span>  <br/> |<span data-ttu-id="6756f-109">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6756f-109">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="6756f-110">Verf�gbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="6756f-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="6756f-111">Attachment-Objekte</span><span class="sxs-lookup"><span data-stu-id="6756f-111">Attachment objects</span></span>  <br/> |
|<span data-ttu-id="6756f-112">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="6756f-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="6756f-113">Nachricht-Anbieter</span><span class="sxs-lookup"><span data-stu-id="6756f-113">Message store providers</span></span>  <br/> |
|<span data-ttu-id="6756f-114">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="6756f-114">Called by:</span></span>  <br/> |<span data-ttu-id="6756f-115">Clientanwendungen</span><span class="sxs-lookup"><span data-stu-id="6756f-115">Client applications</span></span>  <br/> |
|<span data-ttu-id="6756f-116">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="6756f-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="6756f-117">IID_IAttachment</span><span class="sxs-lookup"><span data-stu-id="6756f-117">IID_IAttachment</span></span>  <br/> |
|<span data-ttu-id="6756f-118">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="6756f-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="6756f-119">LPATTACH</span><span class="sxs-lookup"><span data-stu-id="6756f-119">LPATTACH</span></span>  <br/> |
|<span data-ttu-id="6756f-120">Transaktionsmodell:</span><span class="sxs-lookup"><span data-stu-id="6756f-120">Transaction model:</span></span>  <br/> |<span data-ttu-id="6756f-121">Durchgeführt</span><span class="sxs-lookup"><span data-stu-id="6756f-121">Transacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="6756f-122">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="6756f-122">Vtable order</span></span>

<span data-ttu-id="6756f-123">Diese Schnittstelle hat keinen eindeutigen Methoden.</span><span class="sxs-lookup"><span data-stu-id="6756f-123">This interface does not have any unique methods.</span></span>
  
|<span data-ttu-id="6756f-124">**Erforderliche Eigenschaften**</span><span class="sxs-lookup"><span data-stu-id="6756f-124">**Required properties**</span></span>|<span data-ttu-id="6756f-125">**Zugriff**</span><span class="sxs-lookup"><span data-stu-id="6756f-125">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6756f-126">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6756f-126">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="6756f-127">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="6756f-127">Read-only</span></span>  <br/> |
|<span data-ttu-id="6756f-128">**PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6756f-128">**PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="6756f-129">Lese-/Schreibzugriff</span><span class="sxs-lookup"><span data-stu-id="6756f-129">Read/write</span></span>  <br/> |
|<span data-ttu-id="6756f-130">**PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6756f-130">**PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="6756f-131">Lese-/Schreibzugriff</span><span class="sxs-lookup"><span data-stu-id="6756f-131">Read/write</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6756f-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6756f-132">See also</span></span>



[<span data-ttu-id="6756f-133">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="6756f-133">MAPI Interfaces</span></span>](mapi-interfaces.md)
