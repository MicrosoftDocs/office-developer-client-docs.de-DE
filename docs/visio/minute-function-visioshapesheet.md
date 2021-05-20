---
title: MINUTE-Funktion (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251464
localization_priority: Normal
ms.assetid: 5a90cb16-7eef-8876-8e25-408787b16f58
description: Gibt eine ganze Zahl von 0 bis 59 zurück, die die Minutenkomponente von datetime oder Ausdruck darstellt.
ms.openlocfilehash: 35fe1dc8d4026dd6c829a38504d9ba82d64edda2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436566"
---
# <a name="minute-function-visioshapesheet"></a><span data-ttu-id="a43f5-103">MINUTE-Funktion (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="a43f5-103">MINUTE Function (VisioShapeSheet)</span></span>

<span data-ttu-id="a43f5-104">Gibt eine ganze Zahl von 0 bis 59 zurück, die die Minutenkomponente *von datetime oder* *Ausdruck darstellt.*</span><span class="sxs-lookup"><span data-stu-id="a43f5-104">Returns an integer from 0 to 59 that represents the minutes component of  *datetime*  or  *expression*  .</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="a43f5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a43f5-105">Syntax</span></span>

<span data-ttu-id="a43f5-106">MINUTE(" *datetime*  "|  *Ausdruck*  [,  *lcid*  ])</span><span class="sxs-lookup"><span data-stu-id="a43f5-106">MINUTE(" *datetime*  "|  *expression*  [,  *lcid*  ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="a43f5-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="a43f5-107">Parameters</span></span>

|<span data-ttu-id="a43f5-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="a43f5-108">**Name**</span></span>|<span data-ttu-id="a43f5-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="a43f5-109">**Required/Optional**</span></span>|<span data-ttu-id="a43f5-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="a43f5-110">**Data Type**</span></span>|<span data-ttu-id="a43f5-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a43f5-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="a43f5-112">_datetime_</span><span class="sxs-lookup"><span data-stu-id="a43f5-112">_datetime_</span></span> <br/> |<span data-ttu-id="a43f5-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="a43f5-113">Required</span></span>  <br/> |<span data-ttu-id="a43f5-114">**String**</span><span class="sxs-lookup"><span data-stu-id="a43f5-114">**String**</span></span> <br/> |<span data-ttu-id="a43f5-115">Beliebige Zeichenfolge, die allgemein als Datums- und Zeitangabe erkannt wird, oder ein Bezug auf eine Zelle mit einer Datums- und Zeitangabe.</span><span class="sxs-lookup"><span data-stu-id="a43f5-115">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="a43f5-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="a43f5-116">_expression_</span></span> <br/> |<span data-ttu-id="a43f5-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="a43f5-117">Required</span></span>  <br/> |<span data-ttu-id="a43f5-118">**String**</span><span class="sxs-lookup"><span data-stu-id="a43f5-118">**String**</span></span> <br/> | <span data-ttu-id="a43f5-119">Beliebiger Ausdruck, der eine Datums- und Zeitangabe liefert.</span><span class="sxs-lookup"><span data-stu-id="a43f5-119">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="a43f5-120">_lcid_</span><span class="sxs-lookup"><span data-stu-id="a43f5-120">_lcid_</span></span> <br/> |<span data-ttu-id="a43f5-121">Optional.</span><span class="sxs-lookup"><span data-stu-id="a43f5-121">Optional</span></span>  <br/> |<span data-ttu-id="a43f5-122">**Number**</span><span class="sxs-lookup"><span data-stu-id="a43f5-122">**Number**</span></span> <br/> |<span data-ttu-id="a43f5-p101">Der lokale Bezeichner, der bei der Auswertung eines nicht lokalen Werts für datetime verwendet werden soll. Der lokale Bezeichner ist eine Zahl, die in den Systemkopfdateien beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="a43f5-p101">The locale identifier to be used in evaluating a nonlocal datetime. The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="a43f5-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a43f5-125">Return value</span></span>

<span data-ttu-id="a43f5-126">Ganze Zahl</span><span class="sxs-lookup"><span data-stu-id="a43f5-126">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a43f5-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a43f5-127">Remarks</span></span>

<span data-ttu-id="a43f5-128">Die Datumskomponente in  _datetime_ und  _ausdruck_ wird verworfen.</span><span class="sxs-lookup"><span data-stu-id="a43f5-128">The date component in  _datetime_ and  _expression_ is discarded.</span></span> 
  
<span data-ttu-id="a43f5-129">Es findet kein Auf- oder Abrunden statt.</span><span class="sxs-lookup"><span data-stu-id="a43f5-129">No rounding is done.</span></span> <span data-ttu-id="a43f5-130">Wenn  _datetime_ fehlt oder nicht in ein gültiges Ergebnis konvertiert werden kann, gibt die Funktion einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="a43f5-130">If  _datetime_ is missing or cannot be converted to a valid result, the function returns an error.</span></span> 
  
<span data-ttu-id="a43f5-131">Der zurückgegebene Wert wird in dem Zeitformat angezeigt, das aktuell in den Ländereinstellungen des Systems festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="a43f5-131">The returned value is formatted according to the time style set by the system's current Regional Settings.</span></span>
  
<span data-ttu-id="a43f5-132">Die MINUTE-Funktion akzeptiert auch einen einzelnen Zahlenwert  _für_ ausdruck, wobei der Dezimalteil den Bruchteil eines Tages seit Mitternacht darstellt.</span><span class="sxs-lookup"><span data-stu-id="a43f5-132">The MINUTE function also accepts a single number value for  _expression_ where the decimal portion represents the fraction of a day since midnight.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="a43f5-133">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a43f5-133">Example 1</span></span>

<span data-ttu-id="a43f5-134">MINUTE("07.07.1999 13:45:24")</span><span class="sxs-lookup"><span data-stu-id="a43f5-134">MINUTE("7/7/1999 13:45:24")</span></span>
  
<span data-ttu-id="a43f5-135">Gibt 45 zurück.</span><span class="sxs-lookup"><span data-stu-id="a43f5-135">Returns 45.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="a43f5-136">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="a43f5-136">Example 2</span></span>

<span data-ttu-id="a43f5-137">MINUTE(ZEITWERT("25. Jan. 1999 12:07:45")+6 vm.)</span><span class="sxs-lookup"><span data-stu-id="a43f5-137">MINUTE(TIMEVALUE("Jan. 25, 1999 12:07:45")+6 em.)</span></span>
  
<span data-ttu-id="a43f5-138">Gibt 13 zurück.</span><span class="sxs-lookup"><span data-stu-id="a43f5-138">Returns 13.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="a43f5-139">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="a43f5-139">Example 3</span></span>

<span data-ttu-id="a43f5-140">MINUTE(0,575)</span><span class="sxs-lookup"><span data-stu-id="a43f5-140">MINUTE(0.575)</span></span>
  
<span data-ttu-id="a43f5-141">Gibt 48 zurück.</span><span class="sxs-lookup"><span data-stu-id="a43f5-141">Returns 48.</span></span>
  

