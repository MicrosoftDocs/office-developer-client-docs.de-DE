---
title: Zelle "IsDropTarget" (Abschnitt "Group Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm495
localization_priority: Normal
ms.assetid: 8140fc7b-b99c-54bb-7af3-7de6fcdae7d3
description: Legt fest, ob das Shape durch Ablegen auf einer Gruppe dieser Gruppe hinzugefügt werden kann.
ms.openlocfilehash: 326ead15bcdc72797853daee797d8f08d459a638
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797234"
---
# <a name="isdroptarget-cell-group-properties-section"></a><span data-ttu-id="0baa6-103">IsDropTarget Cell (Group Properties Section)</span><span class="sxs-lookup"><span data-stu-id="0baa6-103">IsDropTarget Cell (Group Properties Section)</span></span>

<span data-ttu-id="0baa6-104">Legt fest, ob das Shape durch Ablegen auf einer Gruppe dieser Gruppe hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="0baa6-104">Determines whether the group allows you to add a shape to it by dropping it on the group.</span></span>
  
|<span data-ttu-id="0baa6-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="0baa6-105">**Value**</span></span>|<span data-ttu-id="0baa6-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0baa6-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0baa6-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="0baa6-107">TRUE</span></span>  <br/> |<span data-ttu-id="0baa6-108">Ein Shape kann durch Ablegen auf einer Gruppe dieser Gruppe hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="0baa6-108">Can add a shape to the group by dropping it onto the group.</span></span>  <br/> |
|<span data-ttu-id="0baa6-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="0baa6-109">FALSE</span></span>  <br/> |<span data-ttu-id="0baa6-110">Das Shape kann auf der Gruppe nicht abgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="0baa6-110">Cannot drop shape onto the group.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0baa6-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0baa6-111">Remarks</span></span>

<span data-ttu-id="0baa6-112">Sie können diesen Wert auch festlegen, indem Auswählen der Gruppe auf der Registerkarte [Entwicklertools](run-in-developer-mode-display-the-developer-tab.md) **Verhalten** klicken und anschließend das Kontrollkästchen **abgelegte Shapes annehmen** .</span><span class="sxs-lookup"><span data-stu-id="0baa6-112">You can also set this value by selecting the group, clicking **Behavior** on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, and then selecting the **Accept dropped shapes** check box.</span></span> 
  
<span data-ttu-id="0baa6-113">Um eine Form zu einer Gruppe durch Ablegen der Gruppe hinzufügen möchten, müssen Sie auch ähnliches Shape-Verhalten aktivieren.</span><span class="sxs-lookup"><span data-stu-id="0baa6-113">To add a shape to a group by dropping it on the group, you must also enable similar shape behavior.</span></span> <span data-ttu-id="0baa6-114">Sie müssen das Shape auswählen, klicken Sie auf der Registerkarte [Entwicklertools](run-in-developer-mode-display-the-developer-tab.md) auf **Verhalten** und wählen Sie dann das Kontrollkästchen **Shape beim Ablegen der Gruppe hinzufügen** .</span><span class="sxs-lookup"><span data-stu-id="0baa6-114">You must select the shape, click **Behavior** on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, and then select the **Add shape to groups on drop** check box.</span></span> <span data-ttu-id="0baa6-115">Dieser Wert wird in der Zelle IsDropSource im Abschnitt Miscellaneous gespeichert.</span><span class="sxs-lookup"><span data-stu-id="0baa6-115">This value is stored in the IsDropSource cell in the Miscellaneous section.</span></span> 
  
<span data-ttu-id="0baa6-116">Wenn Sie einen Verweis auf die Zelle IsDropTarget nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="0baa6-116">To get a reference to the IsDropTarget cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0baa6-117">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="0baa6-117">Cell name:</span></span>  <br/> |<span data-ttu-id="0baa6-118">IsDropTarget</span><span class="sxs-lookup"><span data-stu-id="0baa6-118">IsDropTarget</span></span>  <br/> |
   
<span data-ttu-id="0baa6-119">Wenn Sie einen Verweis auf die Zelle IsDropTarget aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="0baa6-119">To get a reference to the IsDropTarget cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0baa6-120">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="0baa6-120">Section index:</span></span>  <br/> |<span data-ttu-id="0baa6-121">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="0baa6-121">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="0baa6-122">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="0baa6-122">Row index:</span></span>  <br/> |<span data-ttu-id="0baa6-123">**visRowGroup**</span><span class="sxs-lookup"><span data-stu-id="0baa6-123">**visRowGroup**</span></span> <br/> |
|<span data-ttu-id="0baa6-124">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="0baa6-124">Cell index:</span></span>  <br/> |<span data-ttu-id="0baa6-125">**visGroupIsDropTarget**</span><span class="sxs-lookup"><span data-stu-id="0baa6-125">**visGroupIsDropTarget**</span></span> <br/> |
   
