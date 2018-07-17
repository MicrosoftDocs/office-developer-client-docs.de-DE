---
title: ISERRNA-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251451
localization_priority: Normal
ms.assetid: 6ee7dc3d-efe9-c862-f71d-034b3d9c3ec6
description: 'Gibt TRUE zurück, wenn der Wert von Zellbezug den Fehlertyp #n ist! (nicht verfügbar); Andernfalls wird FALSE zurückgegeben. ISERRNA-Funktion wird in Formeln verwendet, die auf einer anderen Zelle verweisen.'
ms.openlocfilehash: a471119265d77866e51ccc6bb556f2ce0095d31d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797241"
---
# <a name="iserrna-function"></a><span data-ttu-id="9517a-105">ISERRNA Function</span><span class="sxs-lookup"><span data-stu-id="9517a-105">ISERRNA Function</span></span>

<span data-ttu-id="9517a-106">Gibt TRUE zurück, wenn der Wert von _Zellbezug_ den Fehlertyp #n ist!</span><span class="sxs-lookup"><span data-stu-id="9517a-106">Returns TRUE if the value of  _cellreference_ is error type #N/A!</span></span> <span data-ttu-id="9517a-107">(nicht verfügbar); Andernfalls wird FALSE zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9517a-107">(not available); otherwise, it returns FALSE.</span></span> <span data-ttu-id="9517a-108">ISERRNA-Funktion wird in Formeln verwendet, die auf einer anderen Zelle verweisen.</span><span class="sxs-lookup"><span data-stu-id="9517a-108">The ISERRNA function is used in formulas that refer to another cell.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="9517a-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="9517a-109">Syntax</span></span>

<span data-ttu-id="9517a-110">ISERRNA (** *Zellbezug* **)</span><span class="sxs-lookup"><span data-stu-id="9517a-110">ISERRNA(** *cellreference* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="9517a-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="9517a-111">Parameters</span></span>

|<span data-ttu-id="9517a-112">**Name**</span><span class="sxs-lookup"><span data-stu-id="9517a-112">**Name**</span></span>|<span data-ttu-id="9517a-113">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="9517a-113">**Required/Optional**</span></span>|<span data-ttu-id="9517a-114">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="9517a-114">**Data Type**</span></span>|<span data-ttu-id="9517a-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9517a-115">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="9517a-116">_Zellbezug_</span><span class="sxs-lookup"><span data-stu-id="9517a-116">_cellreference_</span></span> <br/> |<span data-ttu-id="9517a-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="9517a-117">Required</span></span>  <br/> |<span data-ttu-id="9517a-118">**String**</span><span class="sxs-lookup"><span data-stu-id="9517a-118">**String**</span></span> <br/> |<span data-ttu-id="9517a-119">Bezug auf eine Zelle.</span><span class="sxs-lookup"><span data-stu-id="9517a-119">Reference to a cell.</span></span>  <br/> |
   
## <a name="example-1"></a><span data-ttu-id="9517a-120">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9517a-120">Example 1</span></span>

|<span data-ttu-id="9517a-121">**Cell**</span><span class="sxs-lookup"><span data-stu-id="9517a-121">**Cell**</span></span>|<span data-ttu-id="9517a-122">**Formula**</span><span class="sxs-lookup"><span data-stu-id="9517a-122">**Formula**</span></span>|<span data-ttu-id="9517a-123">**Zurückgegebener Wert**</span><span class="sxs-lookup"><span data-stu-id="9517a-123">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9517a-124">Scratch.A1</span><span class="sxs-lookup"><span data-stu-id="9517a-124">Scratch.A1</span></span>  <br/> |<span data-ttu-id="9517a-125">="5 + 3"</span><span class="sxs-lookup"><span data-stu-id="9517a-125">="5 + 3"</span></span>  <br/> |<span data-ttu-id="9517a-126">"8"</span><span class="sxs-lookup"><span data-stu-id="9517a-126">"8"</span></span>  <br/> |
|<span data-ttu-id="9517a-127">Scratch.B1</span><span class="sxs-lookup"><span data-stu-id="9517a-127">Scratch.B1</span></span>  <br/> |<span data-ttu-id="9517a-128">=ISERRNA(Scratch.a1)</span><span class="sxs-lookup"><span data-stu-id="9517a-128">=ISERRNA(Scratch.A1)</span></span>  <br/> |<span data-ttu-id="9517a-129">FALSE</span><span class="sxs-lookup"><span data-stu-id="9517a-129">FALSE</span></span>  <br/> |
   
<span data-ttu-id="9517a-130">Gibt FALSE zurück, da der zurückgegebene Wert verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="9517a-130">Returns FALSE because the value returned is available.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="9517a-131">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="9517a-131">Example 2</span></span>

|<span data-ttu-id="9517a-132">**Cell**</span><span class="sxs-lookup"><span data-stu-id="9517a-132">**Cell**</span></span>|<span data-ttu-id="9517a-133">**Formula**</span><span class="sxs-lookup"><span data-stu-id="9517a-133">**Formula**</span></span>|<span data-ttu-id="9517a-134">**Zurückgegebener Wert**</span><span class="sxs-lookup"><span data-stu-id="9517a-134">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9517a-135">Scratch.A1</span><span class="sxs-lookup"><span data-stu-id="9517a-135">Scratch.A1</span></span>  <br/> |<span data-ttu-id="9517a-136">=NV( )</span><span class="sxs-lookup"><span data-stu-id="9517a-136">=NA( )</span></span>  <br/> |<span data-ttu-id="9517a-137">#N/V!</span><span class="sxs-lookup"><span data-stu-id="9517a-137">#N/A!</span></span>  <br/> |
|<span data-ttu-id="9517a-138">Scratch.B1</span><span class="sxs-lookup"><span data-stu-id="9517a-138">Scratch.B1</span></span>  <br/> |<span data-ttu-id="9517a-139">=ISERRNA(Scratch.a1)</span><span class="sxs-lookup"><span data-stu-id="9517a-139">=ISERRNA(Scratch.A1)</span></span>  <br/> |<span data-ttu-id="9517a-140">TRUE</span><span class="sxs-lookup"><span data-stu-id="9517a-140">TRUE</span></span>  <br/> |
   
<span data-ttu-id="9517a-141">Gibt TRUE zurück, da der Rückgabewert den Fehlertyp #N/V! ergibt.</span><span class="sxs-lookup"><span data-stu-id="9517a-141">Returns TRUE because the value returned is error type #N/A!</span></span>
  
