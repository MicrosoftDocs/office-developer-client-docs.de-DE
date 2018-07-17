---
title: Formatierter Text in MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4d0ff834-253b-4e8c-a5be-6e4745a2a66c
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 6b82a755cbf2c8bd0f1d3676d4560e131dce3bd2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791741"
---
# <a name="formatted-text-in-mapi"></a><span data-ttu-id="91109-103">Formatierter Text in MAPI</span><span class="sxs-lookup"><span data-stu-id="91109-103">Formatted Text in MAPI</span></span>

  
  
<span data-ttu-id="91109-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="91109-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="91109-105">Der Text einer Nachricht gespeichert werden kann und mit unformatiertem Text gesendet oder formatierter Text.</span><span class="sxs-lookup"><span data-stu-id="91109-105">The text of a message can be stored and transmitted using plain text or formatted text.</span></span> <span data-ttu-id="91109-106">Formatierter Text erhöht den Nachrichtentext durch seine Darstellung mit, beispielsweise eine oder mehrere Schriftarten, Schriftgrößen oder Textfarben ändern.</span><span class="sxs-lookup"><span data-stu-id="91109-106">Formatted text enhances the message text by altering its appearance with, for example, one or more fonts, font sizes, or text colors.</span></span> <span data-ttu-id="91109-107">Es wird empfohlen, alle Clients und möglichst unterstützen alle Nachricht Speicher-Anbieter formatierten Text.</span><span class="sxs-lookup"><span data-stu-id="91109-107">It is recommended that all clients and whenever possible, all message store providers, support formatted text.</span></span> <span data-ttu-id="91109-108">Unterstützung von formatierten Text in Nachrichten fügt Wert durch Verbesserung der Lesbarkeit Nachricht und tätigen Nachrichtenbehandlung einfacher und effizienter hinzu.</span><span class="sxs-lookup"><span data-stu-id="91109-108">Supporting formatted text in messages adds value by improving message readability and making message handling easier and more efficient.</span></span>
  
<span data-ttu-id="91109-109">Formatierter Text kann in verschiedene Arten implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="91109-109">Formatted text can be implemented in a variety of ways.</span></span> <span data-ttu-id="91109-110">Die am häufigsten verwendete Methode ist mit Rich Text Format (RTF).</span><span class="sxs-lookup"><span data-stu-id="91109-110">The most common way is with the Rich Text Format (RTF).</span></span> <span data-ttu-id="91109-111">MAPI definiert drei Übertragungseinehit Eigenschaften zum Aufbewahren von Text Nachrichteninformationen: **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) für nur-Text, **http://Schemas.Microsoft.com/mapi/proptag/0x10130102** ([PidTagHtml](pidtaghtml-canonical-property.md)) für HTML und **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md) ) für RTF-Text komprimiert wurde.</span><span class="sxs-lookup"><span data-stu-id="91109-111">MAPI defines three transmittable properties for holding message text information: **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) for plain text, **PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) for HTML, and **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) for RTF text that has been compressed.</span></span> <span data-ttu-id="91109-112">Da die formatierte Version der einen Meldungstext zweimal so groß wie die Version ist, kann ohne Formatierung wird RTF-Text komprimiert, bevor sie mit der Meldung übertragen und in der Eigenschaft **PR_RTF_COMPRESSED** gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="91109-112">Because the formatted version of a message text can be twice as large as the version without the formatting, the RTF text is compressed before it is transferred with the message and stored in the **PR_RTF_COMPRESSED** property.</span></span> <span data-ttu-id="91109-113">Wenn die Meldung auf dem Bildschirm angezeigt wird, ist es nicht komprimierten mithilfe einer Dienstprogrammfunktion von MAPI bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="91109-113">When it is time to display the message on the screen, it is uncompressed using a utility function provided by MAPI.</span></span> 
  
<span data-ttu-id="91109-114">MAPI definiert diese beiden Text Nachrichteneigenschaften und Mechanismen für die Konvertierung zwischen diesen so, dass RTF-fähigen Clients mit Clients und bieten keine Unterstützung für messaging-Systemen interagieren können formatierter Text.</span><span class="sxs-lookup"><span data-stu-id="91109-114">MAPI defines these two message text properties and mechanisms for conversion between them so that RTF-aware clients can interoperate with clients and messaging systems that do not support formatted text.</span></span>
  
### 

[<span data-ttu-id="91109-115">Synchronisieren von Text und Formatierung</span><span class="sxs-lookup"><span data-stu-id="91109-115">Synchronizing Text and Formatting</span></span>](synchronizing-text-and-formatting.md)
  
> <span data-ttu-id="91109-116">Beschreibt, wie RTF Nachrichtentext synchronisiert mit der Formatierung beibehalten.</span><span class="sxs-lookup"><span data-stu-id="91109-116">Describes how to keep RTF message text synchronized with the formatting.</span></span>
    
[<span data-ttu-id="91109-117">Unterstützung von formatierten Text in ausgehenden Nachrichten: Client Zuständigkeiten</span><span class="sxs-lookup"><span data-stu-id="91109-117">Supporting Formatted Text in Outgoing Messages: Client Responsibilities</span></span>](supporting-formatted-text-in-outgoing-messages-client-responsibilities.md)
  
> <span data-ttu-id="91109-118">Beschreibt die Client-Anwendung Aufgaben zur Unterstützung von formatierten Texts in ausgehenden Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="91109-118">Describes client application responsibilities for supporting formatted text in outgoing messages.</span></span>
    
[<span data-ttu-id="91109-119">Unterstützung von formatierten Text in eingehenden Nachrichten: Client Zuständigkeiten</span><span class="sxs-lookup"><span data-stu-id="91109-119">Supporting Formatted Text in Incoming Messages: Client Responsibilities</span></span>](supporting-formatted-text-in-incoming-messages-client-responsibilities.md)
  
> <span data-ttu-id="91109-120">Client-Anwendung Aufgaben zur Unterstützung von formatierten Texts in eingehenden Nachrichten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="91109-120">Describes client application responsibilities for supporting formatted text in incoming messages.</span></span>
    
[<span data-ttu-id="91109-121">Unterstützende formatierter Text: Nachrichtenspeicher Zuständigkeiten</span><span class="sxs-lookup"><span data-stu-id="91109-121">Supporting Formatted Text: Message Store Responsibilities</span></span>](supporting-formatted-text-message-store-responsibilities.md)
  
> <span data-ttu-id="91109-122">Beschreibt Nachricht Store Verantwortung für die Unterstützung von formatierten Texts.</span><span class="sxs-lookup"><span data-stu-id="91109-122">Describes message store responsibilities for supporting formatted text.</span></span>
    
[<span data-ttu-id="91109-123">Unterstützen formatierter Text: Rendern von Anlagen</span><span class="sxs-lookup"><span data-stu-id="91109-123">Supporting Formatted Text: Rendering Attachments</span></span>](supporting-formatted-text-rendering-attachments.md)
  
> <span data-ttu-id="91109-124">Beschreibt, wie auswählen, in dem Anlagen gerendert werden.</span><span class="sxs-lookup"><span data-stu-id="91109-124">Describes how to choose where attachments are rendered.</span></span>
    
[<span data-ttu-id="91109-125">Unterstützung von formatierten Text: Gateway Zuständigkeiten</span><span class="sxs-lookup"><span data-stu-id="91109-125">Supporting Formatted Text: Gateway Responsibilities</span></span>](supporting-formatted-text-gateway-responsibilities.md)
  
> <span data-ttu-id="91109-126">Beschreibt die Gateway Zuständigkeiten für ausgehenden und eingehenden formatierter Text-Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="91109-126">Describes the gateway responsibilities for outgoing and incoming formatted text messages.</span></span>
    
