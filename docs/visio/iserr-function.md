---
title: ISERR-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251448
localization_priority: Normal
ms.assetid: 87508007-8ad2-3bcf-55dc-f0207c7c6fe3
description: 'Gibt TRUE zurück, wenn der Wert von cellreference einen beliebigen Fehlertyp außer #N/A ist. Andernfalls wird FALSE zurückgegeben. Die ISERR-Funktion wird in Formeln verwendet, die auf eine andere Zelle verweisen.'
ms.openlocfilehash: e2117c38d3cad2408295ed6894aefc78e107596e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432107"
---
# <a name="iserr-function"></a><span data-ttu-id="837e3-104">ISERR Function</span><span class="sxs-lookup"><span data-stu-id="837e3-104">ISERR Function</span></span>

<span data-ttu-id="837e3-105">Gibt TRUE zurück, wenn der Wert von  _cellreference_ einen beliebigen Fehlertyp außer #N/A ist. Andernfalls wird FALSE zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="837e3-105">Returns TRUE if the value of  _cellreference_ is any error type except #N/A; otherwise, it returns FALSE.</span></span> <span data-ttu-id="837e3-106">Die ISERR-Funktion wird in Formeln verwendet, die auf eine andere Zelle verweisen.</span><span class="sxs-lookup"><span data-stu-id="837e3-106">The ISERR function is used in formulas that refer to another cell.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="837e3-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="837e3-107">Syntax</span></span>

<span data-ttu-id="837e3-108">ISERR(\*\* *cellreference* \*\* )</span><span class="sxs-lookup"><span data-stu-id="837e3-108">ISERR(\*\* *cellreference* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="837e3-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="837e3-109">Parameters</span></span>

|<span data-ttu-id="837e3-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="837e3-110">**Name**</span></span>|<span data-ttu-id="837e3-111">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="837e3-111">**Required/Optional**</span></span>|<span data-ttu-id="837e3-112">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="837e3-112">**Data Type**</span></span>|<span data-ttu-id="837e3-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="837e3-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="837e3-114">_cellreference_</span><span class="sxs-lookup"><span data-stu-id="837e3-114">_cellreference_</span></span> <br/> |<span data-ttu-id="837e3-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="837e3-115">Required</span></span>  <br/> |<span data-ttu-id="837e3-116">**String**</span><span class="sxs-lookup"><span data-stu-id="837e3-116">**String**</span></span> <br/> |<span data-ttu-id="837e3-117">Bezug auf eine Zelle.</span><span class="sxs-lookup"><span data-stu-id="837e3-117">Reference to a cell.</span></span>  <br/> |
   
## <a name="example-1"></a><span data-ttu-id="837e3-118">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="837e3-118">Example 1</span></span>

|<span data-ttu-id="837e3-119">**Cell**</span><span class="sxs-lookup"><span data-stu-id="837e3-119">**Cell**</span></span>|<span data-ttu-id="837e3-120">**Formula**</span><span class="sxs-lookup"><span data-stu-id="837e3-120">**Formula**</span></span>|<span data-ttu-id="837e3-121">**Zurückgegebener Wert**</span><span class="sxs-lookup"><span data-stu-id="837e3-121">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="837e3-122">Scratch.A1</span><span class="sxs-lookup"><span data-stu-id="837e3-122">Scratch.A1</span></span>  <br/> |<span data-ttu-id="837e3-123">=NV( )</span><span class="sxs-lookup"><span data-stu-id="837e3-123">=NA( )</span></span>  <br/> |<span data-ttu-id="837e3-124">#N/A!</span><span class="sxs-lookup"><span data-stu-id="837e3-124">#N/A!</span></span>  <br/> |
|<span data-ttu-id="837e3-125">Scratch.B1</span><span class="sxs-lookup"><span data-stu-id="837e3-125">Scratch.B1</span></span>  <br/> |<span data-ttu-id="837e3-126">=ISERR(Scratch.A1)</span><span class="sxs-lookup"><span data-stu-id="837e3-126">=ISERR(Scratch.A1)</span></span>  <br/> |<span data-ttu-id="837e3-127">FALSE</span><span class="sxs-lookup"><span data-stu-id="837e3-127">FALSE</span></span>  <br/> |
   
<span data-ttu-id="837e3-p103">Gibt FALSE zurück, da die ISERR-Funktion den Fehler #N/V! nicht erkennt. Verwenden Sie ISERROR, um alle Fehlertypen zu finden.</span><span class="sxs-lookup"><span data-stu-id="837e3-p103">Returns FALSE because the #N/A! error is not recognized by the ISERR function. Use ISERROR to find all error types.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="837e3-131">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="837e3-131">Example 2</span></span>

|<span data-ttu-id="837e3-132">**Cell**</span><span class="sxs-lookup"><span data-stu-id="837e3-132">**Cell**</span></span>|<span data-ttu-id="837e3-133">**Formula**</span><span class="sxs-lookup"><span data-stu-id="837e3-133">**Formula**</span></span>|<span data-ttu-id="837e3-134">**Zurückgegebener Wert**</span><span class="sxs-lookup"><span data-stu-id="837e3-134">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="837e3-135">Scratch.X1</span><span class="sxs-lookup"><span data-stu-id="837e3-135">Scratch.X1</span></span>  <br/> |<span data-ttu-id="837e3-136">="House"</span><span class="sxs-lookup"><span data-stu-id="837e3-136">="House"</span></span>  <br/> |<span data-ttu-id="837e3-137">#VALUE!</span><span class="sxs-lookup"><span data-stu-id="837e3-137">#VALUE!</span></span>  <br/> |
|<span data-ttu-id="837e3-138">Scratch.A1</span><span class="sxs-lookup"><span data-stu-id="837e3-138">Scratch.A1</span></span>  <br/> |<span data-ttu-id="837e3-139">=ISERR(Scratch.X1)</span><span class="sxs-lookup"><span data-stu-id="837e3-139">=ISERR(Scratch.X1)</span></span>  <br/> |<span data-ttu-id="837e3-140">TRUE</span><span class="sxs-lookup"><span data-stu-id="837e3-140">TRUE</span></span>  <br/> |
   
<span data-ttu-id="837e3-p104">Gibt TRUE zurück, da die Funktion ISERR den Fehler #WERT! erkennt.</span><span class="sxs-lookup"><span data-stu-id="837e3-p104">Returns TRUE because the #VALUE! error is recognized by the ISERR function.</span></span>
  

