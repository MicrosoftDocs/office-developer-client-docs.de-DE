---
title: SizedDtblLabel
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedDtblLabel
api_type:
- COM
ms.assetid: c7cb8cf9-7abd-4ee3-b88c-d61695f4ed31
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: c2e275e373677e50510a0aa87f5060070a870a0f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795560"
---
# <a name="sizeddtbllabel"></a><span data-ttu-id="92734-103">SizedDtblLabel</span><span class="sxs-lookup"><span data-stu-id="92734-103">SizedDtblLabel</span></span>

<span data-ttu-id="92734-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="92734-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="92734-105">Erstellt eine benannte Struktur, die eine [DTBLLABEL](dtbllabel.md) -Struktur für die Beschreibung ein Label-Steuerelement und das zugeordnete Beschriftung an einer angegebenen Länge enthält.</span><span class="sxs-lookup"><span data-stu-id="92734-105">Creates a named structure that includes a [DTBLLABEL](dtbllabel.md) structure for describing a label control and the associated label of a specified length.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="92734-106">In der Headerdatei angegeben:</span><span class="sxs-lookup"><span data-stu-id="92734-106">Specified in header file:</span></span>  <br/> |<span data-ttu-id="92734-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="92734-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="92734-108">Verwandte Struktur</span><span class="sxs-lookup"><span data-stu-id="92734-108">Related structure</span></span>  <br/> |<span data-ttu-id="92734-109">**DTBLLABEL**</span><span class="sxs-lookup"><span data-stu-id="92734-109">**DTBLLABEL**</span></span> <br/> |
   
```cpp
SizedDtblLabel (n, u)
```

## <a name="parameters"></a><span data-ttu-id="92734-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="92734-110">Parameters</span></span>

<span data-ttu-id="92734-111">_n_</span><span class="sxs-lookup"><span data-stu-id="92734-111">_n_</span></span>
  
> <span data-ttu-id="92734-112">Länge der Beschriftung.</span><span class="sxs-lookup"><span data-stu-id="92734-112">Length of the label.</span></span> <span data-ttu-id="92734-113">Dazu gehört das letzte Zeichen NULL.</span><span class="sxs-lookup"><span data-stu-id="92734-113">This includes the ending NULL character.</span></span> 
    
<span data-ttu-id="92734-114">_u_</span><span class="sxs-lookup"><span data-stu-id="92734-114">_u_</span></span>
  
> <span data-ttu-id="92734-115">Der Name für die neue Struktur.</span><span class="sxs-lookup"><span data-stu-id="92734-115">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="92734-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="92734-116">Remarks</span></span>

<span data-ttu-id="92734-117">Das Makro **SizedDtblLabel** können Sie eine Beschriftung anzeigen Tabelle definieren, wenn die Anzahl der Zeichen in der Bezeichnung bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="92734-117">The **SizedDtblLabel** macro lets you define a display table label when the number of characters in the label is known.</span></span> <span data-ttu-id="92734-118">Die neue Struktur wird mit der folgenden Elemente erstellt:</span><span class="sxs-lookup"><span data-stu-id="92734-118">The new structure is created with the following members:</span></span> 
  
```cpp
DTBLLABEL dtbllabel;
TCHAR lpszLabelName[n];
```

<span data-ttu-id="92734-119">Führen Sie einen Zeiger auf die resultierende Struktur aus dem Makro **SizedDtblLabel** als Zeiger Struktur **DTBLLABEL** die folgende Umwandlung:</span><span class="sxs-lookup"><span data-stu-id="92734-119">To use a pointer to the resulting structure from the **SizedDtblLabel** macro as a **DTBLLABEL** structure pointer, perform the following cast:</span></span> 
  
```cpp
lpDtblLabel = (LPDTBLLABEL) &SizedDtblLabel;
```

## <a name="see-also"></a><span data-ttu-id="92734-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="92734-120">See also</span></span>

- [<span data-ttu-id="92734-121">DTBLLABEL</span><span class="sxs-lookup"><span data-stu-id="92734-121">DTBLLABEL</span></span>](dtbllabel.md)
- [<span data-ttu-id="92734-122">Makros im Zusammenhang mit Strukturen</span><span class="sxs-lookup"><span data-stu-id="92734-122">Macros Related to Structures</span></span>](macros-related-to-structures.md)
