---
title: Algorithmus für die Eintrags-IDs und Anlage IDs codieren
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: b9ae6679-99b7-6509-74d4-12aa13d54928
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 710ba5173dcce6e948e1f49c7d82e46bc83b8200
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791300"
---
# <a name="algorithm-to-encode-entry-ids-and-attachment-ids"></a><span data-ttu-id="a00d2-103">Algorithmus für die Eintrags-IDs und Anlage IDs codieren</span><span class="sxs-lookup"><span data-stu-id="a00d2-103">Algorithm to Encode Entry IDs and Attachment IDs</span></span>

  
  
<span data-ttu-id="a00d2-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a00d2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a00d2-105">Ein Anbieter anmelden kann im Rahmen einer MAPI-Uniform Resource Locator (URL) senden eine Eintrags-ID und eine Anlage-ID an der MAPI-Protokollhandler, um ein Objekt zu identifizieren, die für die Indizierung bereit ist.</span><span class="sxs-lookup"><span data-stu-id="a00d2-105">A store provider can send as part of a MAPI Uniform Resource Locator (URL) an entry ID and an attachment ID to the MAPI Protocol Handler to identify an object that is ready for indexing.</span></span> <span data-ttu-id="a00d2-106">Speicheranbieter codiert die Eintrags-ID und Anlagen-ID als Unicode-Zeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="a00d2-106">The store provider encodes the entry ID and attachment ID as Unicode strings.</span></span> <span data-ttu-id="a00d2-107">In diesem Thema wird einen Algorithmus, der eine kompakte Darstellung des Eintrags-ID oder der Anlage-ID generiert.</span><span class="sxs-lookup"><span data-stu-id="a00d2-107">This topic shows an algorithm that generates a compact representation of the entry ID or attachment ID.</span></span>
  
```cpp
const WORD kwBaseOffset = 0xAC00;  // Hangul char range (AC00-D7AF) 
LPWSTR EncodeID(ULONG cbEID, LPENTRYID rgbID) 
{ 
    ULONG   i = 0; 
    LPWSTR  pwzDst = NULL; 
    LPBYTE  pbSrc = NULL; 
    LPWSTR  pwzIDEncoded = NULL; 
 
    // rgbID is the item Entry ID or the attachment ID 
    // cbID is the size in bytes of rgbID 
 
    // Allocate memory for pwzIDEncoded 
    pwzIDEncoded = new WCHAR[cbEID]; 
    if (!pwzIDEncoded) return NULL; 
 
    for (i = 0, pbSrc = (LPBYTE)rgbID, pwzDst = pwzIDEncoded; 
        i < cbEID; 
        i++, pbSrc++, pwzDst++) 
    { 
        *pwzDst = (WCHAR) (*pbSrc + kwBaseOffset); 
    } 
 
    // Ensure NULL terminated 
    *pwzDst = L'\0'; 
 
    // pwzIDEncoded now contains the entry ID encoded. 
    return pwzIDEncoded; 
}
```

## <a name="see-also"></a><span data-ttu-id="a00d2-108">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a00d2-108">See also</span></span>



[<span data-ttu-id="a00d2-109">Informationen über die Benachrichtigung-basierten Speicher Indizierung</span><span class="sxs-lookup"><span data-stu-id="a00d2-109">About Notification-Based Store Indexing</span></span>](about-notification-based-store-indexing.md)
  
[<span data-ttu-id="a00d2-110">Informationen zu MAPI-URLs für die Benachrichtigung-basierte Indizierung</span><span class="sxs-lookup"><span data-stu-id="a00d2-110">About MAPI URLs for Notification-Based Indexing</span></span>](about-mapi-urls-for-notification-based-indexing.md)
