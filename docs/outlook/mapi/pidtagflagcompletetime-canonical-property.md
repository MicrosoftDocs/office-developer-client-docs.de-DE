---
title: PidTagFlagCompleteTime (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFlagCompleteTime
api_type:
- HeaderDef
ms.assetid: effc738a-30f4-4a5e-b21d-04b50dad1f45
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 5dd0d4c19f30e189218b1aeddd333df58e42102a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316289"
---
# <a name="pidtagflagcompletetime-canonical-property"></a><span data-ttu-id="ac4f9-103">PidTagFlagCompleteTime (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="ac4f9-103">PidTagFlagCompleteTime Canonical Property</span></span>

  
  
<span data-ttu-id="ac4f9-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ac4f9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ac4f9-105">Gibt Datum und Uhrzeit in koordinierter Weltzeit (Coordinated Universal Time, UTC) an, für die das Nachrichtenobjekt als abgeschlossen gekennzeichnet wurde.</span><span class="sxs-lookup"><span data-stu-id="ac4f9-105">Specifies the date and time in Coordinated Universal Time (UTC) that the message object was flagged as completed.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ac4f9-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="ac4f9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ac4f9-107">PR_FLAG_COMPLETE_TIME</span><span class="sxs-lookup"><span data-stu-id="ac4f9-107">PR_FLAG_COMPLETE_TIME</span></span>  <br/> |
|<span data-ttu-id="ac4f9-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="ac4f9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ac4f9-109">0x1091</span><span class="sxs-lookup"><span data-stu-id="ac4f9-109">0x1091</span></span>  <br/> |
|<span data-ttu-id="ac4f9-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="ac4f9-110">Data type:</span></span>  <br/> |<span data-ttu-id="ac4f9-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="ac4f9-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="ac4f9-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="ac4f9-112">Area:</span></span>  <br/> |<span data-ttu-id="ac4f9-113">Sonstiges</span><span class="sxs-lookup"><span data-stu-id="ac4f9-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ac4f9-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ac4f9-114">Remarks</span></span>

<span data-ttu-id="ac4f9-115">Diese Eigenschaft wird gelöscht, wenn das Message-Objekt nicht als abgeschlossen gekennzeichnet ist.</span><span class="sxs-lookup"><span data-stu-id="ac4f9-115">This property is deleted if the message object is not flagged complete.</span></span> <span data-ttu-id="ac4f9-116">Die kleinste Auflösung der Zeit muss Minuten sein (der Wert muss ein Vielfaches von 600.000.000 sein).</span><span class="sxs-lookup"><span data-stu-id="ac4f9-116">The time's smallest resolution must be minutes (the value must be a multiple of 600,000,000).</span></span> <span data-ttu-id="ac4f9-117">Diese Eigenschaft darf nicht vorhanden sein, wenn es sich bei dem Objekt um ein besprechungsbezogenes Objekt handelt und sie nicht für ein Aufgabenobjekt vorhanden sein sollte.</span><span class="sxs-lookup"><span data-stu-id="ac4f9-117">This property must not exist if the object is a meeting-related object, and it should not exist on a task object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="ac4f9-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="ac4f9-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ac4f9-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="ac4f9-119">Protocol specifications</span></span>

<span data-ttu-id="ac4f9-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ac4f9-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ac4f9-121">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="ac4f9-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ac4f9-122">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ac4f9-122">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ac4f9-123">Gibt die Eigenschaften und Vorgänge im Zusammenhang mit der Kennzeichnung an.</span><span class="sxs-lookup"><span data-stu-id="ac4f9-123">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ac4f9-124">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="ac4f9-124">Header files</span></span>

<span data-ttu-id="ac4f9-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ac4f9-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="ac4f9-126">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="ac4f9-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="ac4f9-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ac4f9-127">Mapitags.h</span></span>
  
> <span data-ttu-id="ac4f9-128">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="ac4f9-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ac4f9-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ac4f9-129">See also</span></span>



[<span data-ttu-id="ac4f9-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ac4f9-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ac4f9-131">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="ac4f9-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ac4f9-132">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="ac4f9-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ac4f9-133">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="ac4f9-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

