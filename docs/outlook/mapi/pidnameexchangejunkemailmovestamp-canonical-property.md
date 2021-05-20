---
title: PidNameExchangeJunkEmailMoveStamp (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidNameExchangeJunkEmailMoveStamp
api_type:
- COM
ms.assetid: 7a52f46c-371c-46d0-8d66-e154482e8269
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 098261cd71631e4816d22272e1b1bef1d5932a94
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540945"
---
# <a name="pidnameexchangejunkemailmovestamp-canonical-property"></a><span data-ttu-id="3c9aa-103">PidNameExchangeJunkEmailMoveStamp (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="3c9aa-103">PidNameExchangeJunkEmailMoveStamp Canonical Property</span></span>

  
  
<span data-ttu-id="3c9aa-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3c9aa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3c9aa-105">Enthält den dauerhaften Nachrichtenwert, der angibt, dass die Nachricht nicht von einem Spamfilter verarbeitet werden soll, da die Nachricht entweder bereits verarbeitet wurde oder sicher ist.</span><span class="sxs-lookup"><span data-stu-id="3c9aa-105">Contains the persisted message value that indicates that the message should not be processed by a spam filter because the message was either already processed or is safe.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3c9aa-106">Anzeigenamen:</span><span class="sxs-lookup"><span data-stu-id="3c9aa-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="3c9aa-107">Keine</span><span class="sxs-lookup"><span data-stu-id="3c9aa-107">None</span></span>  <br/> |
|<span data-ttu-id="3c9aa-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="3c9aa-108">Property set:</span></span>  <br/> |<span data-ttu-id="3c9aa-109">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="3c9aa-109">PS_PUBLIC_STRINGS</span></span>  <br/> |
|<span data-ttu-id="3c9aa-110">Eigenschaftsname:</span><span class="sxs-lookup"><span data-stu-id="3c9aa-110">Property name:</span></span>  <br/> |http://schemas.microsoft.com/exchange/junkemailmovestamp  <br/> |
|<span data-ttu-id="3c9aa-111">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="3c9aa-111">Data type:</span></span>  <br/> |<span data-ttu-id="3c9aa-112">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="3c9aa-112">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="3c9aa-113">Bereich:</span><span class="sxs-lookup"><span data-stu-id="3c9aa-113">Area:</span></span>  <br/> |<span data-ttu-id="3c9aa-114">Sicheres Messaging</span><span class="sxs-lookup"><span data-stu-id="3c9aa-114">Secure messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3c9aa-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="3c9aa-115">Remarks</span></span>

<span data-ttu-id="3c9aa-116">Diese Eigenschaft wird für jede Nachricht gestempelt, die von der Junk-E-Mail-Regel verschoben wird oder anderweitig vertrauenswürdige Inhalte sind.</span><span class="sxs-lookup"><span data-stu-id="3c9aa-116">This property is stamped on every message that is moved by the Junk E-Mail Rule or is otherwise trusted content.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="3c9aa-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="3c9aa-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3c9aa-118">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="3c9aa-118">Protocol specifications</span></span>

<span data-ttu-id="3c9aa-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3c9aa-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3c9aa-120">Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="3c9aa-120">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3c9aa-121">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3c9aa-121">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3c9aa-122">Ermöglicht die Behandlung von Zulässig-/Sperrlisten und die Ermittlung von Junk-E-Mail-Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="3c9aa-122">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
<span data-ttu-id="3c9aa-123">[[MS-OXORSS]](https://msdn.microsoft.com/library/53bc9634-0040-4b5a-aecd-29781d826009%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3c9aa-123">[[MS-OXORSS]](https://msdn.microsoft.com/library/53bc9634-0040-4b5a-aecd-29781d826009%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3c9aa-124">Gibt die Eigenschaften und Vorgänge an, die RSS-Elemente darstellen.</span><span class="sxs-lookup"><span data-stu-id="3c9aa-124">Specifies the properties and operations that represent RSS items.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3c9aa-125">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="3c9aa-125">Header files</span></span>

<span data-ttu-id="3c9aa-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3c9aa-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="3c9aa-127">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="3c9aa-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3c9aa-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3c9aa-128">See also</span></span>



[<span data-ttu-id="3c9aa-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3c9aa-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3c9aa-130">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="3c9aa-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3c9aa-131">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="3c9aa-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3c9aa-132">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="3c9aa-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

