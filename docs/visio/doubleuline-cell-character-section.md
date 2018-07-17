---
title: Zelle "DoubleULine" (Abschnitt "Character")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm260
localization_priority: Normal
ms.assetid: c18955c8-d653-c29d-d3da-9d3cd0241e17
description: Legt fest, ob der Textbereich doppelt unterstrichen ist.
ms.openlocfilehash: d0a07d8c86bd7e9ed3eb14074dda164f82c92475
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796900"
---
# <a name="doubleuline-cell-character-section"></a><span data-ttu-id="09366-103">Zelle "DoubleULine" (Abschnitt "Character")</span><span class="sxs-lookup"><span data-stu-id="09366-103">DoubleULine Cell (Character Section)</span></span>

<span data-ttu-id="09366-104">Legt fest, ob der Textbereich doppelt unterstrichen ist.</span><span class="sxs-lookup"><span data-stu-id="09366-104">Determines whether the range of text has a double underline below it.</span></span>
  
|<span data-ttu-id="09366-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="09366-105">**Value**</span></span>|<span data-ttu-id="09366-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="09366-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="09366-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="09366-107">TRUE</span></span>  <br/> |<span data-ttu-id="09366-108">Text ist doppelt unterstrichen.</span><span class="sxs-lookup"><span data-stu-id="09366-108">Text has a double underline below it.</span></span>  <br/> |
|<span data-ttu-id="09366-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="09366-109">FALSE</span></span>  <br/> |<span data-ttu-id="09366-110">Text ist nicht doppelt unterstrichen.</span><span class="sxs-lookup"><span data-stu-id="09366-110">Text does not have a double underline below it.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="09366-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="09366-111">Remarks</span></span>

<span data-ttu-id="09366-p101">Die Zelle DoubleULine enthält Formatierungsinformationen für einen Unterbereich des Texts eines Shapes, wenn der Abschnitt Character mehrere Zeilen enthält. Andernfalls enthält diese Zelle Formatierungsinformationen für den gesamten Text des Shapes.</span><span class="sxs-lookup"><span data-stu-id="09366-p101">The DoubleULine cell contains formatting information applied to a sub-range of a shape's text if the Characters section contains multiple rows. Otherwise, it contains formatting information for all of the shape's text.</span></span>
  
<span data-ttu-id="09366-114">Sie können den Wert dieser Zelle auch festlegen, indem Sie das Dialogfeld **Text** verwenden (klicken Sie auf den Pfeil neben **Schriftart** auf der Registerkarte **Start** ).</span><span class="sxs-lookup"><span data-stu-id="09366-114">You can also set the value of this cell by using the **Text** dialog box (click the **Font** arrow on the **Home** tab).</span></span> 
  
<span data-ttu-id="09366-115">Wenn Sie einen Verweis auf die Zelle DoubleULine nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="09366-115">To get a reference to the DoubleULine cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="09366-116">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="09366-116">Cell name:</span></span>  <br/> |<span data-ttu-id="09366-117">Char.DblUnderline [ *i* ] wobei *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="09366-117">Char.DblUnderline[ *i*  ]           where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="09366-118">Wenn Sie einen Verweis auf die Zelle DoubleULine aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="09366-118">To get a reference to the DoubleULine cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="09366-119">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="09366-119">Section index:</span></span>  <br/> |<span data-ttu-id="09366-120">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="09366-120">**visSectionCharacter**</span></span> <br/> |
|<span data-ttu-id="09366-121">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="09366-121">Row index:</span></span>  <br/> |<span data-ttu-id="09366-122">**VisRowCharacter** +  *i* wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="09366-122">**visRowCharacter** +  *i*           where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="09366-123">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="09366-123">Cell index:</span></span>  <br/> |<span data-ttu-id="09366-124">**visCharacterDblUnderline**</span><span class="sxs-lookup"><span data-stu-id="09366-124">**visCharacterDblUnderline**</span></span> <br/> |
   
