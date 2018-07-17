---
title: Zelle "SortKey" (Abschnitt "Shape Data")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251345
localization_priority: Normal
ms.assetid: 67fa5389-f0b9-a9db-8d19-9b16e256dfa3
description: Enthält eine Zeichenfolge, die die Reihenfolge beeinflusst, in der Elemente im Fenster Shape-Daten aufgeführt sind.
ms.openlocfilehash: 1dbc093f2cee509531b8148563fbdb1a777a349f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798174"
---
# <a name="sortkey-cell-shape-data-section"></a><span data-ttu-id="81b86-103">SortKey Cell (Shape Data Section)</span><span class="sxs-lookup"><span data-stu-id="81b86-103">SortKey Cell (Shape Data Section)</span></span>

<span data-ttu-id="81b86-104">Enthält eine Zeichenfolge, die die Reihenfolge beeinflusst, in der Elemente im Fenster **Shape-Daten** aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="81b86-104">Evaluates to a string that influences the order in which items in the **Shape Data** window are listed.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="81b86-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="81b86-105">Remarks</span></span>

<span data-ttu-id="81b86-106">Die Berechnung zum Vergleich von Werten SortKey ist gebietsschemaspezifischen und zwischen Groß-und Kleinschreibung.</span><span class="sxs-lookup"><span data-stu-id="81b86-106">The calculation used to compare SortKey values is locale-specific and case insensitive.</span></span> <span data-ttu-id="81b86-107">Wenn beachtet werden, werden die Shape-Daten in der Zeilenreihenfolge aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="81b86-107">If SortKey values are equal, the shape data is listed in row order.</span></span> <span data-ttu-id="81b86-108">Shape-Daten, die keine Sortierschlüssel werden nach Shape-Daten aufgeführt, die einen Sortierschlüssel enthalten.</span><span class="sxs-lookup"><span data-stu-id="81b86-108">Shape data that have no sort key are listed after shape data that contain a sort key.</span></span>
  
<span data-ttu-id="81b86-109">Nachfolgend sehen Sie ein Beispiel der Verwendung von Sortierschlüsseln um die Shape-Daten im Fenster **Shape-Daten** in der Reihenfolge anzuzeigen: Artikelnummer, Menge, Preis.</span><span class="sxs-lookup"><span data-stu-id="81b86-109">Following is an example of using sort keys to display the shape data in the **Shape Data** window in the order: Item Number, Quantity, Price.</span></span> 
  
 <span data-ttu-id="81b86-110">*Zeile, Beschriftung* und *SortKey* verweisen auf Zellen in der Zeile mit Shape-Daten.</span><span class="sxs-lookup"><span data-stu-id="81b86-110">*Row, Label,*  and  *SortKey*  refer to cells in the shape data row.</span></span> <span data-ttu-id="81b86-111">In diesem Fall wurden die Shape-Datenzeilen benannt.</span><span class="sxs-lookup"><span data-stu-id="81b86-111">In this case, the shape data rows have been named.</span></span> 
  
|<span data-ttu-id="81b86-112">**Row**</span><span class="sxs-lookup"><span data-stu-id="81b86-112">**Row**</span></span>|<span data-ttu-id="81b86-113">**Label**</span><span class="sxs-lookup"><span data-stu-id="81b86-113">**Label**</span></span>|<span data-ttu-id="81b86-114">**SortKey**</span><span class="sxs-lookup"><span data-stu-id="81b86-114">**SortKey**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="81b86-115">Prop.Item</span><span class="sxs-lookup"><span data-stu-id="81b86-115">Prop.Item</span></span>  <br/> | <span data-ttu-id="81b86-116">Artikelnummer</span><span class="sxs-lookup"><span data-stu-id="81b86-116">Item Number</span></span>  <br/> | <span data-ttu-id="81b86-117">1</span><span class="sxs-lookup"><span data-stu-id="81b86-117">1</span></span>  <br/> |
| <span data-ttu-id="81b86-118">Prop.Price</span><span class="sxs-lookup"><span data-stu-id="81b86-118">Prop.Price</span></span>  <br/> | <span data-ttu-id="81b86-119">Preis</span><span class="sxs-lookup"><span data-stu-id="81b86-119">Price</span></span>  <br/> | <span data-ttu-id="81b86-120">3</span><span class="sxs-lookup"><span data-stu-id="81b86-120">3</span></span>  <br/> |
| <span data-ttu-id="81b86-121">Prop.Quan</span><span class="sxs-lookup"><span data-stu-id="81b86-121">Prop.Quan</span></span>  <br/> | <span data-ttu-id="81b86-122">Menge</span><span class="sxs-lookup"><span data-stu-id="81b86-122">Quantity</span></span>  <br/> | <span data-ttu-id="81b86-123">2</span><span class="sxs-lookup"><span data-stu-id="81b86-123">2</span></span>  <br/> |
   
<span data-ttu-id="81b86-124">Wenn Sie einen Verweis auf die Zelle SortKey nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="81b86-124">To get a reference to the SortKey cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="81b86-125">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="81b86-125">Cell name:</span></span>  <br/> | <span data-ttu-id="81b86-126">Eigenschaft.  *Name* . SortKey wobei Prop.  *Name* ist der Name der Zeile mit der benutzerdefinierten Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="81b86-126">Prop.  *Name*  .SortKey where Prop.  *Name*  is the name of the custom property row</span></span>  <br/> |
   
<span data-ttu-id="81b86-127">Wenn Sie einen Verweis auf die Zelle SortKey aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="81b86-127">To get a reference to the SortKey cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="81b86-128">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="81b86-128">Section index:</span></span>  <br/> |<span data-ttu-id="81b86-129">**visSectionProp**</span><span class="sxs-lookup"><span data-stu-id="81b86-129">**visSectionProp**</span></span> <br/> |
| <span data-ttu-id="81b86-130">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="81b86-130">Row index:</span></span>  <br/> |<span data-ttu-id="81b86-131">**VisRowProp** +  *i* wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="81b86-131">**visRowProp** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="81b86-132">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="81b86-132">Cell index:</span></span>  <br/> |<span data-ttu-id="81b86-133">**visCustPropsSortKey**</span><span class="sxs-lookup"><span data-stu-id="81b86-133">**visCustPropsSortKey**</span></span> <br/> |
   
