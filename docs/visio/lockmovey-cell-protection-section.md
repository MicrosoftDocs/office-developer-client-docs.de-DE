---
title: Zelle "LockMoveY" (Abschnitt "Protection")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm645
localization_priority: Normal
ms.assetid: 4ed8cab4-112a-e96a-f4e3-02490a6f87fa
description: Sperrt die vertikale Position des Shapes, damit es nicht vertikal verschoben werden kann.
ms.openlocfilehash: 24f6f477860ea3634cfdcfd92199f2de65e543db
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797382"
---
# <a name="lockmovey-cell-protection-section"></a><span data-ttu-id="b65b8-103">LockMoveY Cell (Protection Section)</span><span class="sxs-lookup"><span data-stu-id="b65b8-103">LockMoveY Cell (Protection Section)</span></span>

<span data-ttu-id="b65b8-104">Sperrt die vertikale Position des Shapes, damit es nicht vertikal verschoben werden kann.</span><span class="sxs-lookup"><span data-stu-id="b65b8-104">Locks the vertical position of the shape so it cannot be moved vertically.</span></span>
  
|<span data-ttu-id="b65b8-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="b65b8-105">**Value**</span></span>|<span data-ttu-id="b65b8-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b65b8-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="b65b8-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="b65b8-107">TRUE</span></span>  <br/> | <span data-ttu-id="b65b8-108">Vertikale Position ist gesperrt.</span><span class="sxs-lookup"><span data-stu-id="b65b8-108">Vertical position is locked.</span></span>  <br/> |
| <span data-ttu-id="b65b8-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="b65b8-109">FALSE</span></span>  <br/> | <span data-ttu-id="b65b8-110">Vertikale Position ist nicht gesperrt.</span><span class="sxs-lookup"><span data-stu-id="b65b8-110">Vertical position is not locked.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b65b8-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b65b8-111">Remarks</span></span>

<span data-ttu-id="b65b8-112">Wenn Sie einen Verweis auf die Zelle LockMoveY nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="b65b8-112">To get a reference to the LockMoveY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b65b8-113">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="b65b8-113">Cell name:</span></span>  <br/> | <span data-ttu-id="b65b8-114">LockMoveY</span><span class="sxs-lookup"><span data-stu-id="b65b8-114">LockMoveY</span></span>  <br/> |
   
<span data-ttu-id="b65b8-115">Wenn Sie einen Verweis auf die Zelle LockMoveY aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="b65b8-115">To get a reference to the LockMoveY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b65b8-116">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="b65b8-116">Section index:</span></span>  <br/> |<span data-ttu-id="b65b8-117">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b65b8-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="b65b8-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="b65b8-118">Row index:</span></span>  <br/> |<span data-ttu-id="b65b8-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="b65b8-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="b65b8-120">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="b65b8-120">Cell index:</span></span>  <br/> |<span data-ttu-id="b65b8-121">**visLockMoveY**</span><span class="sxs-lookup"><span data-stu-id="b65b8-121">**visLockMoveY**</span></span> <br/> |
   
