---
title: SzFindLastCh
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SzFindLastCh
api_type:
- COM
ms.assetid: 7c3e5a71-7b78-4328-b8ee-265cc4da4be5
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f22d30c1bc7c797834f58bcd1306b14ac2542c6d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421256"
---
# <a name="szfindlastch"></a><span data-ttu-id="60eec-103">SzFindLastCh</span><span class="sxs-lookup"><span data-stu-id="60eec-103">SzFindLastCh</span></span>

  
  
<span data-ttu-id="60eec-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="60eec-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="60eec-105">Sucht nach dem letzten Vorkommen eines Zeichens in einer mit Null beendeten Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="60eec-105">Searches for the last occurrence of a character in a null-terminated string.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="60eec-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="60eec-106">Header file:</span></span>  <br/> |<span data-ttu-id="60eec-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="60eec-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="60eec-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="60eec-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="60eec-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="60eec-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="60eec-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="60eec-110">Called by:</span></span>  <br/> |<span data-ttu-id="60eec-111">Clientanwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="60eec-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LPSTR SzFindLastCh(
  LPCSTR lpsz,
  USHORT ch
);
```

## <a name="parameters"></a><span data-ttu-id="60eec-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="60eec-112">Parameters</span></span>

 <span data-ttu-id="60eec-113">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="60eec-113">_lpsz_</span></span>
  
> <span data-ttu-id="60eec-114">[in] Zeiger auf die zu durchsuchende Zeichenfolge, die mit Nullen beendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="60eec-114">[in] Pointer to the null-terminated string to be searched.</span></span> 
    
 <span data-ttu-id="60eec-115">_ch_</span><span class="sxs-lookup"><span data-stu-id="60eec-115">_ch_</span></span>
  
> <span data-ttu-id="60eec-116">[in] Das zu durchsuchende Zeichen.</span><span class="sxs-lookup"><span data-stu-id="60eec-116">[in] The character to be searched for.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="60eec-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="60eec-117">Return value</span></span>

 <span data-ttu-id="60eec-118">**SzFindLastCh** gibt einen Zeiger auf das letzte Vorkommen des Zeichens in der Zeichenfolge zurück.</span><span class="sxs-lookup"><span data-stu-id="60eec-118">**SzFindLastCh** returns a pointer to the last occurrence of the character in the string.</span></span> <span data-ttu-id="60eec-119">Wenn das Zeichen nicht an einer beliebigen Stelle in der Zeichenfolge auftritt, oder wenn der  _lpsz-Parameter_ NULL ist, wird der Wert NULL zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="60eec-119">If the character does not occur anywhere in the string, or if the  _lpsz_ parameter is NULL, a value of NULL is returned.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="60eec-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="60eec-120">Remarks</span></span>

<span data-ttu-id="60eec-121">Die **SzFindLastCh-Funktion** sucht nur nach einer genauen Übereinstimmung. es ist sensibel auf Fall- und diakritische Unterschiede.</span><span class="sxs-lookup"><span data-stu-id="60eec-121">The **SzFindLastCh** function searches for an exact match only; it is sensitive to case and diacritical differences.</span></span> <span data-ttu-id="60eec-122">Suchen im Unicode- und DBCS-Format werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="60eec-122">Searches in the Unicode and DBCS formats are supported.</span></span> 
  

