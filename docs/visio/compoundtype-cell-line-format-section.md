---
title: CompoundType Cell (Line Format Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3e2a88ad-d92c-4550-8da3-fa7fdd032e73
description: Bestimmt den zusammengesetzten Typ der Zeile eines Shapes.
ms.openlocfilehash: 663b683030251c8b57324f1d2bdf492463c50eef
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796677"
---
# <a name="compoundtype-cell-line-format-section"></a><span data-ttu-id="05d07-103">CompoundType Cell (Line Format Section)</span><span class="sxs-lookup"><span data-stu-id="05d07-103">CompoundType Cell (Line Format Section)</span></span>

<span data-ttu-id="05d07-104">Bestimmt den zusammengesetzten Typ der Zeile eines Shapes.</span><span class="sxs-lookup"><span data-stu-id="05d07-104">Determines the compound type of the line of a shape.</span></span> 
  
|<span data-ttu-id="05d07-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="05d07-105">**Value**</span></span>|<span data-ttu-id="05d07-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="05d07-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="05d07-107">0</span><span class="sxs-lookup"><span data-stu-id="05d07-107">0</span></span>  <br/> |<span data-ttu-id="05d07-108">Einfach</span><span class="sxs-lookup"><span data-stu-id="05d07-108">Simple</span></span>  <br/> |
|<span data-ttu-id="05d07-109">1</span><span class="sxs-lookup"><span data-stu-id="05d07-109">1</span></span>  <br/> |<span data-ttu-id="05d07-110">Double</span><span class="sxs-lookup"><span data-stu-id="05d07-110">Double</span></span>  <br/> |
|<span data-ttu-id="05d07-111">2</span><span class="sxs-lookup"><span data-stu-id="05d07-111">2</span></span>  <br/> |<span data-ttu-id="05d07-112">Dick Dünn</span><span class="sxs-lookup"><span data-stu-id="05d07-112">Thick thin</span></span>  <br/> |
|<span data-ttu-id="05d07-113">3</span><span class="sxs-lookup"><span data-stu-id="05d07-113">3</span></span>  <br/> |<span data-ttu-id="05d07-114">Dünn dick</span><span class="sxs-lookup"><span data-stu-id="05d07-114">Thin thick</span></span>  <br/> |
|<span data-ttu-id="05d07-115">4</span><span class="sxs-lookup"><span data-stu-id="05d07-115">4</span></span>  <br/> |<span data-ttu-id="05d07-116">Dreifach</span><span class="sxs-lookup"><span data-stu-id="05d07-116">Triple</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="05d07-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="05d07-117">Remarks</span></span>

<span data-ttu-id="05d07-118">Wenn Sie einen Verweis auf die Zelle **CompoundType** nach Namen aus, als Wert des Attributs **N** **ein Zellenelement** , einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="05d07-118">To get a reference to the **CompoundType** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="05d07-119">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="05d07-119">Cell name:</span></span>  <br/> | <span data-ttu-id="05d07-120">CompoundType</span><span class="sxs-lookup"><span data-stu-id="05d07-120">CompoundType</span></span>  <br/> |
   
<span data-ttu-id="05d07-121">Wenn Sie einen Verweis auf die Zelle **CompoundType** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="05d07-121">To get a reference to the **CompoundType** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="05d07-122">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="05d07-122">Section index:</span></span>  <br/> |<span data-ttu-id="05d07-123">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="05d07-123">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="05d07-124">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="05d07-124">Row index:</span></span>  <br/> |<span data-ttu-id="05d07-125">**visRowLine**</span><span class="sxs-lookup"><span data-stu-id="05d07-125">**visRowLine**</span></span> <br/> |
| <span data-ttu-id="05d07-126">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="05d07-126">Cell index:</span></span>  <br/> |<span data-ttu-id="05d07-127">**visCompoundType**</span><span class="sxs-lookup"><span data-stu-id="05d07-127">**visCompoundType**</span></span> <br/> |
   
