---
title: FtMulDwDw
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FtMulDwDw
api_type:
- COM
ms.assetid: 8c1a342c-d7ae-4e26-b327-a63cdd3c3ee6
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 16dca82b94225afc88bcb6c4e698a50565d6b088
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791763"
---
# <a name="ftmuldwdw"></a><span data-ttu-id="a4229-103">FtMulDwDw</span><span class="sxs-lookup"><span data-stu-id="a4229-103">FtMulDwDw</span></span>

  
  
<span data-ttu-id="a4229-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a4229-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a4229-105">Multipliziert einer 32-Bit-Ganzzahl ohne Vorzeichen mit einer anderen.</span><span class="sxs-lookup"><span data-stu-id="a4229-105">Multiplies one unsigned 32-bit integer by another.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a4229-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="a4229-106">Header file:</span></span>  <br/> |<span data-ttu-id="a4229-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="a4229-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="a4229-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="a4229-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="a4229-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="a4229-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="a4229-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="a4229-110">Called by:</span></span>  <br/> |<span data-ttu-id="a4229-111">Clientanwendungen und -Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="a4229-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
FILETIME FtMulDwDw(
  DWORD Multiplicand,
  DWORD Multiplier
);
```

## <a name="parameters"></a><span data-ttu-id="a4229-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="a4229-112">Parameters</span></span>

 <span data-ttu-id="a4229-113">_Multiplikand_</span><span class="sxs-lookup"><span data-stu-id="a4229-113">_Multiplicand_</span></span>
  
> <span data-ttu-id="a4229-114">[in] Double Wort enthält, die 32-Bit-Ganzzahl ohne Vorzeichen durch den Wert im Parameter _Multiplikator_ multipliziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="a4229-114">[in] A double word that contains the unsigned 32-bit integer to be multiplied by the value in the  _Multiplier_ parameter.</span></span> 
    
 <span data-ttu-id="a4229-115">_Multiplikator_</span><span class="sxs-lookup"><span data-stu-id="a4229-115">_Multiplier_</span></span>
  
> <span data-ttu-id="a4229-116">[in] Ein Wort, Double-Wert, der den 32-Bit-Ganzzahl ohne Vorzeichen Multiplikator enthält.</span><span class="sxs-lookup"><span data-stu-id="a4229-116">[in] A double word that contains the unsigned 32-bit integer multiplier.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a4229-117">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="a4229-117">Return value</span></span>

<span data-ttu-id="a4229-118">Die **FtMulDwDw** -Funktion gibt eine [FILETIME](filetime.md) -Struktur, die das Produkt von zwei Ganzzahlen enthält.</span><span class="sxs-lookup"><span data-stu-id="a4229-118">The **FtMulDwDw** function returns a [FILETIME](filetime.md) structure that contains the product of the two integers.</span></span> <span data-ttu-id="a4229-119">Die beiden Eingabeparameter bleiben unverändert.</span><span class="sxs-lookup"><span data-stu-id="a4229-119">The two input parameters remain unchanged.</span></span> 
  
