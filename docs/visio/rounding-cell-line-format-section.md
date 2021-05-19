---
title: Zelle "Rounding" (Abschnitt "Line Format")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm860
localization_priority: Normal
ms.assetid: c44457ca-997a-5315-44dd-4218e4203550
description: Zeigt den Radius des Rundungsbogens an, der sich dort befindet, wo zwei fortlaufende Segmente eines Pfads aufeinander treffen. Die Abrundungsfunktion kann beispielsweise verwendet werden, um die Ecken eines Rechtecks abzurunden. Um die Abrundung festzulegen, geben Sie einen Wert mit einer Maßeinheit ein (d. h. ein Paar aus einer Zahl und einer Einheit).
ms.openlocfilehash: d64d3266e3dd2b0a3998955efe271aab04905fbf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427010"
---
# <a name="rounding-cell-line-format-section"></a><span data-ttu-id="6ada1-105">Zelle "Rounding" (Abschnitt "Line Format")</span><span class="sxs-lookup"><span data-stu-id="6ada1-105">Rounding Cell (Line Format Section)</span></span>

<span data-ttu-id="6ada1-p102">Zeigt den Radius des Rundungsbogens an, der sich dort befindet, wo zwei fortlaufende Segmente eines Pfads aufeinander treffen. Die Abrundungsfunktion kann beispielsweise verwendet werden, um die Ecken eines Rechtecks abzurunden. Um die Abrundung festzulegen, geben Sie einen Wert mit einer Maßeinheit ein (d. h. ein Paar aus einer Zahl und einer Einheit).</span><span class="sxs-lookup"><span data-stu-id="6ada1-p102">Indicates the radius of the rounding arc applied where two contiguous segments of a path meet. For example, rounding can be used to give a rectangle rounded corners. To set rounding, enter a value with units of measure (a number-unit pair).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6ada1-109">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6ada1-109">Remarks</span></span>

<span data-ttu-id="6ada1-110">Sie können diesen Wert  auch im Dialogfeld  Linie festlegen (klicken Sie auf der Registerkarte Start in der **Gruppe Shape** auf **Linie,** zeigen Sie auf **Gewichtung,** und klicken Sie dann auf **Weitere Linien**).</span><span class="sxs-lookup"><span data-stu-id="6ada1-110">You can also set this value in the **Line** dialog box (on the **Home** tab, in the **Shape** group, click **Line**, point to **Weight**, and then click **More Lines**).</span></span>
  
<span data-ttu-id="6ada1-111">Um einen Verweis auf die Rounding-Zelle anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="6ada1-111">To get a reference to the Rounding cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6ada1-112">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="6ada1-112">Cell name:</span></span>  <br/> |<span data-ttu-id="6ada1-113">Rounding</span><span class="sxs-lookup"><span data-stu-id="6ada1-113">Rounding</span></span>  <br/> |
   
<span data-ttu-id="6ada1-114">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Rounding-Zelle nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="6ada1-114">To get a reference to the Rounding cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6ada1-115">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="6ada1-115">Section index:</span></span>  <br/> |<span data-ttu-id="6ada1-116">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="6ada1-116">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="6ada1-117">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="6ada1-117">Row index:</span></span>  <br/> |<span data-ttu-id="6ada1-118">**visRowLine**</span><span class="sxs-lookup"><span data-stu-id="6ada1-118">**visRowLine**</span></span> <br/> |
|<span data-ttu-id="6ada1-119">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="6ada1-119">Cell index:</span></span>  <br/> |<span data-ttu-id="6ada1-120">**visLineRounding**</span><span class="sxs-lookup"><span data-stu-id="6ada1-120">**visLineRounding**</span></span> <br/> |
   

