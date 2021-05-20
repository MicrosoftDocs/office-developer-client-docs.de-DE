---
title: PidTagContentCorrelator (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContentCorrelator
api_type:
- HeaderDef
ms.assetid: 0bf78879-2f9f-4c29-b1f4-2f4882d8464d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 96e0e3152a70eb2913c4559afd99e25adff48ca9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438526"
---
# <a name="pidtagcontentcorrelator-canonical-property"></a><span data-ttu-id="c2ede-103">PidTagContentCorrelator (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="c2ede-103">PidTagContentCorrelator Canonical Property</span></span>

  
  
<span data-ttu-id="c2ede-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c2ede-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c2ede-105">Enthält einen Wert, den der Absender der Nachricht verwenden kann, um einen Bericht mit der ursprünglichen Nachricht zu übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="c2ede-105">Contains a value the message sender can use to match a report with the original message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c2ede-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="c2ede-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c2ede-107">PR_CONTENT_CORRELATOR</span><span class="sxs-lookup"><span data-stu-id="c2ede-107">PR_CONTENT_CORRELATOR</span></span>  <br/> |
|<span data-ttu-id="c2ede-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="c2ede-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c2ede-109">0x0007</span><span class="sxs-lookup"><span data-stu-id="c2ede-109">0x0007</span></span>  <br/> |
|<span data-ttu-id="c2ede-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="c2ede-110">Data type:</span></span>  <br/> |<span data-ttu-id="c2ede-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="c2ede-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="c2ede-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="c2ede-112">Area:</span></span>  <br/> |<span data-ttu-id="c2ede-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="c2ede-113">Exchange</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c2ede-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c2ede-114">Remarks</span></span>

<span data-ttu-id="c2ede-115">Der Inhalt der binären Zeichenfolge wird vom Nachrichtenursprung definiert.</span><span class="sxs-lookup"><span data-stu-id="c2ede-115">The contents of the binary string are defined by the message originator.</span></span> <span data-ttu-id="c2ede-116">Wenn für eine ausgehende Nachricht festgelegt, sollte diese Eigenschaft in alle Berichte kopiert werden, die als Antwort auf die Nachricht generiert werden.</span><span class="sxs-lookup"><span data-stu-id="c2ede-116">If set on an outgoing message, this property should be copied onto any reports generated in response to the message.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c2ede-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="c2ede-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="c2ede-118">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="c2ede-118">Header files</span></span>

<span data-ttu-id="c2ede-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c2ede-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="c2ede-120">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="c2ede-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="c2ede-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c2ede-121">Mapitags.h</span></span>
  
> <span data-ttu-id="c2ede-122">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="c2ede-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c2ede-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c2ede-123">See also</span></span>



[<span data-ttu-id="c2ede-124">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c2ede-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c2ede-125">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="c2ede-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c2ede-126">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="c2ede-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c2ede-127">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="c2ede-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

