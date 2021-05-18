---
title: PidTagAddressType (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAddressType
api_type:
- HeaderDef
ms.assetid: 986719d2-8837-46b4-8d04-c24508f5e19a
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 6051d3403cede21fa4aebdb6ca561dd3efb46771
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360085"
---
# <a name="pidtagaddresstype-canonical-property"></a><span data-ttu-id="5e3b1-103">PidTagAddressType (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="5e3b1-103">PidTagAddressType Canonical Property</span></span>

<span data-ttu-id="5e3b1-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5e3b1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5e3b1-105">Enthält den E-Mail-Adresstyp des Messagingbenutzers, z. B. SMTP.</span><span class="sxs-lookup"><span data-stu-id="5e3b1-105">Contains the messaging user's email address type, such as SMTP.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5e3b1-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="5e3b1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5e3b1-107">PR_ADDRTYPE, PR_ADDRTYPE_A, PR_ADDRTYPE_W</span><span class="sxs-lookup"><span data-stu-id="5e3b1-107">PR_ADDRTYPE, PR_ADDRTYPE_A, PR_ADDRTYPE_W</span></span>  <br/> |
|<span data-ttu-id="5e3b1-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="5e3b1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5e3b1-109">0x3002</span><span class="sxs-lookup"><span data-stu-id="5e3b1-109">0x3002</span></span>  <br/> |
|<span data-ttu-id="5e3b1-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="5e3b1-110">Data type:</span></span>  <br/> |<span data-ttu-id="5e3b1-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="5e3b1-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="5e3b1-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="5e3b1-112">Area:</span></span>  <br/> |<span data-ttu-id="5e3b1-113">Adresse</span><span class="sxs-lookup"><span data-stu-id="5e3b1-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5e3b1-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5e3b1-114">Remarks</span></span>

<span data-ttu-id="5e3b1-115">Diese Eigenschaften sind Beispiele für die Basisadresseneigenschaften, die allen Messagingbenutzern gemeinsam sind.</span><span class="sxs-lookup"><span data-stu-id="5e3b1-115">These properties are examples of the base address properties common to all messaging users.</span></span> <span data-ttu-id="5e3b1-116">Es gibt an, welches Messagingsystem MAPI zum Verarbeiten einer bestimmten Nachricht verwendet.</span><span class="sxs-lookup"><span data-stu-id="5e3b1-116">It specifies which messaging system MAPI uses to handle a given message.</span></span>
  
<span data-ttu-id="5e3b1-117">Diese Eigenschaft bestimmt auch das Format der Adresszeichenfolge im **PR_EMAIL_ADRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="5e3b1-117">This property also determines the format of the address string in the **PR_EMAIL_ADRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)).</span></span> <span data-ttu-id="5e3b1-118">Die zeichenfolge, die sie enthält, kann nur die großbuchstaben alphabetischen Zeichen von A bis Z und die Zahlen von 0 bis 9 enthalten.</span><span class="sxs-lookup"><span data-stu-id="5e3b1-118">The string it provides can contain only the uppercase alphabetic characters from A through Z and the numbers from 0 through 9.</span></span>
  
<span data-ttu-id="5e3b1-119">Gültige Beispiele für die Zeichenfolge sind:</span><span class="sxs-lookup"><span data-stu-id="5e3b1-119">Valid examples for the string include:</span></span> 
  
```cpp
FAX
MHS
PROFS
SMTP
X400

```

## <a name="related-resources"></a><span data-ttu-id="5e3b1-120">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="5e3b1-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5e3b1-121">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="5e3b1-121">Protocol specifications</span></span>

<span data-ttu-id="5e3b1-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5e3b1-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5e3b1-123">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="5e3b1-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5e3b1-124">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5e3b1-124">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5e3b1-125">Gibt die Eigenschaften und Vorgänge für Listen von Benutzern, Kontakten, Gruppen und Ressourcen an.</span><span class="sxs-lookup"><span data-stu-id="5e3b1-125">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="5e3b1-126">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5e3b1-126">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5e3b1-127">Konvertiert von Internetstandard-E-Mail-Konventionen in Nachrichtenobjekte.</span><span class="sxs-lookup"><span data-stu-id="5e3b1-127">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="5e3b1-128">[[MS-NSPI]](https://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5e3b1-128">[[MS-NSPI]](https://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5e3b1-129">Verarbeitet die Kommunikation eines Clients mit einem NSPI-Server (Name Service Provider Interface).</span><span class="sxs-lookup"><span data-stu-id="5e3b1-129">Handles a client's communications with a Name Service Provider Interface (NSPI) server.</span></span>
    
<span data-ttu-id="5e3b1-130">[[MS-OXCDATA]](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5e3b1-130">[[MS-OXCDATA]](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5e3b1-131">Definiert die grundlegenden Datenstrukturen, die in Remotevorgängen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5e3b1-131">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="5e3b1-132">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5e3b1-132">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5e3b1-133">Verarbeitet die Reihenfolge und den Fluss für Datenübertragungen zwischen einem Client und einem Server.</span><span class="sxs-lookup"><span data-stu-id="5e3b1-133">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="5e3b1-134">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5e3b1-134">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5e3b1-135">Konvertiert zwischen IETF RFC2445, RFC2446 und RFC2447 sowie Termin- und Besprechungsobjekten.</span><span class="sxs-lookup"><span data-stu-id="5e3b1-135">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="5e3b1-136">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5e3b1-136">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5e3b1-137">Behandelt Nachrichten- und Anlagenobjekte.</span><span class="sxs-lookup"><span data-stu-id="5e3b1-137">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="5e3b1-138">[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5e3b1-138">[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5e3b1-139">Gibt zulässige Vorgänge für die Zentralen Nachrichtenspeicherobjekte an.</span><span class="sxs-lookup"><span data-stu-id="5e3b1-139">Specifies permissible operations for the core message store objects.</span></span>
    
<span data-ttu-id="5e3b1-140">[[MS-OXOABKT]](https://msdn.microsoft.com/library/cd5a3e78-1eeb-4a75-88eb-e82c8c96ff31%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5e3b1-140">[[MS-OXOABKT]](https://msdn.microsoft.com/library/cd5a3e78-1eeb-4a75-88eb-e82c8c96ff31%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5e3b1-141">Gibt die Eigenschaften und Vorgänge an, die für Adressbuchvorlagen zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="5e3b1-141">Specifies the properties and operations that are permissible for address book templates.</span></span>
    
<span data-ttu-id="5e3b1-142">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5e3b1-142">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5e3b1-143">Gibt die Eigenschaften und Vorgänge an, die für E-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="5e3b1-143">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="5e3b1-144">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5e3b1-144">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5e3b1-145">Bearbeitet eingehende E-Mail-Nachrichten auf einem Server.</span><span class="sxs-lookup"><span data-stu-id="5e3b1-145">Manipulates incoming email messages on a server.</span></span>
    
<span data-ttu-id="5e3b1-146">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5e3b1-146">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5e3b1-147">Gibt die Eigenschaften und Vorgänge zum Bearbeiten einer Suchordnerlistenkonfiguration an.</span><span class="sxs-lookup"><span data-stu-id="5e3b1-147">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5e3b1-148">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="5e3b1-148">Header files</span></span>

<span data-ttu-id="5e3b1-149">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5e3b1-149">Mapidefs.h</span></span>
  
> <span data-ttu-id="5e3b1-150">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="5e3b1-150">Provides data type definitions.</span></span>
    
<span data-ttu-id="5e3b1-151">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="5e3b1-151">Mapitags.h</span></span>
  
> <span data-ttu-id="5e3b1-152">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="5e3b1-152">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5e3b1-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5e3b1-153">See also</span></span>



[<span data-ttu-id="5e3b1-154">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5e3b1-154">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5e3b1-155">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="5e3b1-155">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5e3b1-156">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="5e3b1-156">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5e3b1-157">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="5e3b1-157">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
  
[<span data-ttu-id="5e3b1-158">MAPI-Adresstypen</span><span class="sxs-lookup"><span data-stu-id="5e3b1-158">MAPI Address Types</span></span>](mapi-address-types.md)

