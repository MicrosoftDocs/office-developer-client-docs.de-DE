---
title: FBinFromHex
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FBinFromHex
api_type:
- COM
ms.assetid: 47e6c576-bd99-4410-8e41-7dd3159b23b7
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 55c7deec9d29ae22a07b2f5ccd1c832d56782c03
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414935"
---
# <a name="fbinfromhex"></a><span data-ttu-id="5dd88-103">FBinFromHex</span><span class="sxs-lookup"><span data-stu-id="5dd88-103">FBinFromHex</span></span>

  
  
<span data-ttu-id="5dd88-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5dd88-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5dd88-105">Konvertiert eine Zeichenfolgendarstellung einer Hexadezimalzahl in Binärdaten.</span><span class="sxs-lookup"><span data-stu-id="5dd88-105">Converts a string representation of a hexadecimal number to binary data.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5dd88-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="5dd88-106">Header file:</span></span>  <br/> |<span data-ttu-id="5dd88-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="5dd88-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="5dd88-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="5dd88-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="5dd88-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="5dd88-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="5dd88-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="5dd88-110">Called by:</span></span>  <br/> |<span data-ttu-id="5dd88-111">Clientanwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="5dd88-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
BOOL FBinFromHex(
  LPSTR sz,
  LPBYTE pb
);
```

## <a name="parameters"></a><span data-ttu-id="5dd88-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="5dd88-112">Parameters</span></span>

 <span data-ttu-id="5dd88-113">_sz_</span><span class="sxs-lookup"><span data-stu-id="5dd88-113">_sz_</span></span>
  
> <span data-ttu-id="5dd88-114">[in] Zeiger auf die mit Null beendete ASCII-Zeichenfolge, die konvertiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="5dd88-114">[in] Pointer to the null-terminated ASCII string to be converted.</span></span> <span data-ttu-id="5dd88-115">Es handelt sich nicht um eine Unicode-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="5dd88-115">It is not a Unicode string.</span></span> <span data-ttu-id="5dd88-116">Gültige Zeichen sind die Hexadezimalzeichen Null bis neun sowie die Groß- und Kleinbuchstaben A bis F.</span><span class="sxs-lookup"><span data-stu-id="5dd88-116">Valid characters include the hexadecimal characters zero through nine and both uppercase and lowercase characters A through F.</span></span>
    
 <span data-ttu-id="5dd88-117">_pb_</span><span class="sxs-lookup"><span data-stu-id="5dd88-117">_pb_</span></span>
  
> <span data-ttu-id="5dd88-118">[out] Zeiger auf die zurückgegebene Binärnummer.</span><span class="sxs-lookup"><span data-stu-id="5dd88-118">[out] Pointer to the returned binary number.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5dd88-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5dd88-119">Return value</span></span>

<span data-ttu-id="5dd88-120">TRUE</span><span class="sxs-lookup"><span data-stu-id="5dd88-120">TRUE</span></span> 
  
> <span data-ttu-id="5dd88-121">Die Zeichenfolge wurde erfolgreich in eine binäre Zahl konvertiert.</span><span class="sxs-lookup"><span data-stu-id="5dd88-121">The string was successfully converted into a binary number.</span></span> 
    
<span data-ttu-id="5dd88-122">FALSE</span><span class="sxs-lookup"><span data-stu-id="5dd88-122">FALSE</span></span> 
  
> <span data-ttu-id="5dd88-123">Die Eingabezeichenfolge enthält ungültige ASCII-Hexadezimalzeichen.</span><span class="sxs-lookup"><span data-stu-id="5dd88-123">The input string contains invalid ASCII hexadecimal characters.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5dd88-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5dd88-124">See also</span></span>



[<span data-ttu-id="5dd88-125">ScBinFromHexBounded</span><span class="sxs-lookup"><span data-stu-id="5dd88-125">ScBinFromHexBounded</span></span>](scbinfromhexbounded.md)

