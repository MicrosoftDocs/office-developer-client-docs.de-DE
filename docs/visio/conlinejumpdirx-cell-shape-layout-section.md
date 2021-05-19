---
title: Zelle "ConLineJumpDirX" (Abschnitt "Shape Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm185
localization_priority: Normal
ms.assetid: f0671835-8d48-907a-eca6-43953658f800
description: Bestimmt die Liniensprungrichtung für Liniensprünge, die bei einem horizontalen dynamischen Verbinder für ein Shape auftreten.
ms.openlocfilehash: 22b9366b750a85a76498b83880aac2b9b974e1ac
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415040"
---
# <a name="conlinejumpdirx-cell-shape-layout-section"></a><span data-ttu-id="4426d-103">Zelle "ConLineJumpDirX" (Abschnitt "Shape Layout")</span><span class="sxs-lookup"><span data-stu-id="4426d-103">ConLineJumpDirX Cell (Shape Layout Section)</span></span>

<span data-ttu-id="4426d-104">Bestimmt die Liniensprungrichtung für Liniensprünge, die bei einem horizontalen dynamischen Verbinder für ein Shape auftreten.</span><span class="sxs-lookup"><span data-stu-id="4426d-104">Determines the line jump direction for line jumps occurring on a horizontal dynamic connector for a shape.</span></span>
  
|<span data-ttu-id="4426d-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="4426d-105">**Value**</span></span>|<span data-ttu-id="4426d-106">**Liniensprungrichtung**</span><span class="sxs-lookup"><span data-stu-id="4426d-106">**Line jump direction**</span></span>|<span data-ttu-id="4426d-107">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="4426d-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="4426d-108">0</span><span class="sxs-lookup"><span data-stu-id="4426d-108">0</span></span>  <br/> | <span data-ttu-id="4426d-109">Zeichenblattstandard</span><span class="sxs-lookup"><span data-stu-id="4426d-109">Page default</span></span>  <br/> |<span data-ttu-id="4426d-110">**visLOJumpDirXDefault**</span><span class="sxs-lookup"><span data-stu-id="4426d-110">**visLOJumpDirXDefault**</span></span> <br/> |
| <span data-ttu-id="4426d-111">1</span><span class="sxs-lookup"><span data-stu-id="4426d-111">1</span></span>  <br/> | <span data-ttu-id="4426d-112">Nach oben</span><span class="sxs-lookup"><span data-stu-id="4426d-112">Up</span></span>  <br/> |<span data-ttu-id="4426d-113">**visLOJumpDirXUp**</span><span class="sxs-lookup"><span data-stu-id="4426d-113">**visLOJumpDirXUp**</span></span> <br/> |
| <span data-ttu-id="4426d-114">2</span><span class="sxs-lookup"><span data-stu-id="4426d-114">2</span></span>  <br/> | <span data-ttu-id="4426d-115">Nach unten</span><span class="sxs-lookup"><span data-stu-id="4426d-115">Down</span></span>  <br/> |<span data-ttu-id="4426d-116">**visLOJumpDirXDown**</span><span class="sxs-lookup"><span data-stu-id="4426d-116">**visLOJumpDirXDown**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4426d-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4426d-117">Remarks</span></span>

<span data-ttu-id="4426d-118">Verwenden Sie die Zelle  PageLineJumpDirX im Abschnitt Seitenlayout, um die standardmäßige horizontale Richtung für alle Verbindersprünge auf einer Seite zu festlegen.</span><span class="sxs-lookup"><span data-stu-id="4426d-118">To set the default horizontal direction for  *all*  connector jumps on a page, use the PageLineJumpDirX cell in the Page Layout section.</span></span> 
  
<span data-ttu-id="4426d-119">Um einen Verweis auf die Zelle ConLineJumpDirX anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="4426d-119">To get a reference to the ConLineJumpDirX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4426d-120">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="4426d-120">Cell name:</span></span>  <br/> | <span data-ttu-id="4426d-121">ConLineJumpDirX</span><span class="sxs-lookup"><span data-stu-id="4426d-121">ConLineJumpDirX</span></span>  <br/> |
   
<span data-ttu-id="4426d-122">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die ConLineJumpDirX-Zelle nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="4426d-122">To get a reference to the ConLineJumpDirX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4426d-123">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="4426d-123">Section index:</span></span>  <br/> |<span data-ttu-id="4426d-124">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="4426d-124">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="4426d-125">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="4426d-125">Row index:</span></span>  <br/> |<span data-ttu-id="4426d-126">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="4426d-126">**visRowShapeLayout**</span></span> <br/> |
| <span data-ttu-id="4426d-127">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="4426d-127">Cell index:</span></span>  <br/> |<span data-ttu-id="4426d-128">**visSLOJumpDirX**</span><span class="sxs-lookup"><span data-stu-id="4426d-128">**visSLOJumpDirX**</span></span> <br/> |
   

