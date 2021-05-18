---
title: PidTagGender (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagGender
api_type:
- HeaderDef
ms.assetid: a79a139a-6813-49f6-b622-bb66d62c4462
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: b8ce3898ac021bc6eec2af6220889d71ff5a18dc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316156"
---
# <a name="pidtaggender-canonical-property"></a><span data-ttu-id="867c1-103">PidTagGender (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="867c1-103">PidTagGender Canonical Property</span></span>

  
  
<span data-ttu-id="867c1-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="867c1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="867c1-105">Enthält das Geschlecht des Messagingbenutzers.</span><span class="sxs-lookup"><span data-stu-id="867c1-105">Contains the gender of the messaging user.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="867c1-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="867c1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="867c1-107">PR_GENDER</span><span class="sxs-lookup"><span data-stu-id="867c1-107">PR_GENDER</span></span>  <br/> |
|<span data-ttu-id="867c1-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="867c1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="867c1-109">0x3A4D</span><span class="sxs-lookup"><span data-stu-id="867c1-109">0x3A4D</span></span>  <br/> |
|<span data-ttu-id="867c1-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="867c1-110">Data type:</span></span>  <br/> |<span data-ttu-id="867c1-111">PT_I2</span><span class="sxs-lookup"><span data-stu-id="867c1-111">PT_I2</span></span>  <br/> |
|<span data-ttu-id="867c1-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="867c1-112">Area:</span></span>  <br/> |<span data-ttu-id="867c1-113">MAPI-E-Mail-Benutzer</span><span class="sxs-lookup"><span data-stu-id="867c1-113">MAPI mail user</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="867c1-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="867c1-114">Remarks</span></span>

<span data-ttu-id="867c1-115">Diese Eigenschaft stellt Identifikations- und Zugriffsinformationen zu einem Messagingbenutzer und den Inhalten zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="867c1-115">This property provides identification and access information about a messaging user and the content is.</span></span> <span data-ttu-id="867c1-116">Der Inhalt wird vom Messagingbenutzer und der Organisation des Messagingbenutzers definiert.</span><span class="sxs-lookup"><span data-stu-id="867c1-116">The content is defined by the messaging user and the messaging user's organization.</span></span> 
  
<span data-ttu-id="867c1-117">Die möglichen Werte für diese Eigenschaft werden in der Gender-Enumeration definiert.</span><span class="sxs-lookup"><span data-stu-id="867c1-117">The possible values for this property are defined in the gender enumeration.</span></span> <span data-ttu-id="867c1-118">Sie sind wie folgt aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="867c1-118">They are listed as follows:</span></span>
  
|<span data-ttu-id="867c1-119">**Gender enumeration**</span><span class="sxs-lookup"><span data-stu-id="867c1-119">**Gender enumeration**</span></span>|<span data-ttu-id="867c1-120">**Wert**</span><span class="sxs-lookup"><span data-stu-id="867c1-120">**Value**</span></span>|<span data-ttu-id="867c1-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="867c1-121">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="867c1-122">genderUnspecified</span><span class="sxs-lookup"><span data-stu-id="867c1-122">genderUnspecified</span></span>  <br/> |<span data-ttu-id="867c1-123">0x0000</span><span class="sxs-lookup"><span data-stu-id="867c1-123">0x0000</span></span>  <br/> |<span data-ttu-id="867c1-124">Das Geschlecht des Kontakts ist nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="867c1-124">The contact's gender is unspecified.</span></span>  <br/> |
|<span data-ttu-id="867c1-125">genderFemale</span><span class="sxs-lookup"><span data-stu-id="867c1-125">genderFemale</span></span>  <br/> |<span data-ttu-id="867c1-126">0x0001</span><span class="sxs-lookup"><span data-stu-id="867c1-126">0x0001</span></span>  <br/> |<span data-ttu-id="867c1-127">Der Kontakt ist weiblich.</span><span class="sxs-lookup"><span data-stu-id="867c1-127">The contact is female.</span></span>  <br/> |
|<span data-ttu-id="867c1-128">genderMale</span><span class="sxs-lookup"><span data-stu-id="867c1-128">genderMale</span></span>  <br/> |<span data-ttu-id="867c1-129">0x0002</span><span class="sxs-lookup"><span data-stu-id="867c1-129">0x0002</span></span>  <br/> |<span data-ttu-id="867c1-130">Der Kontakt ist männlich.</span><span class="sxs-lookup"><span data-stu-id="867c1-130">The contact is male.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="867c1-131">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="867c1-131">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="867c1-132">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="867c1-132">Protocol specifications</span></span>

<span data-ttu-id="867c1-133">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="867c1-133">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="867c1-134">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="867c1-134">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="867c1-135">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="867c1-135">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="867c1-136">Gibt die Eigenschaften und Vorgänge an, die für Kontakte und persönliche Verteilerlisten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="867c1-136">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
<span data-ttu-id="867c1-137">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="867c1-137">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="867c1-138">Gibt die Eigenschaften und Vorgänge für Listen von Benutzern, Kontakten, Gruppen und Ressourcen an.</span><span class="sxs-lookup"><span data-stu-id="867c1-138">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="867c1-139">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="867c1-139">Header files</span></span>

<span data-ttu-id="867c1-140">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="867c1-140">Mapidefs.h</span></span>
  
> <span data-ttu-id="867c1-141">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="867c1-141">Provides data type definitions.</span></span>
    
<span data-ttu-id="867c1-142">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="867c1-142">Mapitags.h</span></span>
  
> <span data-ttu-id="867c1-143">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="867c1-143">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="867c1-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="867c1-144">See also</span></span>



[<span data-ttu-id="867c1-145">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="867c1-145">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="867c1-146">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="867c1-146">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="867c1-147">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="867c1-147">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="867c1-148">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="867c1-148">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

