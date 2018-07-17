---
title: Kanonische PidTagSentRepresentingSmtpAddress-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5ed122a2-0967-4de3-a2ee-69f81ae77b16
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: d3a3545c544c7b5cf5200468a94edf720dd326e1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795152"
---
# <a name="pidtagsentrepresentingsmtpaddress-canonical-property"></a><span data-ttu-id="5a3b6-103">Kanonische PidTagSentRepresentingSmtpAddress-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="5a3b6-103">PidTagSentRepresentingSmtpAddress Canonical Property</span></span>

  
  
<span data-ttu-id="5a3b6-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5a3b6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5a3b6-105">Enthält die Simple Mail Transport Protocol (SMTP) e-Mail-Adresse für den messaging-Benutzer, die vom Absender dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="5a3b6-105">Contains the Simple Mail Transport Protocol (SMTP) email address for the messaging user who is represented by the sender.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5a3b6-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="5a3b6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5a3b6-107">PR_SENT_REPRESENTING_SMTP_ADDRESS, PR_SENT_REPRESENTING_SMTP_ADDRESS_A, PR_SENT_REPRESENTING_SMTP_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="5a3b6-107">PR_SENT_REPRESENTING_SMTP_ADDRESS, PR_SENT_REPRESENTING_SMTP_ADDRESS_A, PR_SENT_REPRESENTING_SMTP_ADDRESS_W</span></span>  <br/> |
|<span data-ttu-id="5a3b6-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="5a3b6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5a3b6-109">0x5D02</span><span class="sxs-lookup"><span data-stu-id="5a3b6-109">0x5D02</span></span>  <br/> |
|<span data-ttu-id="5a3b6-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="5a3b6-110">Data type:</span></span>  <br/> |<span data-ttu-id="5a3b6-111">PT_UNICODE PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="5a3b6-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="5a3b6-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="5a3b6-112">Area:</span></span>  <br/> |<span data-ttu-id="5a3b6-113">Adresse</span><span class="sxs-lookup"><span data-stu-id="5a3b6-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5a3b6-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5a3b6-114">Remarks</span></span>

<span data-ttu-id="5a3b6-115">Diese Eigenschaft ist ein Beispiel für die Adresseigenschaften für die messaging-Benutzer, die vom Absender angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="5a3b6-115">This property is an example of the address properties for the messaging user being represented by the sender.</span></span> <span data-ttu-id="5a3b6-116">Wenn eine Clientanwendung eine Nachricht im Auftrag einer anderen Client sendet, sollten sie alle Absender dargestellte Eigenschaften auf die Werte für diesen Client festgelegt.</span><span class="sxs-lookup"><span data-stu-id="5a3b6-116">When a client application sends a message on behalf of another client, it should set all the represented sender properties to the values for that client.</span></span> <span data-ttu-id="5a3b6-117">Ein messaging-Benutzer in der Regel in einem eigenen Auftrag senden bewirkt, dass die dargestellte Absender Eigenschaften nicht festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="5a3b6-117">A messaging user sending on its own behalf typically leaves the represented sender properties unset.</span></span>
  
<span data-ttu-id="5a3b6-118">Der ausgehende Adressbuchhierarchie muss immer lassen Sie diese Eigenschaft geändert, wenn es vom sendenden Client festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="5a3b6-118">The outgoing transport provider must always leave this property unchanged if it has been set by the sending client.</span></span> <span data-ttu-id="5a3b6-119">Wenn es nicht festgelegt ist, sollte der Adressbuchhierarchie legen Sie es an die **PR_SENDER_SMTP_ADDRESS** ([PidTagSenderSmtpAddress](pidtagsendersmtpaddress-canonical-property.md))-Eigenschaft für die ausgehende Kopie der Nachricht, und klicken Sie auf die lokale Kopie nicht festgelegt lassen.</span><span class="sxs-lookup"><span data-stu-id="5a3b6-119">If it is unset, the transport provider should set it to the **PR_SENDER_SMTP_ADDRESS** ([PidTagSenderSmtpAddress](pidtagsendersmtpaddress-canonical-property.md)) property on the outbound copy of the message, and leave it unset on the local copy.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="5a3b6-120">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="5a3b6-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5a3b6-121">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="5a3b6-121">Protocol specifications</span></span>

<span data-ttu-id="5a3b6-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5a3b6-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5a3b6-123">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="5a3b6-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5a3b6-124">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5a3b6-124">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5a3b6-125">Gibt die Eigenschaften und Operationen, die für e-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="5a3b6-125">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="5a3b6-126">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5a3b6-126">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5a3b6-127">Verarbeitet die Reihenfolge und den Fluss für Datenübertragungen zwischen einem Client und Server.</span><span class="sxs-lookup"><span data-stu-id="5a3b6-127">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="5a3b6-128">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5a3b6-128">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5a3b6-129">Gibt die Methoden zum Herstellen einer Verbindung mit und Konfiguration von Postfächer als Stellvertretungen und Interaktionen mit Nachricht und Kalender-Objekte, wenn sie im Auftrag eines anderen Benutzers agieren.</span><span class="sxs-lookup"><span data-stu-id="5a3b6-129">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="5a3b6-130">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5a3b6-130">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5a3b6-131">Konvertiert zwischen IETF RFC2445, RFC2446, RFC2447, und Termine und meeting-Objekte.</span><span class="sxs-lookup"><span data-stu-id="5a3b6-131">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="5a3b6-132">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5a3b6-132">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5a3b6-133">Konvertiert von Internet-standard-e-Mail-Konventionen in Message-Objekten.</span><span class="sxs-lookup"><span data-stu-id="5a3b6-133">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="5a3b6-134">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5a3b6-134">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5a3b6-135">Gibt die Eigenschaften und Operationen, die für Kontakte und persönliche Verteilerlisten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="5a3b6-135">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
<span data-ttu-id="5a3b6-136">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5a3b6-136">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5a3b6-137">Codiert und decodiert Nachrichten- und Objekte, die auf eine effiziente Streamdarstellung.</span><span class="sxs-lookup"><span data-stu-id="5a3b6-137">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5a3b6-138">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="5a3b6-138">Header files</span></span>

<span data-ttu-id="5a3b6-139">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5a3b6-139">Mapidefs.h</span></span>
  
> <span data-ttu-id="5a3b6-140">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="5a3b6-140">Provides data type definitions.</span></span>
    
<span data-ttu-id="5a3b6-141">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="5a3b6-141">Mapitags.h</span></span>
  
> <span data-ttu-id="5a3b6-142">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="5a3b6-142">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5a3b6-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5a3b6-143">See also</span></span>



[<span data-ttu-id="5a3b6-144">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5a3b6-144">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5a3b6-145">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5a3b6-145">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5a3b6-146">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="5a3b6-146">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5a3b6-147">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="5a3b6-147">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
