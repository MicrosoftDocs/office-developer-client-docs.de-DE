---
title: PidTagScheduleInfoMonthsAway (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoMonthsAway
api_type:
- COM
ms.assetid: 282a8ba1-b786-4d17-b6c5-17e935e59a6b
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 90df272a70fd4133a780f205c93b42f26ed1ae96
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303409"
---
# <a name="pidtagscheduleinfomonthsaway-canonical-property"></a><span data-ttu-id="b9159-103">PidTagScheduleInfoMonthsAway (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="b9159-103">PidTagScheduleInfoMonthsAway Canonical Property</span></span>

  
  
<span data-ttu-id="b9159-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b9159-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b9159-105">Enthält eine Liste der Monate, für die Frei/Gebucht-Daten vom Typ "Out of Office" (OOF) in der Frei/Gebucht-Nachricht vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="b9159-105">Contains a list of the months for which free/busy data of type out of office (OOF) is present in the free/busy message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b9159-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="b9159-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b9159-107">PR_SCHDINFO_MONTHS_OOF</span><span class="sxs-lookup"><span data-stu-id="b9159-107">PR_SCHDINFO_MONTHS_OOF</span></span>  <br/> |
|<span data-ttu-id="b9159-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="b9159-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b9159-109">0x6855</span><span class="sxs-lookup"><span data-stu-id="b9159-109">0x6855</span></span>  <br/> |
|<span data-ttu-id="b9159-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="b9159-110">Data type:</span></span>  <br/> |<span data-ttu-id="b9159-111">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="b9159-111">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="b9159-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="b9159-112">Area:</span></span>  <br/> |<span data-ttu-id="b9159-113">Frei/Gebucht</span><span class="sxs-lookup"><span data-stu-id="b9159-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b9159-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b9159-114">Remarks</span></span>

<span data-ttu-id="b9159-115">Das Format, die Berechnung und die Einschränkungen dieser Eigenschaft sind mit denen von **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) identisch, beziehen sich jedoch auf Termine, die im zugeordneten Kalenderobjekt als out of office (OOF) gekennzeichnet sind.</span><span class="sxs-lookup"><span data-stu-id="b9159-115">The format, computation and constraints of this property are the same as those of **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) but refer to appointments that are marked out of office (OOF) on the associated calendar object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b9159-116">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="b9159-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b9159-117">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="b9159-117">Protocol specifications</span></span>

<span data-ttu-id="b9159-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b9159-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b9159-119">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="b9159-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b9159-120">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b9159-120">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b9159-121">Veröffentlicht die Verfügbarkeit eines Benutzers oder einer Ressource.</span><span class="sxs-lookup"><span data-stu-id="b9159-121">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b9159-122">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="b9159-122">Header files</span></span>

<span data-ttu-id="b9159-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b9159-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="b9159-124">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="b9159-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="b9159-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b9159-125">Mapitags.h</span></span>
  
> <span data-ttu-id="b9159-126">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="b9159-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b9159-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b9159-127">See also</span></span>



[<span data-ttu-id="b9159-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b9159-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b9159-129">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="b9159-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b9159-130">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="b9159-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b9159-131">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="b9159-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

