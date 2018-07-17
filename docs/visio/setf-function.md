---
title: SETF-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251496
localization_priority: Normal
ms.assetid: fcf415c1-171f-b75f-6e40-2bbdbe8b1cfb
description: Legt die Formel einer Zelle fest.
ms.openlocfilehash: a1e6a12014a77a20c0968b3ed2f7bc25badad8ce
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797996"
---
# <a name="setf-function"></a><span data-ttu-id="9619f-103">SETF-Funktion</span><span class="sxs-lookup"><span data-stu-id="9619f-103">SETF Function</span></span>

<span data-ttu-id="9619f-104">Legt die Formel einer Zelle fest.</span><span class="sxs-lookup"><span data-stu-id="9619f-104">Sets a cell's formula.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="9619f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9619f-105">Syntax</span></span>

<span data-ttu-id="9619f-106">SETF (GETREF (** *Zelle* **), ** *Formel* **)</span><span class="sxs-lookup"><span data-stu-id="9619f-106">SETF( GETREF(** *cell* ** ), ** *formula* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="9619f-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="9619f-107">Parameters</span></span>

|<span data-ttu-id="9619f-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="9619f-108">**Name**</span></span>|<span data-ttu-id="9619f-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="9619f-109">**Required/Optional**</span></span>|<span data-ttu-id="9619f-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="9619f-110">**Data Type**</span></span>|<span data-ttu-id="9619f-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9619f-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="9619f-112">_Zelle_</span><span class="sxs-lookup"><span data-stu-id="9619f-112">_cell_</span></span> <br/> |<span data-ttu-id="9619f-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="9619f-113">Required</span></span>  <br/> |<span data-ttu-id="9619f-114">**String**</span><span class="sxs-lookup"><span data-stu-id="9619f-114">**String**</span></span> <br/> |<span data-ttu-id="9619f-115">Die Zelle, deren Formel festgelegt.</span><span class="sxs-lookup"><span data-stu-id="9619f-115">The cell whose formula to set.</span></span>  <br/> |
| <span data-ttu-id="9619f-116">_formula_</span><span class="sxs-lookup"><span data-stu-id="9619f-116">_formula_</span></span> <br/> |<span data-ttu-id="9619f-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="9619f-117">Required</span></span>  <br/> |<span data-ttu-id="9619f-118">**String**</span><span class="sxs-lookup"><span data-stu-id="9619f-118">**String**</span></span> <br/> |<span data-ttu-id="9619f-119">Die zu verwendende Formel.</span><span class="sxs-lookup"><span data-stu-id="9619f-119">The formula to use.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9619f-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9619f-120">Remarks</span></span>

<span data-ttu-id="9619f-121">Wenn ausgewertet, wird das Ergebnis des Ausdrucks in _Formel_ als neue Formel in _Zelle_.</span><span class="sxs-lookup"><span data-stu-id="9619f-121">When evaluated, the result of the expression in  _formula_ becomes the new formula in  _cell_.</span></span> <span data-ttu-id="9619f-122">Wenn die _Formel_ in Anführungszeichen eingeschlossen ist, wird der Ausdruck in Anführungszeichen in _Zelle_geschrieben.</span><span class="sxs-lookup"><span data-stu-id="9619f-122">If  _formula_ is enclosed in quotation marks, the quoted expression is written to  _cell_.</span></span> <span data-ttu-id="9619f-123">Um eine _Zelle_ in eine Zeichenfolge festgelegt, setzen Sie _Formel_ in drei Gruppen von Anführungszeichen.</span><span class="sxs-lookup"><span data-stu-id="9619f-123">To set  _cell_ to a string, enclose  _formula_ in three sets of quotation marks.</span></span> 
  
<span data-ttu-id="9619f-p102">Die Zielzelle muss mithilfe eines GETREF()-Bezugs oder als Zeichenfolge angegeben werden, um eine Zirkularität zu vermeiden. Die Verwendung von GETREF wird bevorzugt, da Bezüge in Microsoft Visio angepasst werden können, wenn das Shape in ein anderes Dokument verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="9619f-p102">The target cell must be specified using a GETREF() reference or as a string to avoid circularity. Using GETREF is preferred, because Microsoft Visio can adjust references when the shape is moved to a different document.</span></span>
  
<span data-ttu-id="9619f-126">Wenn _Zelle_ mithilfe GETREF nicht angegeben ist oder als eine Zeichenfolge ist, gibt die Funktion einen Fehler zurück, und keine Formel geändert wird.</span><span class="sxs-lookup"><span data-stu-id="9619f-126">If  _cell_ is not specified using GETREF or as a string, the function returns an error, and no cell's formula is changed.</span></span> <span data-ttu-id="9619f-127">Wenn die _Formel_ einen Syntaxfehler enthält, gibt die Funktion einen Fehler zurück, und die Formel in _Zelle_ wird nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="9619f-127">If  _formula_ contains a syntax error, the function returns an error, and the formula in  _cell_ is not changed.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="9619f-128">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9619f-128">Example 1</span></span>

<span data-ttu-id="9619f-129">SETF (SETF(GETREF(Scratch.a1), 1,5 cm \* 6 + 1 ft)</span><span class="sxs-lookup"><span data-stu-id="9619f-129">SETF( GETREF(Scratch.A1), 1.5 in \* 6 + 1 ft)</span></span>
  
<span data-ttu-id="9619f-130">Legt die Formel von Scratch.A1 auf 39 cm fest.</span><span class="sxs-lookup"><span data-stu-id="9619f-130">Sets the formula of Scratch.A1 to 21 inches.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="9619f-131">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="9619f-131">Example 2</span></span>

<span data-ttu-id="9619f-132">SETF (GETREF(Scratch.A1), "1,5 cm \* 6 + 1 ft")</span><span class="sxs-lookup"><span data-stu-id="9619f-132">SETF( GETREF(Scratch.A1), "1.5 in \* 6 + 1 ft")</span></span>
  
<span data-ttu-id="9619f-133">Legt die Formel von Scratch.</span><span class="sxs-lookup"><span data-stu-id="9619f-133">Sets the formula of Scratch.</span></span> <span data-ttu-id="9619f-134">A1 auf den Ausdruck 1,5 in\*6 + 1 ft.</span><span class="sxs-lookup"><span data-stu-id="9619f-134">A1 to the expression 1.5 in\*6+1 ft.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="9619f-135">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="9619f-135">Example 3</span></span>

<span data-ttu-id="9619f-136">SETF( GETREF(Scratch.A1), """Sag """"ahh""""""")</span><span class="sxs-lookup"><span data-stu-id="9619f-136">SETF( GETREF(Scratch.A1), """Say """"ahh""""""")</span></span>
  
<span data-ttu-id="9619f-137">Legt die Formel von Scratch.A1 auf die Zeichenfolge "Sag ""ahh""" fest, die in Sag "ahh" ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="9619f-137">Sets the formula of Scratch.A1 to the string "Say ""ahh""" which evaluates to Say "ahh".</span></span>
  
