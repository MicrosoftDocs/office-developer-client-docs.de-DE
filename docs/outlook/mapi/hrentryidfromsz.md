---
title: HrEntryIDFromSz
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrEntryIDFromSz
api_type:
- COM
ms.assetid: 14c171ec-0aec-43ab-8be8-e6bc0ce28a58
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 2b7ef789c80f85f3539ec3bbd0caf4a8adc50f3e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791920"
---
# <a name="hrentryidfromsz"></a><span data-ttu-id="51b38-103">HrEntryIDFromSz</span><span class="sxs-lookup"><span data-stu-id="51b38-103">HrEntryIDFromSz</span></span>

  
  
<span data-ttu-id="51b38-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="51b38-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="51b38-105">Erstellt eine Eintrags-ID aus der ASCII-Codierung neu.</span><span class="sxs-lookup"><span data-stu-id="51b38-105">Recreates an entry identifier from its ASCII encoding.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="51b38-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="51b38-106">Header file:</span></span>  <br/> |<span data-ttu-id="51b38-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="51b38-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="51b38-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="51b38-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="51b38-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="51b38-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="51b38-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="51b38-110">Called by:</span></span>  <br/> |<span data-ttu-id="51b38-111">Clientanwendungen</span><span class="sxs-lookup"><span data-stu-id="51b38-111">Client applications</span></span>  <br/> |
   
```cpp
HRESULT HrEntryIDFromSz(
  LPSTR sz,
  ULONG FAR * pcb,
  LPENTRYID FAR * ppentry
);
```

## <a name="parameters"></a><span data-ttu-id="51b38-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="51b38-112">Parameters</span></span>

 <span data-ttu-id="51b38-113">_su_</span><span class="sxs-lookup"><span data-stu-id="51b38-113">_sz_</span></span>
  
> <span data-ttu-id="51b38-114">[in] Zeiger auf die ASCII-Zeichenfolge aus dem Eintrags-ID erstellt.</span><span class="sxs-lookup"><span data-stu-id="51b38-114">[in] Pointer to the ASCII string from which to create an entry identifier.</span></span> 
    
 <span data-ttu-id="51b38-115">_PCB_</span><span class="sxs-lookup"><span data-stu-id="51b38-115">_pcb_</span></span>
  
> <span data-ttu-id="51b38-116">[out] Zeiger auf die Größe des Eintrags-ID, die auf das durch den Parameter _Ppentry_ in Bytes.</span><span class="sxs-lookup"><span data-stu-id="51b38-116">[out] Pointer to the size, in bytes, of the entry identifier pointed to by the  _ppentry_ parameter.</span></span> 
    
 <span data-ttu-id="51b38-117">_ppentry_</span><span class="sxs-lookup"><span data-stu-id="51b38-117">_ppentry_</span></span>
  
> <span data-ttu-id="51b38-118">[out] Zeiger auf einen Zeiger auf das zurückgegebene [ENTRYID](entryid.md) -Struktur, die neuen Eintrags-ID enthält.</span><span class="sxs-lookup"><span data-stu-id="51b38-118">[out] Pointer to a pointer to the returned [ENTRYID](entryid.md) structure that contains the new entry identifier.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="51b38-119">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="51b38-119">Return value</span></span>

<span data-ttu-id="51b38-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="51b38-120">S_OK</span></span>
  
> <span data-ttu-id="51b38-121">Erneutes Erstellen war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="51b38-121">The recreation was successful.</span></span>
    
<span data-ttu-id="51b38-122">MAPI_E_INVALID_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="51b38-122">MAPI_E_INVALID_ENTRYID</span></span>
  
> <span data-ttu-id="51b38-123">Die Eintrags-ID ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="51b38-123">The entry ID was invalid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="51b38-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="51b38-124">Remarks</span></span>

<span data-ttu-id="51b38-125">Die Funktionen **HrEntryIDFromSz** und [HrSzFromEntryID](hrszfromentryid.md) bieten eine Konvertierung zwischen der Zeichenfolge und der binären Formate der Eintragsbezeichner.</span><span class="sxs-lookup"><span data-stu-id="51b38-125">The **HrEntryIDFromSz** and [HrSzFromEntryID](hrszfromentryid.md) functions provide conversion between the string and binary formats of entry identifiers.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="51b38-126">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="51b38-126">Notes to callers</span></span>

<span data-ttu-id="51b38-127">Die **HrEntryIDFromSz** -Funktion weist Speicher für die Verwendung der Funktion [MAPIAllocateBuffer](mapiallocatebuffer.md) ASCII-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="51b38-127">The **HrEntryIDFromSz** function allocates memory for the ASCII string using the [MAPIAllocateBuffer](mapiallocatebuffer.md) function.</span></span> 
  
