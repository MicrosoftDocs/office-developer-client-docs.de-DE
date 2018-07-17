---
title: Zelle "FlipY" (Abschnitt "Shape Transform")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251198
localization_priority: Normal
ms.assetid: 062022ff-e243-2540-becd-d9b969ce83ce
description: Gibt an, ob das Shape vertikal gekippt wurde.
ms.openlocfilehash: 42ee740a13c3f447f5cd4a6caa9959189320a8af
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797021"
---
# <a name="flipy-cell-shape-transform-section"></a><span data-ttu-id="609a4-103">FlipY Cell (Shape Transform Section)</span><span class="sxs-lookup"><span data-stu-id="609a4-103">FlipY Cell (Shape Transform Section)</span></span>

<span data-ttu-id="609a4-104">Gibt an, ob das Shape vertikal gekippt wurde.</span><span class="sxs-lookup"><span data-stu-id="609a4-104">Indicates whether the shape has been flipped vertically.</span></span>
  
|<span data-ttu-id="609a4-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="609a4-105">**Value**</span></span>|<span data-ttu-id="609a4-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="609a4-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="609a4-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="609a4-107">TRUE</span></span>  <br/> | <span data-ttu-id="609a4-108">Das Shape wurde vertikal gekippt.</span><span class="sxs-lookup"><span data-stu-id="609a4-108">The shape has been flipped vertically.</span></span>  <br/> |
| <span data-ttu-id="609a4-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="609a4-109">FALSE</span></span>  <br/> | <span data-ttu-id="609a4-110">Das Shape wurde nicht vertikal gekippt.</span><span class="sxs-lookup"><span data-stu-id="609a4-110">The shape has not been flipped vertically.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="609a4-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="609a4-111">Remarks</span></span>

<span data-ttu-id="609a4-112">Wenn Sie einen Verweis auf die Zelle FlipY nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="609a4-112">To get a reference to the FlipY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="609a4-113">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="609a4-113">Cell name:</span></span>  <br/> | <span data-ttu-id="609a4-114">FlipY</span><span class="sxs-lookup"><span data-stu-id="609a4-114">FlipY</span></span>  <br/> |
   
<span data-ttu-id="609a4-115">Wenn Sie einen Verweis auf die Zelle FlipY aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="609a4-115">To get a reference to the FlipY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="609a4-116">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="609a4-116">Section index:</span></span>  <br/> |<span data-ttu-id="609a4-117">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="609a4-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="609a4-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="609a4-118">Row index:</span></span>  <br/> |<span data-ttu-id="609a4-119">**visRowXFormOut**</span><span class="sxs-lookup"><span data-stu-id="609a4-119">**visRowXFormOut**</span></span> <br/> |
| <span data-ttu-id="609a4-120">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="609a4-120">Cell index:</span></span>  <br/> |<span data-ttu-id="609a4-121">**visXFormFlipY**</span><span class="sxs-lookup"><span data-stu-id="609a4-121">**visXFormFlipY**</span></span> <br/> |
   
