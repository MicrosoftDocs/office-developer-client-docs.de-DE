---
title: IEnumFBBlockNext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9b46358c-bcab-f097-8746-fabfd4722b3c
description: Ruft die nächste angegebene Anzahl von Blöcken von Frei/Gebucht-Daten in einer Enumeration ab.
ms.openlocfilehash: f6ec49a9bac6bcf4fff67991d55c7656f6c8cce2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422138"
---
# <a name="ienumfbblocknext"></a><span data-ttu-id="75155-103">IEnumFBBlock::Next</span><span class="sxs-lookup"><span data-stu-id="75155-103">IEnumFBBlock::Next</span></span>

<span data-ttu-id="75155-104">Ruft die nächste angegebene Anzahl von Blöcken von Frei/Gebucht-Daten in einer Enumeration ab.</span><span class="sxs-lookup"><span data-stu-id="75155-104">Gets the next specified number of blocks of free/busy data in an enumeration.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="75155-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="75155-105">Quick info</span></span>

<span data-ttu-id="75155-106">Weitere [Informationen finden Sie unter IEnumFBBlock](ienumfbblock.md).</span><span class="sxs-lookup"><span data-stu-id="75155-106">See [IEnumFBBlock](ienumfbblock.md).</span></span>
  
```cpp
HRESULT Next(  
        LONG celt,
        FBBlock_1 *pblk,
        LONG *pcfetch
);
```

## <a name="parameters"></a><span data-ttu-id="75155-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="75155-107">Parameters</span></span>

<span data-ttu-id="75155-108">_sellert_</span><span class="sxs-lookup"><span data-stu-id="75155-108">_celt_</span></span>
  
> <span data-ttu-id="75155-109">[in] Die Anzahl der abzurufende Frei/Gebucht-Datenblöcke in *pblk.*</span><span class="sxs-lookup"><span data-stu-id="75155-109">[in] The number of free/busy data blocks in  *pblk*  to retrieve.</span></span> 
    
<span data-ttu-id="75155-110">_pblk_</span><span class="sxs-lookup"><span data-stu-id="75155-110">_pblk_</span></span>
  
> <span data-ttu-id="75155-111">[in] Ein Zeiger auf ein Array von Frei/Gebucht-Blöcken.</span><span class="sxs-lookup"><span data-stu-id="75155-111">[in] A pointer to an array of free/busy blocks.</span></span> <span data-ttu-id="75155-112">Dem Array wird eine Größe von *Kelten zugewiesen.*</span><span class="sxs-lookup"><span data-stu-id="75155-112">The array is allocated a size of  *celt*  .</span></span> <span data-ttu-id="75155-113">Die angeforderten Frei/Gebucht-Blöcke werden in diesem Array zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="75155-113">The requested free/busy blocks are returned in this array.</span></span> 
    
<span data-ttu-id="75155-114">_pcfetch_</span><span class="sxs-lookup"><span data-stu-id="75155-114">_pcfetch_</span></span>
  
> <span data-ttu-id="75155-115">[out] Die Anzahl der frei/gebucht-Blöcke, die tatsächlich in *pblk zurückgegeben werden.*</span><span class="sxs-lookup"><span data-stu-id="75155-115">[out] The number of free/busy blocks actually returned in  *pblk*  .</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="75155-116">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="75155-116">Return values</span></span>

|<span data-ttu-id="75155-117">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="75155-117">**HRESULT**</span></span>|<span data-ttu-id="75155-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="75155-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="75155-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="75155-119">S_OK</span></span>  <br/> |<span data-ttu-id="75155-120">Die angeforderte Anzahl von Blöcken wurde zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="75155-120">The requested number of blocks has been returned.</span></span>  <br/> |
|<span data-ttu-id="75155-121">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="75155-121">S_FALSE</span></span>  <br/> |<span data-ttu-id="75155-122">Die angeforderte Anzahl von Blöcken wurde nicht zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="75155-122">The requested number of blocks has not been returned.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="75155-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="75155-123">See also</span></span>

- [<span data-ttu-id="75155-124">Konstanten (Frei/Gebucht-API)</span><span class="sxs-lookup"><span data-stu-id="75155-124">Constants (Free/busy API)</span></span>](constants-free-busy-api.md)  
- [<span data-ttu-id="75155-125">FBBlock_1</span><span class="sxs-lookup"><span data-stu-id="75155-125">FBBlock_1</span></span>](fbblock_1.md)  
- [<span data-ttu-id="75155-126">IEnumFBBlock::Clone</span><span class="sxs-lookup"><span data-stu-id="75155-126">IEnumFBBlock::Clone</span></span>](ienumfbblock-clone.md)  
- [<span data-ttu-id="75155-127">IEnumFBBlock::Reset</span><span class="sxs-lookup"><span data-stu-id="75155-127">IEnumFBBlock::Reset</span></span>](ienumfbblock-reset.md)  
- [<span data-ttu-id="75155-128">IEnumFBBlock::Restrict</span><span class="sxs-lookup"><span data-stu-id="75155-128">IEnumFBBlock::Restrict</span></span>](ienumfbblock-restrict.md)  
- [<span data-ttu-id="75155-129">IEnumFBBlock::Skip</span><span class="sxs-lookup"><span data-stu-id="75155-129">IEnumFBBlock::Skip</span></span>](ienumfbblock-skip.md)

