---
title: Unterstützung für RTF-Text für Nachrichtenspeicher-Anbieter
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0022fe70-cf11-49a5-9c97-a6bc5b5b13aa
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: d7d64c8a7d4df4898502f4574ca879c736547b37
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795693"
---
# <a name="supporting-rtf-text-for-message-store-providers"></a><span data-ttu-id="7ad17-103">Unterstützung für RTF-Text für Nachrichtenspeicher-Anbieter</span><span class="sxs-lookup"><span data-stu-id="7ad17-103">Supporting RTF Text for Message Store Providers</span></span>

  
  
<span data-ttu-id="7ad17-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7ad17-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7ad17-105">Einige Clientanwendungen können Benutzer Rich Text Format (RTF) Text in ihren Nachrichten verwenden.</span><span class="sxs-lookup"><span data-stu-id="7ad17-105">Some client applications allow users to use Rich Text Format (RTF) text in their messages.</span></span> <span data-ttu-id="7ad17-106">Wenn Ihre Nachricht Anbieter muss zur Unterstützung von RTF-Text in Nachrichten gespeichert werden sollen, muss es zur Behandlung der Eigenschaft **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)), zusätzlich zu den **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md))-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="7ad17-106">If your message store provider needs to support RTF text in messages, it needs to handle the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property, in addition to the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property.</span></span> <span data-ttu-id="7ad17-107">In erster Linie, bedeutet dies beide Eigenschaften speichern und dabei sicherstellen, dass **PR_BODY** eine nur-Text-Version des Texts in **PR_RTF_COMPRESSED**enthält.</span><span class="sxs-lookup"><span data-stu-id="7ad17-107">Primarily, this means storing both properties, and making sure that **PR_BODY** contains a plain text version of the text in **PR_RTF_COMPRESSED**.</span></span> <span data-ttu-id="7ad17-108">Die Funktion [RTFSync](rtfsync.md) eignet sich für diesen Zweck.</span><span class="sxs-lookup"><span data-stu-id="7ad17-108">The [RTFSync](rtfsync.md) function is useful for this purpose.</span></span> 
  
<span data-ttu-id="7ad17-109">Es gibt zwei Flags, die in der Nachricht Store-Objekt **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))-Eigenschaft festgelegt werden können, die Clients mitteilen, was sie vom Anbieter für die Nachricht im Hinblick auf die **PR_BODY** und **PR_ erwarten können RTF_COMPRESSED** Nachrichten im Nachrichtenspeicher-Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="7ad17-109">There are two flags that can be set in the message store object's **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property that tell clients what they can expect from the message store provider with respect to the **PR_BODY** and **PR_RTF_COMPRESSED** properties on messages in the message store.</span></span> <span data-ttu-id="7ad17-110">Das STORE_RTF_OK-Flag gibt an, dass der Speicher den Wert der Eigenschaft **PR_BODY** aus der Eigenschaft **PR_RTF_COMPRESSED** dynamisch der Benutzer von der Last generieren kann des sie explizit synchronisieren entlastet.</span><span class="sxs-lookup"><span data-stu-id="7ad17-110">The STORE_RTF_OK flag indicates that the store can generate the value of the **PR_BODY** property from the **PR_RTF_COMPRESSED** property dynamically, which relieves clients from the burden of synchronizing them explicitly.</span></span> <span data-ttu-id="7ad17-111">Das STORE_UNCOMPRESSED_RTF-Flag gibt an, dass die Nachricht Informationsdienst nicht komprimierte Daten in **PR_RTF_COMPRESSED**unterstützen kann.</span><span class="sxs-lookup"><span data-stu-id="7ad17-111">The STORE_UNCOMPRESSED_RTF flag indicates that the message store provider can support uncompressed data in **PR_RTF_COMPRESSED**.</span></span>
  
<span data-ttu-id="7ad17-112">Die Eigenschaft **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) zu löschen, wenn die **PR_BODY** -Eigenschaft geändert wird, um ordnungsgemäß mit Clientanwendungen interagieren, die RTF-Text unterstützen müssen Nachricht-Anbieter, die keine für RTF-Text Unterstützung .</span><span class="sxs-lookup"><span data-stu-id="7ad17-112">Message store providers that do not support RTF text need to delete the **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) property when the **PR_BODY** property changes in order to interoperate properly with client applications that do support RTF text.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7ad17-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7ad17-113">See also</span></span>



[<span data-ttu-id="7ad17-114">Nachrichtenspeicher-Features</span><span class="sxs-lookup"><span data-stu-id="7ad17-114">Message Store Features</span></span>](message-store-features.md)
