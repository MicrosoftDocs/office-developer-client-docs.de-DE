---
title: Zelle "TextPosAfterBullet" (Abschnitt "Paragraph")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60089
localization_priority: Normal
ms.assetid: 08958abb-9d66-5a83-dac3-4cbfd1f6d85e
description: Stellt den Abstand zwischen der ersten Zeile des Absatzes und dem Aufzählungszeichen dar.
ms.openlocfilehash: a98967cb5f9541434745c3b3d6afafde0878074a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422152"
---
# <a name="textposafterbullet-cell-paragraph-section"></a><span data-ttu-id="95e4a-103">Zelle "TextPosAfterBullet" (Abschnitt "Paragraph")</span><span class="sxs-lookup"><span data-stu-id="95e4a-103">TextPosAfterBullet Cell (Paragraph Section)</span></span>

<span data-ttu-id="95e4a-104">Stellt den Abstand zwischen der ersten Zeile des Absatzes und dem Aufzählungszeichen dar.</span><span class="sxs-lookup"><span data-stu-id="95e4a-104">Represents the distance between the first line of the paragraph and the bullet.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="95e4a-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="95e4a-105">Remarks</span></span>

<span data-ttu-id="95e4a-p101">Dieser Abstand wird zum Abstand in der Zelle IndFirst addiert, der den Standardeinzug links darstellt. Dieser Wert ist unabhängig vom Zeichnungsmaßstab.</span><span class="sxs-lookup"><span data-stu-id="95e4a-p101">This distance is added to the distance contained in the IndFirst cell, which is the default left indent. This value is independent of the scale of the drawing.</span></span> 
  
<span data-ttu-id="95e4a-108">Verwenden Sie folgendes, um einen Verweis auf die Zelle TextPosAfterBullet anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="95e4a-108">To get a reference to the TextPosAfterBullet cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="95e4a-109">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="95e4a-109">Cell name:</span></span>  <br/> | <span data-ttu-id="95e4a-110">Para.TextPosAfterBullet[  *i*  ] where  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="95e4a-110">Para.TextPosAfterBullet[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="95e4a-111">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die TextPosAfterBullet-Zelle nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="95e4a-111">To get a reference to the TextPosAfterBullet cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="95e4a-112">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="95e4a-112">Section index:</span></span>  <br/> |<span data-ttu-id="95e4a-113">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="95e4a-113">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="95e4a-114">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="95e4a-114">Row index:</span></span>  <br/> |<span data-ttu-id="95e4a-115">**visRowParagraph**  +   *i,* *wobei i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="95e4a-115">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="95e4a-116">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="95e4a-116">Cell index:</span></span>  <br/> |<span data-ttu-id="95e4a-117">**visTextPosAfterBullet**</span><span class="sxs-lookup"><span data-stu-id="95e4a-117">**visTextPosAfterBullet**</span></span> <br/> |
   

