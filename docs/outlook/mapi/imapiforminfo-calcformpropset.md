---
title: IMAPIFormInfoCalcFormPropSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormInfo.CalcFormPropSet
api_type:
- COM
ms.assetid: cc3ffb8d-9cc4-47d3-9aa9-02c3a5b7775c
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 0b62c21348da71c1ee863f70d6e6a549a5d10003
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438071"
---
# <a name="imapiforminfocalcformpropset"></a><span data-ttu-id="fac78-103">IMAPIFormInfo::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="fac78-103">IMAPIFormInfo::CalcFormPropSet</span></span>

  
  
<span data-ttu-id="fac78-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fac78-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fac78-105">Gibt einen Zeiger auf den vollständigen Satz von Eigenschaften zurück, den ein Formular verwendet.</span><span class="sxs-lookup"><span data-stu-id="fac78-105">Returns a pointer to the complete set of properties that a form uses.</span></span>
  
```cpp
HRESULT CalcFormPropSet(
  ULONG ulFlags,
  LPMAPIFORMPROPARRAY FAR * ppFormPropArray
);
```

## <a name="parameters"></a><span data-ttu-id="fac78-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="fac78-106">Parameters</span></span>

 <span data-ttu-id="fac78-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="fac78-107">_ulFlags_</span></span>
  
> <span data-ttu-id="fac78-108">[in] Eine Bitmaske mit Flags, die den Typ der zurückgegebenen Zeichenfolgen steuert.</span><span class="sxs-lookup"><span data-stu-id="fac78-108">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="fac78-109">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="fac78-109">The following flag can be set:</span></span>
    
<span data-ttu-id="fac78-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="fac78-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="fac78-111">Die zurückgegebenen Zeichenfolgen sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="fac78-111">The returned strings are in Unicode format.</span></span> <span data-ttu-id="fac78-112">Wenn das MAPI_UNICODE nicht festgelegt ist, befinden sich die Zeichenfolgen im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="fac78-112">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="fac78-113">_ppFormPropArray_</span><span class="sxs-lookup"><span data-stu-id="fac78-113">_ppFormPropArray_</span></span>
  
> <span data-ttu-id="fac78-114">[out] Ein Zeiger auf einen Zeiger auf die zurückgegebene [SMAPIFormPropArray-Struktur.](smapiformproparray.md)</span><span class="sxs-lookup"><span data-stu-id="fac78-114">[out] A pointer to a pointer to the returned [SMAPIFormPropArray](smapiformproparray.md) structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="fac78-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fac78-115">Return value</span></span>

<span data-ttu-id="fac78-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="fac78-116">S_OK</span></span> 
  
> <span data-ttu-id="fac78-117">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="fac78-117">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="fac78-118">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="fac78-118">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="fac78-119">Entweder wurde MAPI_UNICODE-Flag festgelegt, und die Implementierung unterstützt unicode nicht, oder MAPI_UNICODE wurde nicht festgelegt, und die Implementierung unterstützt nur Unicode.</span><span class="sxs-lookup"><span data-stu-id="fac78-119">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="fac78-120">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="fac78-120">MFCMAPI reference</span></span>

<span data-ttu-id="fac78-121">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="fac78-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="fac78-122">**Datei**</span><span class="sxs-lookup"><span data-stu-id="fac78-122">**File**</span></span>|<span data-ttu-id="fac78-123">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="fac78-123">**Function**</span></span>|<span data-ttu-id="fac78-124">**Comment**</span><span class="sxs-lookup"><span data-stu-id="fac78-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="fac78-125">MFCOutput.cpp</span><span class="sxs-lookup"><span data-stu-id="fac78-125">MFCOutput.cpp</span></span>  <br/> |<span data-ttu-id="fac78-126">_OutputFormInfo</span><span class="sxs-lookup"><span data-stu-id="fac78-126">_OutputFormInfo</span></span>  <br/> |<span data-ttu-id="fac78-127">MFCMAPI verwendet die **IMAPIFormInfo::CalcFormPropSet-Methode** beim Schreiben der Debugausgabe für Formularinformationsobjekte.</span><span class="sxs-lookup"><span data-stu-id="fac78-127">MFCMAPI uses the **IMAPIFormInfo::CalcFormPropSet** method when writing debug output for form information objects.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fac78-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fac78-128">See also</span></span>



[<span data-ttu-id="fac78-129">SMAPIFormPropArray</span><span class="sxs-lookup"><span data-stu-id="fac78-129">SMAPIFormPropArray</span></span>](smapiformproparray.md)
  
[<span data-ttu-id="fac78-130">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="fac78-130">IMAPIFormInfo : IMAPIProp</span></span>](imapiforminfoimapiprop.md)


[<span data-ttu-id="fac78-131">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="fac78-131">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

