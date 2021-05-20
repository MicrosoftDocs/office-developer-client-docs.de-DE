---
title: BOUNDINGBOXDIST-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8a2490f2-48c4-5df3-a3b3-40e8e0c80479
description: Gibt die Messung für den angegebenen Teil des das Shape umgebenden Felds zurück.
ms.openlocfilehash: a62d5b82c310e7b99e16b70982b75a68172b7fd8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428277"
---
# <a name="boundingboxdist-function"></a><span data-ttu-id="b68cd-103">BOUNDINGBOXDIST Function</span><span class="sxs-lookup"><span data-stu-id="b68cd-103">BOUNDINGBOXDIST Function</span></span>

<span data-ttu-id="b68cd-104">Gibt die Messung für den angegebenen Teil des das Shape umgebenden Felds zurück.</span><span class="sxs-lookup"><span data-stu-id="b68cd-104">Returns the measurement of the specified part of the shape's bounding box.</span></span> 
  
## <a name="version-information"></a><span data-ttu-id="b68cd-105">Versionsinformationen</span><span class="sxs-lookup"><span data-stu-id="b68cd-105">Version Information</span></span>

<span data-ttu-id="b68cd-106">Hinzugefügte Version: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="b68cd-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="b68cd-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b68cd-107">Syntax</span></span>

<span data-ttu-id="b68cd-108">BOUNDINGBOXDIST(\*\* *Index* \*\* )</span><span class="sxs-lookup"><span data-stu-id="b68cd-108">BOUNDINGBOXDIST(\*\* *Index* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="b68cd-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="b68cd-109">Parameters</span></span>

|<span data-ttu-id="b68cd-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="b68cd-110">**Name**</span></span>|<span data-ttu-id="b68cd-111">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="b68cd-111">**Required/Optional**</span></span>|<span data-ttu-id="b68cd-112">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="b68cd-112">**Data Type**</span></span>|<span data-ttu-id="b68cd-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b68cd-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="b68cd-114">_Index_</span><span class="sxs-lookup"><span data-stu-id="b68cd-114">_Index_</span></span> <br/> |<span data-ttu-id="b68cd-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="b68cd-115">Required</span></span>  <br/> |<span data-ttu-id="b68cd-116">**Number**</span><span class="sxs-lookup"><span data-stu-id="b68cd-116">**Number**</span></span> <br/> |<span data-ttu-id="b68cd-117">Der Teil des begrenzungsfelds des Shapes, der gemessen und zurückzukehren ist.</span><span class="sxs-lookup"><span data-stu-id="b68cd-117">The part of the shape's bounding box to measure and return.</span></span> <span data-ttu-id="b68cd-118">Mögliche Werte finden Sie in den Hinweisen.</span><span class="sxs-lookup"><span data-stu-id="b68cd-118">See Remarks for possible values.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="b68cd-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b68cd-119">Return value</span></span>

 <span data-ttu-id="b68cd-120">**Number**</span><span class="sxs-lookup"><span data-stu-id="b68cd-120">**Number**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b68cd-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b68cd-121">Remarks</span></span>

 <span data-ttu-id="b68cd-122">*Index*  kann einer der folgenden Werte sein.</span><span class="sxs-lookup"><span data-stu-id="b68cd-122">*Index*  can be one of the following values.</span></span> 
  
|<span data-ttu-id="b68cd-123">**Aspekt**</span><span class="sxs-lookup"><span data-stu-id="b68cd-123">**Item**</span></span>|<span data-ttu-id="b68cd-124">**Wert**</span><span class="sxs-lookup"><span data-stu-id="b68cd-124">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b68cd-125">Width</span><span class="sxs-lookup"><span data-stu-id="b68cd-125">Width</span></span>  <br/> |<span data-ttu-id="b68cd-126">0</span><span class="sxs-lookup"><span data-stu-id="b68cd-126">0</span></span>  <br/> |
|<span data-ttu-id="b68cd-127">Height</span><span class="sxs-lookup"><span data-stu-id="b68cd-127">Height</span></span>  <br/> |<span data-ttu-id="b68cd-128">1</span><span class="sxs-lookup"><span data-stu-id="b68cd-128">1</span></span>  <br/> |
|<span data-ttu-id="b68cd-129">Shape-Pin bis linke Kante</span><span class="sxs-lookup"><span data-stu-id="b68cd-129">Left edge to shape pin</span></span>  <br/> |<span data-ttu-id="b68cd-130">2</span><span class="sxs-lookup"><span data-stu-id="b68cd-130">2</span></span>  <br/> |
|<span data-ttu-id="b68cd-131">Shape-Pin bis rechte Kante</span><span class="sxs-lookup"><span data-stu-id="b68cd-131">Shape pin to right edge</span></span>  <br/> |<span data-ttu-id="b68cd-132">3</span><span class="sxs-lookup"><span data-stu-id="b68cd-132">3</span></span>  <br/> |
|<span data-ttu-id="b68cd-133">Shape-Pin bis obere Kante</span><span class="sxs-lookup"><span data-stu-id="b68cd-133">Shape pin to top edge</span></span>  <br/> |<span data-ttu-id="b68cd-134">4 </span><span class="sxs-lookup"><span data-stu-id="b68cd-134">4</span></span>  <br/> |
|<span data-ttu-id="b68cd-135">Shape-Pin bis untere Kante</span><span class="sxs-lookup"><span data-stu-id="b68cd-135">Bottom edge to shape pin</span></span>  <br/> |<span data-ttu-id="b68cd-136">5 </span><span class="sxs-lookup"><span data-stu-id="b68cd-136">5</span></span>  <br/> |
|<span data-ttu-id="b68cd-137">Mitte des umgebenden Felds bis PinX</span><span class="sxs-lookup"><span data-stu-id="b68cd-137">Center of bounding box to PinX</span></span>  <br/> |<span data-ttu-id="b68cd-138">6 </span><span class="sxs-lookup"><span data-stu-id="b68cd-138">6</span></span>  <br/> |
|<span data-ttu-id="b68cd-139">Mitte des umgebenden Felds bis PinY</span><span class="sxs-lookup"><span data-stu-id="b68cd-139">Center of bounding box to PinY</span></span>  <br/> |<span data-ttu-id="b68cd-140">7 </span><span class="sxs-lookup"><span data-stu-id="b68cd-140">7</span></span>  <br/> |
   

