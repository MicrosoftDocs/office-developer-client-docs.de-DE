---
title: Zelle "TxtHeight" (Abschnitt "Text Transform")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1025
localization_priority: Normal
ms.assetid: cfa3ecc6-61a8-506c-ba1d-b5e1f757d44f
description: 'Definiert die Höhe eines Textblocks. Die Standardformel lautet:'
ms.openlocfilehash: e9495eef837a61fa9b7ecb2b242fdabc5df30080
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798326"
---
# <a name="txtheight-cell-text-transform-section"></a><span data-ttu-id="ae000-104">Zelle "TxtHeight" (Abschnitt "Text Transform")</span><span class="sxs-lookup"><span data-stu-id="ae000-104">TxtHeight Cell (Text Transform Section)</span></span>

<span data-ttu-id="ae000-p102">Definiert die Höhe eines Textblocks. Die Standardformel lautet:</span><span class="sxs-lookup"><span data-stu-id="ae000-p102">Determines the height of the text block. The default formula is:</span></span>
  
<span data-ttu-id="ae000-107">= Höhe \* 1</span><span class="sxs-lookup"><span data-stu-id="ae000-107">= Height \* 1</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ae000-108">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ae000-108">Remarks</span></span>

<span data-ttu-id="ae000-109">Wenn Sie einen Verweis auf die Zelle TxtHeight nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="ae000-109">To get a reference to the TxtHeight cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ae000-110">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="ae000-110">Cell name:</span></span>  <br/> | <span data-ttu-id="ae000-111">TxtHeight</span><span class="sxs-lookup"><span data-stu-id="ae000-111">TxtHeight</span></span>  <br/> |
   
<span data-ttu-id="ae000-112">Wenn Sie einen Verweis auf die Zelle TxtHeight aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="ae000-112">To get a reference to the TxtHeight cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ae000-113">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="ae000-113">Section index:</span></span>  <br/> |<span data-ttu-id="ae000-114">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="ae000-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="ae000-115">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="ae000-115">Row index:</span></span>  <br/> |<span data-ttu-id="ae000-116">**visRowTextXForm**</span><span class="sxs-lookup"><span data-stu-id="ae000-116">**visRowTextXForm**</span></span> <br/> |
| <span data-ttu-id="ae000-117">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="ae000-117">Cell index:</span></span>  <br/> |<span data-ttu-id="ae000-118">**visXFormHeight**</span><span class="sxs-lookup"><span data-stu-id="ae000-118">**visXFormHeight**</span></span> <br/> |
   
