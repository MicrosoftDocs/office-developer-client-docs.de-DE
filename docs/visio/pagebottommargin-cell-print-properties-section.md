---
title: Zelle "PageBottomMargin" (Abschnitt "Print Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60060
localization_priority: Normal
ms.assetid: 7a97e97c-278d-2e1e-6c4f-f5f32e2cdeb0
description: Gibt den unteren Rand der gedruckten Seite an.
ms.openlocfilehash: fb67cf87f5e50719d24b0f354acc93209eed8811
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797575"
---
# <a name="pagebottommargin-cell-print-properties-section"></a><span data-ttu-id="c12af-103">PageBottomMargin Cell (Print Properties Section)</span><span class="sxs-lookup"><span data-stu-id="c12af-103">PageBottomMargin Cell (Print Properties Section)</span></span>

<span data-ttu-id="c12af-104">Gibt den unteren Rand der gedruckten Seite an.</span><span class="sxs-lookup"><span data-stu-id="c12af-104">Specifies the margin at the bottom of the printed page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c12af-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c12af-105">Remarks</span></span>

<span data-ttu-id="c12af-p101">Durch diesen Wert werden physische Einheiten dargestellt, und er wird weder durch Skalierung noch durch Zeichnungseinheiten beeinflusst. Wenn diese Zelle beispielsweise den Wert 0,5 cm aufweist, beträgt der Rand 0,5 Zentimeter, selbst wenn als Einheit der Seite Dezimeter angegeben werden. Wenn keine Einheiten explizit angegeben sind, ist die Standardeinstellung Seiteneinheiten.</span><span class="sxs-lookup"><span data-stu-id="c12af-p101">This value represents physical units and is unaffected by scale or drawing units. For example, if this cell has a value of 0.5 in., this margin is 0.5 inch even if page units are feet. If units are not explicitly stated, this value defaults to page units.</span></span> 
  
<span data-ttu-id="c12af-109">Wenn Sie einen Verweis auf die Zelle PageBottomMargin nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="c12af-109">To get a reference to the PageBottomMargin cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c12af-110">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="c12af-110">Cell name:</span></span>  <br/> | <span data-ttu-id="c12af-111">PageBottomMargin</span><span class="sxs-lookup"><span data-stu-id="c12af-111">PageBottomMargin</span></span>  <br/> |
   
<span data-ttu-id="c12af-112">Wenn Sie einen Verweis auf die Zelle PageBottomMargin aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="c12af-112">To get a reference to the PageBottomMargin cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c12af-113">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="c12af-113">Section index:</span></span>  <br/> |<span data-ttu-id="c12af-114">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c12af-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="c12af-115">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="c12af-115">Row index:</span></span>  <br/> |<span data-ttu-id="c12af-116">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="c12af-116">**visRowPrintProperties**</span></span> <br/> |
| <span data-ttu-id="c12af-117">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="c12af-117">Cell index:</span></span>  <br/> |<span data-ttu-id="c12af-118">**visPrintPropertiesBottomMargin**</span><span class="sxs-lookup"><span data-stu-id="c12af-118">**visPrintPropertiesBottomMargin**</span></span> <br/> |
   
