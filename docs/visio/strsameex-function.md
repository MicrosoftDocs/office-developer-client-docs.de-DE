---
title: STRSAMEEX-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251787
localization_priority: Normal
ms.assetid: 056b54ae-1475-9480-6ebc-5c34ef48e0f8
description: Bestimmt, ob zwei Zeichenfolgen identisch sind.
ms.openlocfilehash: ac5a74e08079f86c28b086b92302ebb01a4b0627
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413864"
---
# <a name="strsameex-function"></a><span data-ttu-id="afb69-103">STRSAMEEX Function</span><span class="sxs-lookup"><span data-stu-id="afb69-103">STRSAMEEX Function</span></span>

<span data-ttu-id="afb69-104">Bestimmt, ob zwei Zeichenfolgen identisch sind.</span><span class="sxs-lookup"><span data-stu-id="afb69-104">Determines whether two strings are the same.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="afb69-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="afb69-105">Syntax</span></span>

<span data-ttu-id="afb69-106">STRSAMEEX (" \*\* *string1* \*\* ", " \*\* *string2* \*\* ", \*\* *localeID* \*\*, \*\* *flag* \*\* )</span><span class="sxs-lookup"><span data-stu-id="afb69-106">STRSAMEEX (" \*\* *string1* \*\* ", " \*\* *string2* \*\* ", \*\* *localeID* \*\*, \*\* *flag* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="afb69-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="afb69-107">Parameters</span></span>

|<span data-ttu-id="afb69-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="afb69-108">**Name**</span></span>|<span data-ttu-id="afb69-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="afb69-109">**Required/Optional**</span></span>|<span data-ttu-id="afb69-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="afb69-110">**Data Type**</span></span>|<span data-ttu-id="afb69-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="afb69-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="afb69-112">_string1_</span><span class="sxs-lookup"><span data-stu-id="afb69-112">_string1_</span></span> <br/> |<span data-ttu-id="afb69-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="afb69-113">Required</span></span>  <br/> |<span data-ttu-id="afb69-114">**String**</span><span class="sxs-lookup"><span data-stu-id="afb69-114">**String**</span></span> <br/> |<span data-ttu-id="afb69-115">Die erste zu vergleichende Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="afb69-115">The first string to compare.</span></span>  <br/> |
| <span data-ttu-id="afb69-116">_string2_</span><span class="sxs-lookup"><span data-stu-id="afb69-116">_string2_</span></span> <br/> |<span data-ttu-id="afb69-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="afb69-117">Required</span></span>  <br/> |<span data-ttu-id="afb69-118">**String**</span><span class="sxs-lookup"><span data-stu-id="afb69-118">**String**</span></span> <br/> | <span data-ttu-id="afb69-119">Die zweite zu vergleichende Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="afb69-119">The second string to compare.</span></span>  <br/> |
| <span data-ttu-id="afb69-120">_localeID_</span><span class="sxs-lookup"><span data-stu-id="afb69-120">_localeID_</span></span> <br/> |<span data-ttu-id="afb69-121">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="afb69-121">Required</span></span>  <br/> |<span data-ttu-id="afb69-122">**Numeric**</span><span class="sxs-lookup"><span data-stu-id="afb69-122">**Numeric**</span></span> <br/> |<span data-ttu-id="afb69-123">Der lokale ID-Code.</span><span class="sxs-lookup"><span data-stu-id="afb69-123">The locale ID code.</span></span>  <br/> |
| <span data-ttu-id="afb69-124">_Flag_</span><span class="sxs-lookup"><span data-stu-id="afb69-124">_flag_</span></span> <br/> |<span data-ttu-id="afb69-125">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="afb69-125">Required</span></span>  <br/> |<span data-ttu-id="afb69-126">**Numeric**</span><span class="sxs-lookup"><span data-stu-id="afb69-126">**Numeric**</span></span> <br/> | <span data-ttu-id="afb69-127">Ein Bit, das den Typ des Vergleichs bestimmt.</span><span class="sxs-lookup"><span data-stu-id="afb69-127">A bit that specifies the type of comparison.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="afb69-128">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="afb69-128">Return value</span></span>

<span data-ttu-id="afb69-129">Boolesch</span><span class="sxs-lookup"><span data-stu-id="afb69-129">Boolean</span></span>
  
## <a name="remarks"></a><span data-ttu-id="afb69-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="afb69-130">Remarks</span></span>

<span data-ttu-id="afb69-p101">STRSAMEEX gibt TRUE zurück, wenn beide Eingabezeichenfolgen identisch sind. Ist dies nicht der Fall, wird FALSE zurückgegeben. Verwenden Sie diese Funktion, wenn Sie Multibyte-Zeichenfolgen vergleichen oder Vergleiche mit Groß- und Kleinschreibregeln für ein bestimmtes Gebietsschema durchführen möchten.
			
</span><span class="sxs-lookup"><span data-stu-id="afb69-p101">STRSAMEEX returns TRUE if both input strings are the same and FALSE if they aren't. Use this function to compare multi-byte strings or to do comparisons that use case rules for a specific locale.</span></span>
  
<span data-ttu-id="afb69-133">Sie können eine beliebige Kombination folgender Flags mit der STRGLEICHEX-Funktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="afb69-133">You can use a combination of any of the following flags with the STRSAMEEX function.</span></span>
  
|<span data-ttu-id="afb69-134">**Wert**</span><span class="sxs-lookup"><span data-stu-id="afb69-134">**Flag**</span></span>|<span data-ttu-id="afb69-135">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="afb69-135">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="afb69-136">1</span><span class="sxs-lookup"><span data-stu-id="afb69-136">1</span></span>  <br/> |<span data-ttu-id="afb69-137">Groß- und Kleinschreibung ignorieren.</span><span class="sxs-lookup"><span data-stu-id="afb69-137">Ignore case.</span></span>  <br/> |
|<span data-ttu-id="afb69-138">2</span><span class="sxs-lookup"><span data-stu-id="afb69-138">2</span></span>  <br/> |<span data-ttu-id="afb69-139">Nicht-gesperrte Zeichen ignorieren.</span><span class="sxs-lookup"><span data-stu-id="afb69-139">Ignore non-spacing characters.</span></span>  <br/> |
|<span data-ttu-id="afb69-140">4 </span><span class="sxs-lookup"><span data-stu-id="afb69-140">4</span></span>  <br/> |<span data-ttu-id="afb69-141">Symbole ignorieren.</span><span class="sxs-lookup"><span data-stu-id="afb69-141">Ignore symbols.</span></span>  <br/> |
|<span data-ttu-id="afb69-142">4096</span><span class="sxs-lookup"><span data-stu-id="afb69-142">4096</span></span>  <br/> |<span data-ttu-id="afb69-143">Interpunktionszeichen wie Symbole behandeln.</span><span class="sxs-lookup"><span data-stu-id="afb69-143">Treat punctuation the same as symbols.</span></span>  <br/> |
|<span data-ttu-id="afb69-144">65536</span><span class="sxs-lookup"><span data-stu-id="afb69-144">65536</span></span>  <br/> |<span data-ttu-id="afb69-145">Nicht zwischen Hiragana- und Katakana-Zeichen unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="afb69-145">Don't differentiate between Hiragana and Katakana characters.</span></span>  <br/> |
|<span data-ttu-id="afb69-146">131072</span><span class="sxs-lookup"><span data-stu-id="afb69-146">131072</span></span>  <br/> |<span data-ttu-id="afb69-147">Nicht zwischen Einzel-Byte-Zeichen und dem gleichen Zeichen als Doppel-Byte-Zeichen unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="afb69-147">Don't differentiate between a single-byte character and the same character as a double-byte character.</span></span>  <br/> |
   

