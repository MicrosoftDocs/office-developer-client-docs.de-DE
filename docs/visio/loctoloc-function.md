---
title: LOCTOLOC-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251586
localization_priority: Normal
ms.assetid: 1f09482a-0b1b-1bef-bc23-7f7793c4c65f
description: Gibt einen transformierten Punkt in lokalen Koordinaten im Zielkoordinatensystem zurück.
ms.openlocfilehash: f08feb6137c3022027d19b45f06285fb8b6441a7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427486"
---
# <a name="loctoloc-function"></a><span data-ttu-id="d9aff-103">LOCTOLOC Function</span><span class="sxs-lookup"><span data-stu-id="d9aff-103">LOCTOLOC Function</span></span>

<span data-ttu-id="d9aff-104">Gibt einen transformierten Punkt in lokalen Koordinaten im Zielkoordinatensystem zurück.</span><span class="sxs-lookup"><span data-stu-id="d9aff-104">Returns a transformed point in local coordinates in the destination coordinate system.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="d9aff-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d9aff-105">Syntax</span></span>

<span data-ttu-id="d9aff-106">LOCTOLOC(\*\* *srcPoint* \*\*, \*\* *srcRef* \*\*, \*\* *dstRef* \*\* )</span><span class="sxs-lookup"><span data-stu-id="d9aff-106">LOCTOLOC(\*\* *srcPoint* \*\*, \*\* *srcRef* \*\*, \*\* *dstRef* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="d9aff-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="d9aff-107">Parameters</span></span>

|<span data-ttu-id="d9aff-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="d9aff-108">**Name**</span></span>|<span data-ttu-id="d9aff-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="d9aff-109">**Required/Optional**</span></span>|<span data-ttu-id="d9aff-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="d9aff-110">**Data Type**</span></span>|<span data-ttu-id="d9aff-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d9aff-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="d9aff-112">_srcPoint_</span><span class="sxs-lookup"><span data-stu-id="d9aff-112">_srcPoint_</span></span> <br/> |<span data-ttu-id="d9aff-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="d9aff-113">Required</span></span>  <br/> |<span data-ttu-id="d9aff-114">**String**</span><span class="sxs-lookup"><span data-stu-id="d9aff-114">**String**</span></span> <br/> | <span data-ttu-id="d9aff-115">Ein Punkt in den lokalen Koordinaten des Quellkoordinatensystems.</span><span class="sxs-lookup"><span data-stu-id="d9aff-115">A point in local coordinates in the source coordinate system.</span></span>  <br/> |
| <span data-ttu-id="d9aff-116">_srcRef_</span><span class="sxs-lookup"><span data-stu-id="d9aff-116">_srcRef_</span></span> <br/> |<span data-ttu-id="d9aff-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="d9aff-117">Required</span></span>  <br/> |<span data-ttu-id="d9aff-118">**String**</span><span class="sxs-lookup"><span data-stu-id="d9aff-118">**String**</span></span> <br/> | <span data-ttu-id="d9aff-119">Ein Bezug auf eine Zelle im Quellobjekt.</span><span class="sxs-lookup"><span data-stu-id="d9aff-119">A reference to a cell in the source object.</span></span>  <br/> |
| <span data-ttu-id="d9aff-120">_dstRef_</span><span class="sxs-lookup"><span data-stu-id="d9aff-120">_dstRef_</span></span> <br/> |<span data-ttu-id="d9aff-121">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="d9aff-121">Required</span></span>  <br/> |<span data-ttu-id="d9aff-122">**String**</span><span class="sxs-lookup"><span data-stu-id="d9aff-122">**String**</span></span> <br/> | <span data-ttu-id="d9aff-123">Ein Bezug auf eine Zelle im Zielobjekt.</span><span class="sxs-lookup"><span data-stu-id="d9aff-123">A reference to a cell in the destination object.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="d9aff-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d9aff-124">Return value</span></span>

<span data-ttu-id="d9aff-125">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="d9aff-125">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d9aff-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d9aff-126">Remarks</span></span>

<span data-ttu-id="d9aff-p101">Die LOCTOLOC-Funktion konvertiert einen Punkt aus lokalen Koordinaten in einem Quell-Shape in die lokalen Koordinaten eines Ziel-Shapes. Sie können diese Funktion verwenden, um beispielsweise ein Shape aus einem Punkt eines anderen Koordinatensystems zu konstruieren. Außerdem können Sie diese Funktion verwenden, um einen lokalen Punkt in Zeichenblattkoordinaten zu transformieren- und umgekehrt.</span><span class="sxs-lookup"><span data-stu-id="d9aff-p101">The LOCTOLOC function converts a point from local coordinates in a source shape to local coordinates in a destination shape. You can use this function to construct a shape, for example, in terms of a point from another coordinate space. You can also use this function to transform a local point to page coordinates, or vice versa.</span></span>
  
<span data-ttu-id="d9aff-p102">Diese Funktion ist auch dann ausführbar, wenn die Ausgangs- und Ziel-Shapes in Gruppen eingebunden sind. Wird ebenfalls für Dreh- und Kippvorgänge in der Zwischentransformation angepasst.</span><span class="sxs-lookup"><span data-stu-id="d9aff-p102">This function works even when the source and destination shapes are within groups. It also adjusts for rotation and flips in the intermediate transformation.</span></span>
  
<span data-ttu-id="d9aff-132">Die Ausgangs- und Zielkoordinaten müssen auf dem gleichen Zeichenblatt liegen.</span><span class="sxs-lookup"><span data-stu-id="d9aff-132">The source and destination coordinates must be on the same page.</span></span>
  
## <a name="example"></a><span data-ttu-id="d9aff-133">Beispiel</span><span class="sxs-lookup"><span data-stu-id="d9aff-133">Example</span></span>

<span data-ttu-id="d9aff-134">Mit der folgenden Formel wird der lokale Pin der form, die der Formel zugeordnet ist, in einen Punkt auf der Seite konvertiert.</span><span class="sxs-lookup"><span data-stu-id="d9aff-134">The following formula converts the local pin of the shape associated with the formula to a point on the page.</span></span>
  
```vb
LOCTOLOC(PNT(LocPinX, LocPinY), Width, ThePage!PageWidth)
```


