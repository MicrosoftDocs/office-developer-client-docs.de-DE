---
title: PidLidExceptionReplaceTime (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidExceptionReplaceTime
api_type:
- COM
ms.assetid: c3aae4f5-7f00-45bf-b007-370041ba360e
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: b364fb91bda7e895b546f9a281ef14ce33b073f9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337982"
---
# <a name="pidlidexceptionreplacetime-canonical-property"></a><span data-ttu-id="357b0-103">PidLidExceptionReplaceTime (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="357b0-103">PidLidExceptionReplaceTime Canonical Property</span></span>

  
  
<span data-ttu-id="357b0-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="357b0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="357b0-105">Gibt das Datum und die Uhrzeit innerhalb des Serienmusters an, das durch die Ausnahme ersetzt wird.</span><span class="sxs-lookup"><span data-stu-id="357b0-105">Specifies the date and time within the recurrence pattern that the exception will replace.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="357b0-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="357b0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="357b0-107">dispidExceptionReplaceTime</span><span class="sxs-lookup"><span data-stu-id="357b0-107">dispidExceptionReplaceTime</span></span>  <br/> |
|<span data-ttu-id="357b0-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="357b0-108">Property set:</span></span>  <br/> |<span data-ttu-id="357b0-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="357b0-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="357b0-110">Lange ID (LID):</span><span class="sxs-lookup"><span data-stu-id="357b0-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="357b0-111">0x00008228</span><span class="sxs-lookup"><span data-stu-id="357b0-111">0x00008228</span></span>  <br/> |
|<span data-ttu-id="357b0-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="357b0-112">Data type:</span></span>  <br/> |<span data-ttu-id="357b0-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="357b0-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="357b0-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="357b0-114">Area:</span></span>  <br/> |<span data-ttu-id="357b0-115">Kalender</span><span class="sxs-lookup"><span data-stu-id="357b0-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="357b0-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="357b0-116">Remarks</span></span>

<span data-ttu-id="357b0-117">Der Wert muss in koordinierter Weltzeit (Coordinated Universal Time, UTC) angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="357b0-117">The value must be specified in Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="357b0-118">Mit dieser Eigenschaft kann das Ausnahmeanlageobjekt für eine bestimmte Instanz gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="357b0-118">This property allows the exception attachment object to be found for a particular instance.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="357b0-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="357b0-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="357b0-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="357b0-120">Protocol specifications</span></span>

<span data-ttu-id="357b0-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="357b0-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="357b0-122">Stellt Eigenschaftensatzdefinitionen zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="357b0-122">Provides property set definitions.</span></span>
    
<span data-ttu-id="357b0-123">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="357b0-123">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="357b0-124">Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungs- und Antwortnachrichten an.</span><span class="sxs-lookup"><span data-stu-id="357b0-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="357b0-125">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="357b0-125">Header files</span></span>

<span data-ttu-id="357b0-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="357b0-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="357b0-127">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="357b0-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="357b0-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="357b0-128">See also</span></span>



[<span data-ttu-id="357b0-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="357b0-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="357b0-130">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="357b0-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="357b0-131">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="357b0-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="357b0-132">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="357b0-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

