---
title: Zeile "SplineKnot" (Abschnitt "Geometry")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm3050
localization_priority: Normal
ms.assetid: 9fbae27d-4f1b-c5f7-aacb-16f359331e83
description: Enthält x- und y-Koordinaten für den Kontrollpunkt eines Splines und den Knoten eines Splines.
ms.openlocfilehash: 432b714772d96e0ab0861bbfb62075258404e607
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407417"
---
# <a name="splineknot-row-geometry-section"></a><span data-ttu-id="1bcec-103">Zeile "SplineKnot" (Abschnitt "Geometry")</span><span class="sxs-lookup"><span data-stu-id="1bcec-103">SplineKnot Row (Geometry Section)</span></span>

<span data-ttu-id="1bcec-104">Enthält  *x-*  und  *y-Koordinaten*  für den Kontrollpunkt eines Splines und den Knoten eines Splines.</span><span class="sxs-lookup"><span data-stu-id="1bcec-104">Contains  *x*  - and  *y*  -coordinates for a spline's control point and a spline's knot.</span></span> 
  
<span data-ttu-id="1bcec-105">Eine Zeile SplineKnot enthält folgende Zellen.</span><span class="sxs-lookup"><span data-stu-id="1bcec-105">A SplineKnot row contains the following cells.</span></span>
  
|<span data-ttu-id="1bcec-106">**Cell**</span><span class="sxs-lookup"><span data-stu-id="1bcec-106">**Cell**</span></span>|<span data-ttu-id="1bcec-107">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1bcec-107">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1bcec-108">X</span><span class="sxs-lookup"><span data-stu-id="1bcec-108">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="1bcec-109">Die  x-Koordinate eines Kontrollpunkts.</span><span class="sxs-lookup"><span data-stu-id="1bcec-109">The  *x*  -coordinate of a control point.</span></span>  <br/> |
|[<span data-ttu-id="1bcec-110">Y</span><span class="sxs-lookup"><span data-stu-id="1bcec-110">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="1bcec-111">Die  y-Koordinate eines Kontrollpunkts.</span><span class="sxs-lookup"><span data-stu-id="1bcec-111">The  *y*  -coordinate of a control point.</span></span>  <br/> |
|[<span data-ttu-id="1bcec-112">A</span><span class="sxs-lookup"><span data-stu-id="1bcec-112">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="1bcec-113">Einer der Splineknoten (außer dem letzten bzw. den ersten beiden).</span><span class="sxs-lookup"><span data-stu-id="1bcec-113">One of the spline's knots (other than the last one or the first two).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1bcec-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1bcec-114">Remarks</span></span>

<span data-ttu-id="1bcec-p101">Visio zeigt die Definition eines Splines im Abschnitt Geometry, in dem die Zeile SplineStart enthalten ist, der eine oder mehrere Zeile(n) SplineKnoten nachgestellt ist (sind). Der Zeile SplineStart muss eine andere Art von Zeile vorangehen, etwa MoveTo, die den ersten Kontrollpunkt des Splines anzeigt. Die vorangehende Zeile kann vom Typ LineTo, ArcTo, NURBSTo, PolylineTo oder EllipticalArcTo sein, wenn der Spline einem Segment dieses Typs folgt.</span><span class="sxs-lookup"><span data-stu-id="1bcec-p101">Visio displays the definition of a spline in a Geometry section that contains a SplineStart row followed by one or more SplineKnot rows. The SplineStart row must be preceded by another kind of row, such as a MoveTo row, to indicate the first control point of the spline. The preceding row can be a LineTo, ArcTo, NURBSTo, PolylineTo, or EllipticalArcTo row if the spline follows a segment of that type.</span></span>
  

