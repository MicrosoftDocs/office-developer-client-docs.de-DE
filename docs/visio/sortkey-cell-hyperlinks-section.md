---
title: Zelle "SortKey" (Abschnitt "Hyperlinks")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60086
localization_priority: Normal
ms.assetid: 93d7b00c-bd34-6b4e-44fe-afeb8aa9a294
description: Eine Nummer, mit der die Reihenfolge der Hyperlinks im Kontextmenü angegeben wird.
ms.openlocfilehash: 002ab036f5305aa6daa631c15b0e9eb6148a9635
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406381"
---
# <a name="sortkey-cell-hyperlinks-section"></a><span data-ttu-id="744f1-103">Zelle "SortKey" (Abschnitt "Hyperlinks")</span><span class="sxs-lookup"><span data-stu-id="744f1-103">SortKey Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="744f1-104">Eine Nummer, mit der die Reihenfolge der Hyperlinks im Kontextmenü angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="744f1-104">A number that determines the order of hyperlinks that appear on a shortcut menu.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="744f1-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="744f1-105">Remarks</span></span>

<span data-ttu-id="744f1-p101">Die Hyperlinks in Kontextmenüs werden von unten nach oben sortiert, wobei die Hyperlinks mit der kleinsten Nummer im Menü an oberster Stelle angezeigt werden. Wenn zwei Hyperlinks für die Zelle SortKey denselben Wert aufweisen, wird die Reihenfolge durch die physische Zeilenreihenfolge bestimmt. Der Standardwert ist 0 (Null).</span><span class="sxs-lookup"><span data-stu-id="744f1-p101">The hyperlinks on a shortcut menu appear on the menu sorted from lowest to highest, with lower numbers appearing at the top of the menu. If two hyperlink rows have the same SortKey cell value, the order is determined by physical row order. The default is 0 (zero).</span></span> 
  
<span data-ttu-id="744f1-109">Verwenden Sie zum Erhalten eines Verweises auf die Zelle SortKey anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft:**</span><span class="sxs-lookup"><span data-stu-id="744f1-109">To get a reference to the SortKey cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="744f1-110">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="744f1-110">Cell name:</span></span>  <br/> |<span data-ttu-id="744f1-111">Hyperlink.</span><span class="sxs-lookup"><span data-stu-id="744f1-111">Hyperlink.</span></span> <span data-ttu-id="744f1-112">*Name*  . SortKey, wobei Hyperlink  *.name*  der Zeilenname ist</span><span class="sxs-lookup"><span data-stu-id="744f1-112">*name*  .SortKey where Hyperlink  *.name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="744f1-113">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle SortKey nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="744f1-113">To get a reference to the SortKey cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="744f1-114">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="744f1-114">Section index:</span></span>  <br/> |<span data-ttu-id="744f1-115">**visSectionHyperlink**</span><span class="sxs-lookup"><span data-stu-id="744f1-115">**visSectionHyperlink**</span></span> <br/> |
|<span data-ttu-id="744f1-116">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="744f1-116">Row index:</span></span>  <br/> |<span data-ttu-id="744f1-117">**visRow1stHyperlink**  +   *i,* *wobei i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="744f1-117">**visRow1stHyperlink** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="744f1-118">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="744f1-118">Cell index:</span></span>  <br/> |<span data-ttu-id="744f1-119">**visHLinkSortKey**</span><span class="sxs-lookup"><span data-stu-id="744f1-119">**visHLinkSortKey**</span></span> <br/> |
   

