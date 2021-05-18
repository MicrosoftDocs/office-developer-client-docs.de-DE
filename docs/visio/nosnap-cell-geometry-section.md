---
title: Zelle "NoSnap" (Abschnitt "Geometry")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm740
localization_priority: Normal
ms.assetid: 0e6c8621-868c-9eac-926b-3049f18023b0
description: Definiert, ob andere Shapes an einem Pfad einrasten.
ms.openlocfilehash: 60a6532aee0f391eb38609f6ed87577e5558d5c2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408544"
---
# <a name="nosnap-cell-geometry-section"></a><span data-ttu-id="d9b4f-103">Zelle "NoSnap" (Abschnitt "Geometry")</span><span class="sxs-lookup"><span data-stu-id="d9b4f-103">NoSnap Cell (Geometry Section)</span></span>

<span data-ttu-id="d9b4f-104">Definiert, ob andere Shapes an einem Pfad einrasten.</span><span class="sxs-lookup"><span data-stu-id="d9b4f-104">Determines whether other shapes snap to a path.</span></span>
  
|<span data-ttu-id="d9b4f-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="d9b4f-105">**Value**</span></span>|<span data-ttu-id="d9b4f-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d9b4f-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="d9b4f-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="d9b4f-107">TRUE</span></span>  <br/> | <span data-ttu-id="d9b4f-108">Andere Shapes können nicht an diesem Pfad einrasten.</span><span class="sxs-lookup"><span data-stu-id="d9b4f-108">Do not allow other shapes to snap to this path.</span></span>  <br/> |
| <span data-ttu-id="d9b4f-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="d9b4f-109">FALSE</span></span>  <br/> | <span data-ttu-id="d9b4f-110">Andere Shapes können an diesem Pfad einrasten.</span><span class="sxs-lookup"><span data-stu-id="d9b4f-110">Allow other shapes to snap to this path.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d9b4f-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d9b4f-111">Remarks</span></span>

<span data-ttu-id="d9b4f-112">Um einen Verweis auf die Zelle NoSnap anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="d9b4f-112">To get a reference to the NoSnap cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d9b4f-113">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="d9b4f-113">Cell name:</span></span>  <br/> | <span data-ttu-id="d9b4f-114">Geometry  *i*  . NoSnap, wobei  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="d9b4f-114">Geometry  *i*  .NoSnap            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="d9b4f-115">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die NoSnap-Zelle nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="d9b4f-115">To get a reference to the NoSnap cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d9b4f-116">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="d9b4f-116">Section index:</span></span>  <br/> |<span data-ttu-id="d9b4f-117">**visSectionFirstComponent**  +   *i,* *wobei i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="d9b4f-117">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="d9b4f-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="d9b4f-118">Row index:</span></span>  <br/> |<span data-ttu-id="d9b4f-119">**visRowComponent**</span><span class="sxs-lookup"><span data-stu-id="d9b4f-119">**visRowComponent**</span></span> <br/> |
| <span data-ttu-id="d9b4f-120">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="d9b4f-120">Cell index:</span></span>  <br/> |<span data-ttu-id="d9b4f-121">**visCompNoSnap**</span><span class="sxs-lookup"><span data-stu-id="d9b4f-121">**visCompNoSnap**</span></span> <br/> |
   

