---
title: PidTagDefaultViewEntryId (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDefaultViewEntryId
api_type:
- HeaderDef
ms.assetid: 1b4e82ed-c207-4828-8a5b-0ef312962355
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 6d284782de86b603e6bbe190931a85cd9196c88b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270014"
---
# <a name="pidtagdefaultviewentryid-canonical-property"></a><span data-ttu-id="5dd1e-103">PidTagDefaultViewEntryId (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="5dd1e-103">PidTagDefaultViewEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="5dd1e-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5dd1e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5dd1e-105">Enthält die Eintrags-ID der Standardansicht eines Ordners.</span><span class="sxs-lookup"><span data-stu-id="5dd1e-105">Contains the entry identifier of a folder's default view.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5dd1e-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="5dd1e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5dd1e-107">PR_DEFAULT_VIEW_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="5dd1e-107">PR_DEFAULT_VIEW_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="5dd1e-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="5dd1e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5dd1e-109">0x3616</span><span class="sxs-lookup"><span data-stu-id="5dd1e-109">0x3616</span></span>  <br/> |
|<span data-ttu-id="5dd1e-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="5dd1e-110">Data type:</span></span>  <br/> |<span data-ttu-id="5dd1e-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="5dd1e-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="5dd1e-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="5dd1e-112">Area:</span></span>  <br/> |<span data-ttu-id="5dd1e-113">MAPI-Container</span><span class="sxs-lookup"><span data-stu-id="5dd1e-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5dd1e-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5dd1e-114">Remarks</span></span>

<span data-ttu-id="5dd1e-115">Diese Eigenschaft ist die Eintrags-ID der Ordneransicht, die als Ausgangsansicht festgelegt werden sollte.</span><span class="sxs-lookup"><span data-stu-id="5dd1e-115">This property is the entry identifier of the folder view that should be set as the initial view.</span></span> <span data-ttu-id="5dd1e-116">Die Eigenschaft muss nicht festgelegt werden, wenn die "Normal"-Ansicht als Ausgangsansicht verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="5dd1e-116">The property need not be set if the "Normal" view is to be used as the initial view.</span></span>
  
<span data-ttu-id="5dd1e-117">Eine Clientanwendung kann diese Eigenschaft beim Öffnen des Ordners abrufen und erhebliche Leistungsgewinne erzielen.</span><span class="sxs-lookup"><span data-stu-id="5dd1e-117">A client application can obtain this property at the time it opens the folder and realize significant performance gains.</span></span> <span data-ttu-id="5dd1e-118">Diese Eigenschaft kann als Verknüpfung verwendet werden, um die Standardansicht zu erhalten, anstatt die zugeordnete Inhaltstabelle zu öffnen und eine Einschränkung zu übermitteln.</span><span class="sxs-lookup"><span data-stu-id="5dd1e-118">This property can be used as a shortcut to obtain the default view, instead of opening the associated contents table and submitting a restriction.</span></span>
  
<span data-ttu-id="5dd1e-119">Eine Dienstanbieterimplementierung der [IMAPIFolder::CopyFolder-Methode](imapifolder-copyfolder.md) kann diese Eigenschaft kopieren, wenn Ordner kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="5dd1e-119">A service provider implementation of the [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md) method can copy this property when it copies folders.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="5dd1e-120">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="5dd1e-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5dd1e-121">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="5dd1e-121">Protocol specifications</span></span>

<span data-ttu-id="5dd1e-122">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5dd1e-122">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5dd1e-123">Verarbeitet Ordnervorgänge.</span><span class="sxs-lookup"><span data-stu-id="5dd1e-123">Handles folder operations.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5dd1e-124">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="5dd1e-124">Header files</span></span>

<span data-ttu-id="5dd1e-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5dd1e-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="5dd1e-126">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="5dd1e-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="5dd1e-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="5dd1e-127">Mapitags.h</span></span>
  
> <span data-ttu-id="5dd1e-128">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="5dd1e-128">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5dd1e-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5dd1e-129">See also</span></span>



[<span data-ttu-id="5dd1e-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5dd1e-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5dd1e-131">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="5dd1e-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5dd1e-132">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="5dd1e-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5dd1e-133">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="5dd1e-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

