---
title: LockReplace Cell (Protection Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b3880511-dd27-4dc2-9e50-a49084ef8195
description: Gibt an, ob eine Form einen Ersetzungsvorgang (als ein Ziel oder ein Replacement-Shape) teilnehmen kann.
ms.openlocfilehash: 6f3e41d6a6c5b28c55e21961de63d0cc20eeb129
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797384"
---
# <a name="lockreplace-cell-protection-section"></a><span data-ttu-id="0d8a6-103">LockReplace Cell (Protection Section)</span><span class="sxs-lookup"><span data-stu-id="0d8a6-103">LockReplace Cell (Protection Section)</span></span>

<span data-ttu-id="0d8a6-104">Gibt an, ob eine Form einen Ersetzungsvorgang (als ein Ziel oder ein Replacement-Shape) teilnehmen kann.</span><span class="sxs-lookup"><span data-stu-id="0d8a6-104">Indicates whether a shape can participate in a replacement operation (as either a target or a replacement shape).</span></span> 
  
|<span data-ttu-id="0d8a6-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="0d8a6-105">**Value**</span></span>|<span data-ttu-id="0d8a6-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0d8a6-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0d8a6-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="0d8a6-107">TRUE</span></span>  <br/> |<span data-ttu-id="0d8a6-108">Das Shape kann nicht ersetzt werden oder als Ersatz-Shape verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0d8a6-108">The shape cannot be replaced or be used as a replacement shape.</span></span>  <br/> <span data-ttu-id="0d8a6-109">Für ein Shape auf die Canvas ist die Schaltfläche **Form ändern** deaktiviert, wenn ein Shape ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="0d8a6-109">For a shape on the canvas, the **Change Shape** button is disabled when the shape is selected.</span></span>  <br/> <span data-ttu-id="0d8a6-110">Für ein Shape in einer Schablone wird die Form nicht als Ersatz-Shape angezeigt, wenn die **Form ändern** Schaltfläche geklickt wird.</span><span class="sxs-lookup"><span data-stu-id="0d8a6-110">For a shape on a stencil, the shape does not appear as a replacement shape when the **Change Shape** button is clicked.</span></span>  <br/> |
|<span data-ttu-id="0d8a6-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="0d8a6-111">FALSE</span></span>  <br/> |<span data-ttu-id="0d8a6-112">Das Shape kann ersetzt oder als Ersatz-Shape verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0d8a6-112">The shape can be replaced or used as a replacement shape.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0d8a6-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0d8a6-113">Remarks</span></span>

<span data-ttu-id="0d8a6-114">Wenn Sie einen Verweis auf die Zelle **LockReplace** nach Namen aus, als Wert des Attributs **N** **ein Zellenelement** , einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="0d8a6-114">To get a reference to the **LockReplace** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0d8a6-115">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="0d8a6-115">Cell name:</span></span>  <br/> | <span data-ttu-id="0d8a6-116">LockReplace</span><span class="sxs-lookup"><span data-stu-id="0d8a6-116">LockReplace</span></span>  <br/> |
   
<span data-ttu-id="0d8a6-117">Wenn Sie einen Verweis auf die Zelle **LockReplace** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="0d8a6-117">To get a reference to the **LockReplace** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0d8a6-118">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="0d8a6-118">Section index:</span></span>  <br/> |<span data-ttu-id="0d8a6-119">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="0d8a6-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="0d8a6-120">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="0d8a6-120">Row index:</span></span>  <br/> |<span data-ttu-id="0d8a6-121">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="0d8a6-121">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="0d8a6-122">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="0d8a6-122">Cell index:</span></span>  <br/> |<span data-ttu-id="0d8a6-123">**visLockReplace**</span><span class="sxs-lookup"><span data-stu-id="0d8a6-123">**visLockReplace**</span></span> <br/> |
   
