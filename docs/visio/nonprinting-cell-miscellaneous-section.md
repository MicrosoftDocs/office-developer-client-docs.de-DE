---
title: Zelle "NonPrinting" (Abschnitt "Miscellaneous")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251321
localization_priority: Normal
ms.assetid: 59fe0887-2092-4fad-ea38-2aba354f3b92
description: Aktiviert bzw. deaktiviert das Drucken für das ausgewählte Shape.
ms.openlocfilehash: c3e1fc1b2d91fa4808f8ea89c904218c2236f5b0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437259"
---
# <a name="nonprinting-cell-miscellaneous-section"></a><span data-ttu-id="92341-103">Zelle "NonPrinting" (Abschnitt "Miscellaneous")</span><span class="sxs-lookup"><span data-stu-id="92341-103">NonPrinting Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="92341-104">Aktiviert bzw. deaktiviert das Drucken für das ausgewählte Shape.</span><span class="sxs-lookup"><span data-stu-id="92341-104">Switches printing on and off for the selected shape.</span></span>
  
|<span data-ttu-id="92341-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="92341-105">**Value**</span></span>|<span data-ttu-id="92341-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="92341-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="92341-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="92341-107">TRUE</span></span>  <br/> | <span data-ttu-id="92341-108">Das Drucken ist deaktiviert, doch das Shape wird im Zeichnungsfenster angezeigt.</span><span class="sxs-lookup"><span data-stu-id="92341-108">Printing disabled, but the shape will be displayed in the drawing window.</span></span>  <br/> |
| <span data-ttu-id="92341-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="92341-109">FALSE</span></span>  <br/> | <span data-ttu-id="92341-110">Drucken ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="92341-110">Printing enabled.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="92341-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="92341-111">Remarks</span></span>

<span data-ttu-id="92341-112">Sie können eine Führungslinie drucken, indem Sie sie auswählen und anschließend den Wert ihrer Zelle NonPrinting auf FALSE setzen.</span><span class="sxs-lookup"><span data-stu-id="92341-112">You can print a guide by selecting it, and then setting the value of its NonPrinting cell to FALSE.</span></span>
  
<span data-ttu-id="92341-113">Um einen Verweis auf die Zelle NonPrinting anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="92341-113">To get a reference to the NonPrinting cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="92341-114">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="92341-114">Cell name:</span></span>  <br/> | <span data-ttu-id="92341-115">NonPrinting</span><span class="sxs-lookup"><span data-stu-id="92341-115">NonPrinting</span></span>  <br/> |
   
<span data-ttu-id="92341-116">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle NonPrinting nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="92341-116">To get a reference to the NonPrinting cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="92341-117">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="92341-117">Section index:</span></span>  <br/> |<span data-ttu-id="92341-118">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="92341-118">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="92341-119">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="92341-119">Row index:</span></span>  <br/> |<span data-ttu-id="92341-120">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="92341-120">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="92341-121">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="92341-121">Cell index:</span></span>  <br/> |<span data-ttu-id="92341-122">**visNonPrinting**</span><span class="sxs-lookup"><span data-stu-id="92341-122">**visNonPrinting**</span></span> <br/> |
   

