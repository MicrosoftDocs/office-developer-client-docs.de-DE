---
title: MNLS_MultiByteToWideChar
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 065d78bf-4c9c-48dd-b1f1-b4e59f3f1243
description: 'Zuletzt geändert: 21 Februar 2012'
ms.openlocfilehash: ab082c8ac70bf851097080fb41033f76bccc3044
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793276"
---
# <a name="mnlsmultibytetowidechar"></a><span data-ttu-id="2d069-103">MNLS_MultiByteToWideChar</span><span class="sxs-lookup"><span data-stu-id="2d069-103">MNLS_MultiByteToWideChar</span></span>

  
  
<span data-ttu-id="2d069-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2d069-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2d069-105">Vergleichbar mit der **MultiByteToWideChar**, der eine Zeichenfolge in einen String UTF-16 (Breitzeichen) zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="2d069-105">Similar to **MultiByteToWideChar**, which maps a character string to a UTF-16 (wide character) string.</span></span> <span data-ttu-id="2d069-106">Die Zeichenfolge ist nicht unbedingt aus einem multibyte-Zeichen festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2d069-106">The character string is not necessarily from a multibyte character set.</span></span>
  
```cpp
int MNLS_MultiByteToWideChar(
  UINT uCodePage,
  DWORD dwFlags,
  LPCSTR lpMultiByteStr,
  int cchMultiByte,
  LPWSTR lpWideCharStr,
  int cchWideChar);
```

## <a name="parameters"></a><span data-ttu-id="2d069-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="2d069-107">Parameters</span></span>

 <span data-ttu-id="2d069-108">_uCodePage_</span><span class="sxs-lookup"><span data-stu-id="2d069-108">_uCodePage_</span></span>
  
> <span data-ttu-id="2d069-109">[in] Codepage verwendet wird, in die Konvertierung ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2d069-109">[in] Code page to use in performing the conversion.</span></span>
    
 <span data-ttu-id="2d069-110">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="2d069-110">_dwFlags_</span></span>
  
> <span data-ttu-id="2d069-111">[in] Flags, die den Typ für die Konvertierung angibt.</span><span class="sxs-lookup"><span data-stu-id="2d069-111">[in] Flags indicating the conversion type.</span></span>
    
 <span data-ttu-id="2d069-112">_lpMultiByteStr_</span><span class="sxs-lookup"><span data-stu-id="2d069-112">_lpMultiByteStr_</span></span>
  
> <span data-ttu-id="2d069-113">[in] Zeiger auf die Zeichenfolge zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="2d069-113">[in] Pointer to the character string to convert.</span></span>
    
 <span data-ttu-id="2d069-114">_cchMultiByte_</span><span class="sxs-lookup"><span data-stu-id="2d069-114">_cchMultiByte_</span></span>
  
> <span data-ttu-id="2d069-115">[in] Größe in Bytes, der von der _LpMultiByteStr_ -Parameter angegebene Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="2d069-115">[in] Size, in bytes, of the string indicated by the  _lpMultiByteStr_ parameter.</span></span> 
    
 <span data-ttu-id="2d069-116">_lpWideCharStr_</span><span class="sxs-lookup"><span data-stu-id="2d069-116">_lpWideCharStr_</span></span>
  
> <span data-ttu-id="2d069-117">[out] Optional.</span><span class="sxs-lookup"><span data-stu-id="2d069-117">[out] Optional.</span></span> <span data-ttu-id="2d069-118">Zeiger auf einen Puffer, der die konvertierte Zeichenfolge empfängt.</span><span class="sxs-lookup"><span data-stu-id="2d069-118">Pointer to a buffer that receives the converted string.</span></span>
    
 <span data-ttu-id="2d069-119">_cchWideChar_</span><span class="sxs-lookup"><span data-stu-id="2d069-119">_cchWideChar_</span></span>
  
> <span data-ttu-id="2d069-120">[in] Größe des Puffers durch _LpWideCharStr_in Zeichen.</span><span class="sxs-lookup"><span data-stu-id="2d069-120">[in] Size, in characters, of the buffer indicated by  _lpWideCharStr_.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2d069-121">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="2d069-121">Return value</span></span>

<span data-ttu-id="2d069-122">Gibt die Anzahl der Zeichen in den Puffer angegeben durch _LpWideCharStr_ bei erfolgreicher geschriebenen zurück.</span><span class="sxs-lookup"><span data-stu-id="2d069-122">Returns the number of characters written to the buffer indicated by  _lpWideCharStr_ if successful.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="2d069-123">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2d069-123">Remarks</span></span>

<span data-ttu-id="2d069-124">Diese Funktion wird die Funktion **MultiByteToWideChar** umbrochen.</span><span class="sxs-lookup"><span data-stu-id="2d069-124">This function wraps the **MultiByteToWideChar** function.</span></span> <span data-ttu-id="2d069-125">Weitere Informationen finden Sie unter [MultiByteToWideChar](http://msdn.microsoft.com/de-de/library/dd319072%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="2d069-125">For more information, see [MultiByteToWideChar](http://msdn.microsoft.com/de-de/library/dd319072%28VS.85%29.aspx).</span></span>
  
