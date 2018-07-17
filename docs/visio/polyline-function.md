---
title: POLYLINE-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251576
localization_priority: Normal
ms.assetid: 10baeec9-6c9b-b4ba-3138-7d1156a9e056
description: Gibt eine Polylinie zurück. Diese Funktion wird in der Zelle PolyLineTo Geometriezeilen verwendet.
ms.openlocfilehash: afe31b3963cca03d0273b8768f6cc5538d1850ee
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797635"
---
# <a name="polyline-function"></a><span data-ttu-id="e4c96-104">POLYLINE Function</span><span class="sxs-lookup"><span data-stu-id="e4c96-104">POLYLINE Function</span></span>

<span data-ttu-id="e4c96-105">Gibt eine Polylinie zurück.</span><span class="sxs-lookup"><span data-stu-id="e4c96-105">Returns a polyline.</span></span> <span data-ttu-id="e4c96-106">Diese Funktion wird in der Zelle PolyLineTo Geometriezeilen verwendet.</span><span class="sxs-lookup"><span data-stu-id="e4c96-106">This function is used in the A cell of PolyLineTo geometry rows.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="e4c96-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e4c96-107">Syntax</span></span>

<span data-ttu-id="e4c96-108">POLYLINIE (** *xTyp gleich* **, ** *gleich* **, ** *X1* **, ** *y1* **...)</span><span class="sxs-lookup"><span data-stu-id="e4c96-108">POLYLINE(** *xType* **, ** *yType* **, ** *x1* **, ** *y1* **...)</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="e4c96-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="e4c96-109">Parameters</span></span>

|<span data-ttu-id="e4c96-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="e4c96-110">**Name**</span></span>|<span data-ttu-id="e4c96-111">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="e4c96-111">**Required/Optional**</span></span>|<span data-ttu-id="e4c96-112">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="e4c96-112">**Data Type**</span></span>|<span data-ttu-id="e4c96-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e4c96-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="e4c96-114">_xTyp gleich_</span><span class="sxs-lookup"><span data-stu-id="e4c96-114">_xType_</span></span> <br/> |<span data-ttu-id="e4c96-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="e4c96-115">Required</span></span>  <br/> |<span data-ttu-id="e4c96-116">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="e4c96-116">**Boolean**</span></span> <br/> |<span data-ttu-id="e4c96-117">Gibt an, wie die _X_ -Eingabedaten interpretiert werden.</span><span class="sxs-lookup"><span data-stu-id="e4c96-117">Specifies how to interpret the  _x_ input data.</span></span> <span data-ttu-id="e4c96-118">Ist _xTyp gleich_ 0, werden die eingegebenen _X_-Daten als Prozentsatz der Breite interpretiert werden.</span><span class="sxs-lookup"><span data-stu-id="e4c96-118">If  _xType_ is 0, the input  _x_-data is interpreted as a percentage of Width.</span></span> <span data-ttu-id="e4c96-119">Ist _xTyp gleich_ 1, werden die eingegebenen _X_-Daten als eine lokale Koordinate interpretiert werden.</span><span class="sxs-lookup"><span data-stu-id="e4c96-119">If  _xType_ is 1, the input  _x_-data is interpreted as a local coordinate.</span></span>  <br/> |
| <span data-ttu-id="e4c96-120">_Gleich_</span><span class="sxs-lookup"><span data-stu-id="e4c96-120">_yType_</span></span> <br/> |<span data-ttu-id="e4c96-121">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="e4c96-121">Required</span></span>  <br/> |<span data-ttu-id="e4c96-122">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="e4c96-122">**Boolean**</span></span> <br/> |<span data-ttu-id="e4c96-123">Gibt an, wie Interpretieren der _y_-Eingabedaten.</span><span class="sxs-lookup"><span data-stu-id="e4c96-123">Specifies how to interpret the  _y_-input data.</span></span> <span data-ttu-id="e4c96-124">Ist _gleich_ 0, werden die eingegebenen _y_-Daten als Prozentsatz der Höhe interpretiert werden.</span><span class="sxs-lookup"><span data-stu-id="e4c96-124">If  _yType_ is 0, the input  _y_-data is interpreted as a percentage of Height.</span></span> <span data-ttu-id="e4c96-125">Ist _gleich_ 1, werden die eingegebenen _y_-Daten als eine lokale Koordinate interpretiert werden.</span><span class="sxs-lookup"><span data-stu-id="e4c96-125">If  _yType_ is 1, the input  _y_-data is interpreted as a local coordinate.</span></span>  <br/> |
| <span data-ttu-id="e4c96-126">_x1_</span><span class="sxs-lookup"><span data-stu-id="e4c96-126">_x1_</span></span> <br/> |<span data-ttu-id="e4c96-127">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="e4c96-127">Required</span></span>  <br/> |<span data-ttu-id="e4c96-128">**Nummer**</span><span class="sxs-lookup"><span data-stu-id="e4c96-128">**Number**</span></span> <br/> | <span data-ttu-id="e4c96-129">Eine _X_-Koordinate.</span><span class="sxs-lookup"><span data-stu-id="e4c96-129">An  _x_-coordinate.</span></span>  <br/> |
| <span data-ttu-id="e4c96-130">_Y1_</span><span class="sxs-lookup"><span data-stu-id="e4c96-130">_y1_</span></span> <br/> |<span data-ttu-id="e4c96-131">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="e4c96-131">Required</span></span>  <br/> |<span data-ttu-id="e4c96-132">**Nummer**</span><span class="sxs-lookup"><span data-stu-id="e4c96-132">**Number**</span></span> <br/> |<span data-ttu-id="e4c96-133">Eine _y_-Koordinate.</span><span class="sxs-lookup"><span data-stu-id="e4c96-133">A  _y_-coordinate.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e4c96-134">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e4c96-134">Remarks</span></span>

<span data-ttu-id="e4c96-135">Für jedes *X* -Argument muss ein *y* -Argument; Andernfalls wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e4c96-135">For every  *x*  argument, there must be a  *y*  argument; otherwise, an error is returned.</span></span> 
  
## <a name="example"></a><span data-ttu-id="e4c96-136">Beispiel</span><span class="sxs-lookup"><span data-stu-id="e4c96-136">Example</span></span>

<span data-ttu-id="e4c96-137">POLYLINE (0, 0, 0, 0, 0, 1, 1, 1, 1, 0, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="e4c96-137">POLYLINE (0, 0, 0, 0, 0, 1, 1, 1, 1, 0, 0, 0)</span></span> 
  
<span data-ttu-id="e4c96-138">Gibt ein Rechteck der Dimensionen Breite x Höhe zurück.</span><span class="sxs-lookup"><span data-stu-id="e4c96-138">Returns a rectangle of dimensions Width x Height.</span></span> 
  
