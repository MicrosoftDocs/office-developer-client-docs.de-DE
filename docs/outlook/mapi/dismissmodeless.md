---
title: DISMISSMODELESS
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DISMISSMODELESS
api_type:
- COM
ms.assetid: ef93ef3d-c159-40ae-9b8d-0af8a0567565
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: dd962515a85cb6a4b8661a0fd5294cea55cd6e96
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428186"
---
# <a name="dismissmodeless"></a><span data-ttu-id="0b28d-103">DISMISSMODELESS</span><span class="sxs-lookup"><span data-stu-id="0b28d-103">DISMISSMODELESS</span></span>

  
  
<span data-ttu-id="0b28d-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0b28d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0b28d-105">Definiert eine Rückruffunktion, die MAPI aufruft, wenn sie ein Dialogfeld für ein modusloses Adressbuch verworfen hat.</span><span class="sxs-lookup"><span data-stu-id="0b28d-105">Defines a callback function that MAPI calls when it has dismissed a modeless address book dialog box.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0b28d-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="0b28d-106">Header file:</span></span>  <br/> |<span data-ttu-id="0b28d-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0b28d-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="0b28d-108">Definierte Funktion implementiert von:</span><span class="sxs-lookup"><span data-stu-id="0b28d-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="0b28d-109">Clientanwendungen</span><span class="sxs-lookup"><span data-stu-id="0b28d-109">Client applications</span></span>  <br/> |
|<span data-ttu-id="0b28d-110">Definierte Funktion, die von:</span><span class="sxs-lookup"><span data-stu-id="0b28d-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="0b28d-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="0b28d-111">MAPI</span></span>  <br/> |
   
```cpp
void (STDMETHODCALLTYPE DISMISSMODELESS)(
  ULONG_PTR ulUIParam,
  LPVOID lpvContext
);
```

## <a name="parameters"></a><span data-ttu-id="0b28d-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="0b28d-112">Parameters</span></span>

 <span data-ttu-id="0b28d-113">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="0b28d-113">_ulUIParam_</span></span>
  
> <span data-ttu-id="0b28d-114">[in] Ein implementierungsspezifischer Wert, der in der Regel zum Übergeben von Benutzeroberflächeninformationen an eine Funktion verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0b28d-114">[in] An implementation-specific value typically used for passing user interface information to a function.</span></span> <span data-ttu-id="0b28d-115">In Microsoft Windows ist dieser Parameter beispielsweise das übergeordnete Fensterhandle für das Dialogfeld und hat den Typ HWND, wird in ein **ULONG_PTR.**</span><span class="sxs-lookup"><span data-stu-id="0b28d-115">For example, in Microsoft Windows this parameter is the parent window handle for the dialog box and is of type HWND, cast to a **ULONG_PTR**.</span></span> <span data-ttu-id="0b28d-116">Der Wert Null gibt an, dass kein übergeordnetes Fenster besteht.</span><span class="sxs-lookup"><span data-stu-id="0b28d-116">A value of zero indicates there is no parent window.</span></span> 
    
 <span data-ttu-id="0b28d-117">_lpvContext_</span><span class="sxs-lookup"><span data-stu-id="0b28d-117">_lpvContext_</span></span>
  
> <span data-ttu-id="0b28d-118">[in] Zeiger auf einen beliebigen Wert, der an die Rückruffunktion übergeben wird, wenn MAPI ihn aufruft.</span><span class="sxs-lookup"><span data-stu-id="0b28d-118">[in] Pointer to an arbitrary value passed to the callback function when MAPI calls it.</span></span> <span data-ttu-id="0b28d-119">Dieser Wert kann eine Für die Clientanwendung wichtige Adresse darstellen.</span><span class="sxs-lookup"><span data-stu-id="0b28d-119">This value can represent an address of significance to the client application.</span></span> <span data-ttu-id="0b28d-120">In der Regel ist  _lpvContext_ für C++-Code ein Zeiger auf die Adresse einer C++-Objektinstanz.</span><span class="sxs-lookup"><span data-stu-id="0b28d-120">Typically, for C++ code,  _lpvContext_ is a pointer to the address of a C++ object instance.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="0b28d-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0b28d-121">Return value</span></span>

<span data-ttu-id="0b28d-122">Keine</span><span class="sxs-lookup"><span data-stu-id="0b28d-122">None</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0b28d-123">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0b28d-123">Remarks</span></span>

<span data-ttu-id="0b28d-124">Wenn die Clientanwendung ein Dialogfeld ohne Adressbuch aufruft, enthält sie in der Windows-Nachrichtenschleife einen Aufruf einer Funktion basierend auf dem [ACCELERATEABSDI-Prototyp,](accelerateabsdi.md) der nach Zugriffstasten sucht und diese verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="0b28d-124">When the client application invokes a modeless address book dialog box, it includes in its Windows message loop a call to a function based on the [ACCELERATEABSDI](accelerateabsdi.md) prototype, which checks for and processes accelerator keys.</span></span> <span data-ttu-id="0b28d-125">Wenn das Dialogfeld geschlossen wird, ruft MAPI die **DISMISSMODELESS-basierte** Funktion auf, sodass die Clientanwendung den Aufruf der **ACCELERATEABSDI-basierten** Funktion beendet.</span><span class="sxs-lookup"><span data-stu-id="0b28d-125">When the dialog box is closed, MAPI calls the **DISMISSMODELESS** based function so that the client application will stop calling the **ACCELERATEABSDI** based function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0b28d-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0b28d-126">See also</span></span>



[<span data-ttu-id="0b28d-127">ADRPARM</span><span class="sxs-lookup"><span data-stu-id="0b28d-127">ADRPARM</span></span>](adrparm.md)

