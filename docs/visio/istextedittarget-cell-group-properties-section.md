---
title: Zelle "IsTextEditTarget" (Abschnitt "Group Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251627
localization_priority: Normal
ms.assetid: 355cef8b-9213-479a-af95-b591f4bc51ad
description: Definiert die Textzuweisung für eine Gruppe.
ms.openlocfilehash: 78a70dc0398745765bca12a1e768390b35fce8ce
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432646"
---
# <a name="istextedittarget-cell-group-properties-section"></a><span data-ttu-id="53433-103">Zelle "IsTextEditTarget" (Abschnitt "Group Properties")</span><span class="sxs-lookup"><span data-stu-id="53433-103">IsTextEditTarget Cell (Group Properties Section)</span></span>

<span data-ttu-id="53433-104">Definiert die Textzuweisung für eine Gruppe.</span><span class="sxs-lookup"><span data-stu-id="53433-104">Determines text assignment for a group.</span></span>
  
|<span data-ttu-id="53433-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="53433-105">**Value**</span></span>|<span data-ttu-id="53433-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="53433-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="53433-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="53433-107">TRUE</span></span>  <br/> |<span data-ttu-id="53433-108">Dem Gruppen-Shape wird Text hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="53433-108">Text is added to the group shape.</span></span>  <br/> |
|<span data-ttu-id="53433-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="53433-109">FALSE</span></span>  <br/> |<span data-ttu-id="53433-110">Text wird dem Shape in der obersten Gruppe des Stapels hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="53433-110">Text is added to the shape in the group at the top of the stacking order.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="53433-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="53433-111">Remarks</span></span>

<span data-ttu-id="53433-112">Sie können diesen Wert auch festlegen, indem Sie die Gruppe auswählen, auf der Registerkarte [Entwickler](run-in-developer-mode-display-the-developer-tab.md) auf **Verhalten** klicken und anschließend das Kontrollkästchen **Text der Gruppe bearbeiten** aktivieren.</span><span class="sxs-lookup"><span data-stu-id="53433-112">You can also set this value by selecting the group, clicking **Behavior** on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, and then selecting the **Edit text of group** check box.</span></span> 
  
<span data-ttu-id="53433-p101">Bei Gruppen, die mit Versionen vor Visio 2000 erstellt wurden, ist der Standardwert FALSE vorgegeben. Ab Visio 2000-Versionen wird der Standardwert TRUE verwendet.</span><span class="sxs-lookup"><span data-stu-id="53433-p101">Groups created in versions earlier than Visio 2000 have a default value of FALSE. Beginning with Visio version 2000, the default value is TRUE.</span></span> 
  
<span data-ttu-id="53433-115">Verwenden Sie folgendes, um einen Verweis auf die Zelle IsTextEditTarget anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="53433-115">To get a reference to the IsTextEditTarget cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="53433-116">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="53433-116">Cell name:</span></span>  <br/> |<span data-ttu-id="53433-117">IsTextEditTarget</span><span class="sxs-lookup"><span data-stu-id="53433-117">IsTextEditTarget</span></span>  <br/> |
   
<span data-ttu-id="53433-118">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die IsTextEditTarget-Zelle nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="53433-118">To get a reference to the IsTextEditTarget cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="53433-119">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="53433-119">Section index:</span></span>  <br/> |<span data-ttu-id="53433-120">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="53433-120">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="53433-121">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="53433-121">Row index:</span></span>  <br/> |<span data-ttu-id="53433-122">**visRowGroup**</span><span class="sxs-lookup"><span data-stu-id="53433-122">**visRowGroup**</span></span> <br/> |
|<span data-ttu-id="53433-123">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="53433-123">Cell index:</span></span>  <br/> |<span data-ttu-id="53433-124">**visGroupIsTextEditTarget**</span><span class="sxs-lookup"><span data-stu-id="53433-124">**visGroupIsTextEditTarget**</span></span> <br/> |
   

