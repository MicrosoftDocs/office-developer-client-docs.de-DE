---
title: Zelle "LineToNodeX" (Abschnitt "Page Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm575
localization_priority: Normal
ms.assetid: 9d58e23e-b411-c5c1-b785-5014488d42c8
description: Legt den horizontalen Abstand zwischen sämtlichen Verbindern und Shapes auf dem Zeichenblatt fest.
ms.openlocfilehash: c5a27edb25ce7b1449ad6e2988027b474bd79fdb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439709"
---
# <a name="linetonodex-cell-page-layout-section"></a><span data-ttu-id="7d1cd-103">Zelle "LineToNodeX" (Abschnitt "Page Layout")</span><span class="sxs-lookup"><span data-stu-id="7d1cd-103">LineToNodeX Cell (Page Layout Section)</span></span>

<span data-ttu-id="7d1cd-104">Legt den horizontalen Abstand zwischen sämtlichen Verbindern und Shapes auf dem Zeichenblatt fest.</span><span class="sxs-lookup"><span data-stu-id="7d1cd-104">Determines the horizontal clearance between all connectors and shapes on the drawing page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7d1cd-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7d1cd-105">Remarks</span></span>

<span data-ttu-id="7d1cd-p101">Sie können den Wert dieser Zelle auch im Dialogfeld **Abstände für Layout und Routing** festlegen. (Klicken Sie dazu auf der Registerkarte **Entwurf** auf den Pfeil neben **Seite einrichten**, wählen Sie **Layout und Routing** aus, und klicken Sie dann auf **Abstand**.)</span><span class="sxs-lookup"><span data-stu-id="7d1cd-p101">You can also set the value of this cell in the **Layout and Routing Spacing** dialog box. (On the **Design** tab, click the **Page Setup** arrow, click **Layout and Routing**, and then click **Spacing**.)</span></span>
  
<span data-ttu-id="7d1cd-108">Um einen Verweis auf die Zelle LineToNodeY anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="7d1cd-108">To get a reference to the LineToNodeY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7d1cd-109">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="7d1cd-109">Cell name:</span></span>  <br/> |<span data-ttu-id="7d1cd-110">LineToNodeX</span><span class="sxs-lookup"><span data-stu-id="7d1cd-110">LineToNodeX</span></span>  <br/> |
   
<span data-ttu-id="7d1cd-111">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die LineToNodeX-Zelle nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="7d1cd-111">To get a reference to the LineToNodeX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7d1cd-112">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="7d1cd-112">Section index:</span></span>  <br/> |<span data-ttu-id="7d1cd-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="7d1cd-113">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="7d1cd-114">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="7d1cd-114">Row index:</span></span>  <br/> |<span data-ttu-id="7d1cd-115">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="7d1cd-115">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="7d1cd-116">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="7d1cd-116">Cell index:</span></span>  <br/> |<span data-ttu-id="7d1cd-117">**visPLOLineToNodeX**</span><span class="sxs-lookup"><span data-stu-id="7d1cd-117">**visPLOLineToNodeX**</span></span> <br/> |
   

