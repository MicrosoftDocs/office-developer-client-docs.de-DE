---
title: Zelle "FillForegnd" (Abschnitt "Fill Format")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251241
localization_priority: Normal
ms.assetid: 7548a480-4dce-45e0-281b-f6f8bdf05c0b
description: Legt die Farbe fest, die für den Vordergrund (Pinselstrich) des Füllmusters des Shapes verwendet wird.
ms.openlocfilehash: 27126457963e4e55419b0cac5baf1eab08fe3cc6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797015"
---
# <a name="fillforegnd-cell-fill-format-section"></a><span data-ttu-id="480a7-103">FillForegnd Cell (Fill Format Section)</span><span class="sxs-lookup"><span data-stu-id="480a7-103">FillForegnd Cell (Fill Format Section)</span></span>

<span data-ttu-id="480a7-104">Legt die Farbe fest, die für den Vordergrund (Pinselstrich) des Füllmusters des Shapes verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="480a7-104">Determines the color used for the foreground (stroke) of the shape's fill pattern.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="480a7-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="480a7-105">Remarks</span></span>

<span data-ttu-id="480a7-106">Wenn Sie die Farbe festlegen möchten, geben Sie eine Zahl von 0 bis 23 ein.</span><span class="sxs-lookup"><span data-stu-id="480a7-106">To set the color, enter a number from 0 to 23.</span></span>
  
<span data-ttu-id="480a7-107">Um eine benutzerdefinierte Farbe eingeben möchten, verwenden Sie die RGB oder HSL-Funktion.</span><span class="sxs-lookup"><span data-stu-id="480a7-107">To enter a custom color, use the RGB or HSL function.</span></span> <span data-ttu-id="480a7-108">Der Wert einer benutzerdefinierten Farbe ist ihre RGB-Farbe und RGB ( *R, g, b*), anstatt eine Zahl in das ShapeSheet-Fenster angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="480a7-108">The value of a custom color is its RGB color, and RGB( *r, g, b*), rather than a number, will be shown in the ShapeSheet window.</span></span> <span data-ttu-id="480a7-109">Bei Verwendung in numerischen Operationen haben benutzerdefinierte Farben Werte von 24 und höher.</span><span class="sxs-lookup"><span data-stu-id="480a7-109">When used in numeric operations, custom colors have values of 24 and above.</span></span> 
  
<span data-ttu-id="480a7-110">Die Fülltransparenz für den Vordergrund können Sie in der Zelle FüllbereichVGrundTrans festlegen.</span><span class="sxs-lookup"><span data-stu-id="480a7-110">You can set the transparency of the foreground fill in the FillForegndTrans cell.</span></span>
  
<span data-ttu-id="480a7-111">Wenn Sie einen Verweis auf die Zelle FillForegnd nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="480a7-111">To get a reference to the FillForegnd cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="480a7-112">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="480a7-112">Cell name:</span></span>  <br/> |<span data-ttu-id="480a7-113">FillForegnd</span><span class="sxs-lookup"><span data-stu-id="480a7-113">FillForegnd</span></span>  <br/> |
   
<span data-ttu-id="480a7-114">Wenn Sie einen Verweis auf die Zelle FillForegnd aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="480a7-114">To get a reference to the FillForegnd cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="480a7-115">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="480a7-115">Section index:</span></span>  <br/> |<span data-ttu-id="480a7-116">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="480a7-116">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="480a7-117">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="480a7-117">Row index:</span></span>  <br/> |<span data-ttu-id="480a7-118">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="480a7-118">**visRowFill**</span></span> <br/> |
|<span data-ttu-id="480a7-119">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="480a7-119">Cell index:</span></span>  <br/> |<span data-ttu-id="480a7-120">**visFillForegnd**</span><span class="sxs-lookup"><span data-stu-id="480a7-120">**visFillForegnd**</span></span> <br/> |
   
