---
title: IMAPIViewContextGetPrintSetup
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewContext.GetPrintSetup
api_type:
- COM
ms.assetid: eaf3bafb-975d-42c8-99ea-7f9ef9c934ba
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a58e723113f70c10b5c8468f5bdd0d8d9014bd2c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425127"
---
# <a name="imapiviewcontextgetprintsetup"></a><span data-ttu-id="9fe13-103">IMAPIViewContext::GetPrintSetup</span><span class="sxs-lookup"><span data-stu-id="9fe13-103">IMAPIViewContext::GetPrintSetup</span></span>

  
  
<span data-ttu-id="9fe13-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9fe13-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9fe13-105">Ruft aktuelle Druckinformationen ab.</span><span class="sxs-lookup"><span data-stu-id="9fe13-105">Retrieves current printing information.</span></span>
  
```cpp
HRESULT GetPrintSetup(
ULONG ulFlags,
LPFORMPRINTSETUP FAR * lppFormPrintSetup
);
```

## <a name="parameters"></a><span data-ttu-id="9fe13-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9fe13-106">Parameters</span></span>

 <span data-ttu-id="9fe13-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9fe13-107">_ulFlags_</span></span>
  
> <span data-ttu-id="9fe13-108">[in] Bitmaske von Flags, die den Typ der zurückgegebenen Zeichenfolgen steuert.</span><span class="sxs-lookup"><span data-stu-id="9fe13-108">[in] Bitmask of flags that controls the type of the returned strings.</span></span> <span data-ttu-id="9fe13-109">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="9fe13-109">The following flag can be set:</span></span>
    
<span data-ttu-id="9fe13-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="9fe13-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="9fe13-111">Die zurückgegebenen Zeichenfolgen sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="9fe13-111">The returned strings are in Unicode format.</span></span> <span data-ttu-id="9fe13-112">Wenn das MAPI_UNICODE nicht festgelegt ist, befinden sich die Zeichenfolgen im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="9fe13-112">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="9fe13-113">_lppFormPrintSetup_</span><span class="sxs-lookup"><span data-stu-id="9fe13-113">_lppFormPrintSetup_</span></span>
  
> <span data-ttu-id="9fe13-114">[out] Zeiger auf einen Zeiger auf eine Struktur, die die Druckinformationen enthält.</span><span class="sxs-lookup"><span data-stu-id="9fe13-114">[out] Pointer to a pointer to a structure that holds the printing information.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9fe13-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9fe13-115">Return value</span></span>

<span data-ttu-id="9fe13-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="9fe13-116">S_OK</span></span> 
  
> <span data-ttu-id="9fe13-117">Die Druckinformationen wurden erfolgreich abgerufen.</span><span class="sxs-lookup"><span data-stu-id="9fe13-117">The printing information was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9fe13-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9fe13-118">Remarks</span></span>

<span data-ttu-id="9fe13-119">Formularobjekte rufen die **IMAPIViewContext::GetPrintSetup-Methode** auf, um Informationen zum Druckersetup abzurufen, bevor versucht wird, die aktuelle Nachricht zu drucken.</span><span class="sxs-lookup"><span data-stu-id="9fe13-119">Form objects call the **IMAPIViewContext::GetPrintSetup** method to retrieve information about the printer setup before attempting to print the current message.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="9fe13-120">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="9fe13-120">Notes to implementers</span></span>

<span data-ttu-id="9fe13-121">Weisen Sie **die Mitglieder hDevMode** und **hDevName** der [FORMPRINTSETUP-Struktur](formprintsetup.md) mithilfe der Win32-Funktion **GlobalAlloc zu.**</span><span class="sxs-lookup"><span data-stu-id="9fe13-121">Allocate the **hDevMode** and **hDevName** members of the [FORMPRINTSETUP](formprintsetup.md) structure using the Win32 function **GlobalAlloc**.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="9fe13-122">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="9fe13-122">Notes to callers</span></span>

<span data-ttu-id="9fe13-123">Wenn Sie erwarten, dass **die Elemente hDevMode** und **hDevName** der **FORMPRINTSETUP-Struktur,** auf die der  _lppFormPrintSetup-Parameter_ verweist, Unicode-Zeichenfolgen sind, legen Sie  _ulFlags_ auf MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="9fe13-123">If you expect the **hDevMode** and **hDevName** members of the **FORMPRINTSETUP** structure pointed to by the  _lppFormPrintSetup_ parameter to be Unicode strings, set  _ulFlags_ to MAPI_UNICODE.</span></span> <span data-ttu-id="9fe13-124">Andernfalls **gibt GetPrintSetup** diese Zeichenfolgen im ANSI-Format zurück.</span><span class="sxs-lookup"><span data-stu-id="9fe13-124">Otherwise, **GetPrintSetup** will return these strings in ANSI format.</span></span> 
  
<span data-ttu-id="9fe13-125">Geben Sie **die Mitglieder hDevMode** und **hDevName** der **FORMPRINTSETUP-Struktur** frei, indem Sie die Win32-Funktion **GlobalFree aufrufen.**</span><span class="sxs-lookup"><span data-stu-id="9fe13-125">Free the **hDevMode** and **hDevName** members of the **FORMPRINTSETUP** structure by calling the Win32 function **GlobalFree**.</span></span> <span data-ttu-id="9fe13-126">Geben Sie die gesamte **FORMPRINTSETUP-Struktur** frei, indem Sie [MAPIFreeBuffer aufrufen.](mapifreebuffer.md)</span><span class="sxs-lookup"><span data-stu-id="9fe13-126">Free the entire **FORMPRINTSETUP** structure by calling [MAPIFreeBuffer](mapifreebuffer.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9fe13-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9fe13-127">See also</span></span>



[<span data-ttu-id="9fe13-128">FORMPRINTSETUP</span><span class="sxs-lookup"><span data-stu-id="9fe13-128">FORMPRINTSETUP</span></span>](formprintsetup.md)
  
[<span data-ttu-id="9fe13-129">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9fe13-129">IMAPIViewContext : IUnknown</span></span>](imapiviewcontextiunknown.md)

