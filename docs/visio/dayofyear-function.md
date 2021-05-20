---
title: DAYOFYEAR-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251416
localization_priority: Normal
ms.assetid: 154d76a2-81f5-d8b1-b665-26dbae5da615
description: Gibt eine ganze Zahl von 1 bis 366 zurück, die den sequenziellen Tag des Jahres in Datetime oder Ausdruck darstellt. Die DAYOFYEAR-Funktion verwendet den gregorianischen Kalender.
ms.openlocfilehash: 30c0331a57282baee97e81689b6a8f362581b8f1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439451"
---
# <a name="dayofyear-function"></a><span data-ttu-id="6388b-104">TAGDESJAHRES-Funktion</span><span class="sxs-lookup"><span data-stu-id="6388b-104">DAYOFYEAR Function</span></span>

<span data-ttu-id="6388b-105">Gibt eine ganze Zahl von 1 bis 366 zurück, die den sequenziellen Tag des Jahres in _datetime oder_ _Ausdruck darstellt._</span><span class="sxs-lookup"><span data-stu-id="6388b-105">Returns an integer, 1 to 366, that represents the sequential day of the year in  _datetime_ or  _expression_.</span></span> <span data-ttu-id="6388b-106">Die DAYOFYEAR-Funktion verwendet den gregorianischen Kalender.</span><span class="sxs-lookup"><span data-stu-id="6388b-106">The DAYOFYEAR function uses the Gregorian calendar.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="6388b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="6388b-107">Syntax</span></span>

<span data-ttu-id="6388b-108">DAYOFYEAR(" \*\* *datetime* \*\* "| \*\* *Ausdruck* \*\* [, \*\* *lcid* \*\* ])</span><span class="sxs-lookup"><span data-stu-id="6388b-108">DAYOFYEAR(" \*\* *datetime* \*\* "| \*\* *expression* \*\* [, \*\* *lcid* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="6388b-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="6388b-109">Parameters</span></span>

|<span data-ttu-id="6388b-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="6388b-110">**Name**</span></span>|<span data-ttu-id="6388b-111">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="6388b-111">**Required/Optional**</span></span>|<span data-ttu-id="6388b-112">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="6388b-112">**Data Type**</span></span>|<span data-ttu-id="6388b-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6388b-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="6388b-114">_datetime_</span><span class="sxs-lookup"><span data-stu-id="6388b-114">_datetime_</span></span> <br/> |<span data-ttu-id="6388b-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="6388b-115">Required</span></span>  <br/> |<span data-ttu-id="6388b-116">**String**</span><span class="sxs-lookup"><span data-stu-id="6388b-116">**String**</span></span> <br/> |<span data-ttu-id="6388b-117">Beliebige Zeichenfolge, die allgemein als Datums- und Zeitangabe erkannt wird, oder ein Bezug auf eine Zelle mit einer Datums- und Zeitangabe.</span><span class="sxs-lookup"><span data-stu-id="6388b-117">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="6388b-118">_expression_</span><span class="sxs-lookup"><span data-stu-id="6388b-118">_expression_</span></span> <br/> |<span data-ttu-id="6388b-119">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="6388b-119">Required</span></span>  <br/> |<span data-ttu-id="6388b-120">**String**</span><span class="sxs-lookup"><span data-stu-id="6388b-120">**String**</span></span> <br/> |<span data-ttu-id="6388b-121">Beliebiger Ausdruck, der eine Datums- und Zeitangabe liefert.</span><span class="sxs-lookup"><span data-stu-id="6388b-121">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="6388b-122">_lcid_</span><span class="sxs-lookup"><span data-stu-id="6388b-122">_lcid_</span></span> <br/> |<span data-ttu-id="6388b-123">Optional.</span><span class="sxs-lookup"><span data-stu-id="6388b-123">Optional</span></span>  <br/> |<span data-ttu-id="6388b-124">**Number**</span><span class="sxs-lookup"><span data-stu-id="6388b-124">**Number**</span></span> <br/> |<span data-ttu-id="6388b-p103">Gibt den lokalen Bezeichner an, der bei der Auswertung eines nicht lokalen Werts für datetime verwendet werden soll. Der lokale Bezeichner ist eine Zahl, die in den Systemkopfdateien beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="6388b-p103">Specifies the locale identifier to be used in evaluating a non-local datetime. The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="6388b-127">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6388b-127">Return value</span></span>

<span data-ttu-id="6388b-128">Ganze Zahl</span><span class="sxs-lookup"><span data-stu-id="6388b-128">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6388b-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6388b-129">Remarks</span></span>

<span data-ttu-id="6388b-130">Jede Zeitkomponente in  _datetime_ oder  _ausdruck_ wird verworfen.</span><span class="sxs-lookup"><span data-stu-id="6388b-130">Any time component in  _datetime_ or  _expression_ is discarded.</span></span> 
  
<span data-ttu-id="6388b-131">Das Ergebnis entspricht dem 1. Januar bis zum 31. Dezember.</span><span class="sxs-lookup"><span data-stu-id="6388b-131">The result corresponds to January 1 to December 31.</span></span> <span data-ttu-id="6388b-132">Es findet kein Auf- oder Abrunden statt.</span><span class="sxs-lookup"><span data-stu-id="6388b-132">No rounding is done.</span></span> <span data-ttu-id="6388b-133">Wenn  _datetime_ fehlt oder nicht als gültiges Datum oder eine gültige Uhrzeit interpretiert werden kann, gibt die Funktion einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="6388b-133">If  _datetime_ is missing or cannot be interpreted as a valid date or time, the function returns an error.</span></span> 
  
<span data-ttu-id="6388b-134">Die DAYOFYEAR-Funktion akzeptiert auch  einen einzelnen Zahlenwert für ausdruck, wobei der ganzzahlige Teil des Ergebnisses die Anzahl der Tage seit dem 30. Dezember 1899 darstellt.</span><span class="sxs-lookup"><span data-stu-id="6388b-134">The DAYOFYEAR function also accepts a single number value for  _expression_ where the integer portion of the result represents the number of days since December 30, 1899.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="6388b-135">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6388b-135">Example 1</span></span>

<span data-ttu-id="6388b-136">DAYOFYEAR("30. Mai 1997 13:45:24")</span><span class="sxs-lookup"><span data-stu-id="6388b-136">DAYOFYEAR("May 30, 1997 13:45:24")</span></span>
  
<span data-ttu-id="6388b-137">Gibt 150 zurück</span><span class="sxs-lookup"><span data-stu-id="6388b-137">Returns 150.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="6388b-138">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="6388b-138">Example 2</span></span>

<span data-ttu-id="6388b-139">DAYOFYEAR(DATUMSWERT("30. Mai 1997")+7 t.)</span><span class="sxs-lookup"><span data-stu-id="6388b-139">DAYOFYEAR(DATEVALUE("May 30, 1997")+7 ed.)</span></span>
  
<span data-ttu-id="6388b-140">Gibt 157 zurück.</span><span class="sxs-lookup"><span data-stu-id="6388b-140">Returns 157.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="6388b-141">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="6388b-141">Example 3</span></span>

<span data-ttu-id="6388b-142">DAYOFYEAR(35580.6337)</span><span class="sxs-lookup"><span data-stu-id="6388b-142">DAYOFYEAR(35580.6337)</span></span>
  
<span data-ttu-id="6388b-143">Gibt 150 zurück.</span><span class="sxs-lookup"><span data-stu-id="6388b-143">Returns 150.</span></span>
  

