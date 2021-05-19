---
title: Zelle "PageLeftMargin" (Abschnitt "Print Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60061
localization_priority: Normal
ms.assetid: 7ecdfc37-c9d4-2fde-ed3e-be81657c24e2
description: Gibt den linken Rand der gedruckten Seite an.
ms.openlocfilehash: 289bd0bf16c6dcd9b26ec1a8c7920a29dab724a7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435670"
---
# <a name="pageleftmargin-cell-print-properties-section"></a><span data-ttu-id="a8de5-103">Zelle "PageLeftMargin" (Abschnitt "Print Properties")</span><span class="sxs-lookup"><span data-stu-id="a8de5-103">PageLeftMargin Cell (Print Properties Section)</span></span>

<span data-ttu-id="a8de5-104">Gibt den linken Rand der gedruckten Seite an.</span><span class="sxs-lookup"><span data-stu-id="a8de5-104">Specifies the margin on the left of the printed page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a8de5-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a8de5-105">Remarks</span></span>

<span data-ttu-id="a8de5-p101">Durch diesen Wert werden physische Einheiten dargestellt, und er wird weder durch Skalierung noch durch Zeichnungseinheiten beeinflusst. Wenn diese Zelle beispielsweise den Wert 0,25 cm aufweist, beträgt der Rand 0,25 Zentimeter, selbst wenn als Einheit der Seite Dezimeter angegeben werden. Wenn keine Einheiten explizit angegeben sind, ist die Standardeinstellung Seiteneinheiten.</span><span class="sxs-lookup"><span data-stu-id="a8de5-p101">This value represents physical units and is unaffected by scale or drawing units. For example, if this cell has a value of 0.25 in., this margin is 0.25 inch even if page units are feet. If units are not explicitly stated, this value defaults to page units.</span></span> 
  
<span data-ttu-id="a8de5-109">Um einen Verweis auf die Zelle PageLeftMargin anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="a8de5-109">To get a reference to the PageLeftMargin cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a8de5-110">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="a8de5-110">Cell name:</span></span>  <br/> | <span data-ttu-id="a8de5-111">PageLeftMargin</span><span class="sxs-lookup"><span data-stu-id="a8de5-111">PageLeftMargin</span></span>  <br/> |
   
<span data-ttu-id="a8de5-112">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die PageLeftMargin-Zelle nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="a8de5-112">To get a reference to the PageLeftMargin cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a8de5-113">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="a8de5-113">Section index:</span></span>  <br/> |<span data-ttu-id="a8de5-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="a8de5-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="a8de5-115">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="a8de5-115">Row index:</span></span>  <br/> |<span data-ttu-id="a8de5-116">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="a8de5-116">**visRowPrintProperties**</span></span> <br/> |
| <span data-ttu-id="a8de5-117">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="a8de5-117">Cell index:</span></span>  <br/> |<span data-ttu-id="a8de5-118">**visPrintPropertiesLeftMargin**</span><span class="sxs-lookup"><span data-stu-id="a8de5-118">**visPrintPropertiesLeftMargin**</span></span> <br/> |
   

