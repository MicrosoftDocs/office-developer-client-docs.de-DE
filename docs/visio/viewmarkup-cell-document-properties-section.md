---
title: Zelle "ViewMarkup" (Abschnitt "Document Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1030802
localization_priority: Normal
ms.assetid: 6c956266-8266-3312-5a68-cc9d8bdb8cd9
description: Bestimmt, ob im Zeichnungsfenster Markup angezeigt wird.
ms.openlocfilehash: eeccdd0d14bf28630937b0e480822abb6fb19da5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416405"
---
# <a name="viewmarkup-cell-document-properties-section"></a><span data-ttu-id="5d173-103">Zelle "ViewMarkup" (Abschnitt "Document Properties")</span><span class="sxs-lookup"><span data-stu-id="5d173-103">ViewMarkup Cell (Document Properties Section)</span></span>

<span data-ttu-id="5d173-104">Bestimmt, ob im Zeichnungsfenster Markup angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="5d173-104">Determines whether markup appears in the drawing window.</span></span> 
  
|<span data-ttu-id="5d173-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="5d173-105">**Value**</span></span>|<span data-ttu-id="5d173-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5d173-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5d173-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="5d173-107">TRUE</span></span>  <br/> |<span data-ttu-id="5d173-108">Markup wird in der Zeichnung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5d173-108">Markup is displayed on the drawing.</span></span>  <br/> |
|<span data-ttu-id="5d173-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="5d173-109">FALSE</span></span>  <br/> |<span data-ttu-id="5d173-110">Markup wird nicht angezeigt (Standardwert).</span><span class="sxs-lookup"><span data-stu-id="5d173-110">Markup is not displayed (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5d173-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5d173-111">Remarks</span></span>

 <span data-ttu-id="5d173-112">Wenn die Markupverfolgung aktiviert ist (Zelle AddMarkup ist TRUE), wird die Zelle ViewMarkup automatisch auf TRUE festgelegt und bleibt true, auch wenn die Markupverfolgung deaktiviert wurde (AddMarkup-Zelle ist FALSE).</span><span class="sxs-lookup"><span data-stu-id="5d173-112">When markup tracking is turned on (AddMarkup cell is TRUE), the ViewMarkup cell is automatically set to TRUE and remains TRUE even after markup tracking has been turned off (AddMarkup cell is FALSE).</span></span> <span data-ttu-id="5d173-113">Der Wert in der Zelle ViewMarkup wird ignoriert, wenn die Zelle AddMarkup WAHR ist.</span><span class="sxs-lookup"><span data-stu-id="5d173-113">The value in the ViewMarkup cell is ignored when the AddMarkup cell is TRUE.</span></span> 
  
<span data-ttu-id="5d173-114">Die Zelle ViewMarkup wird ebenfalls auf WAHR festgelegt, wenn Kommentare in eine Zeichnung eingefügt werden (wobei es keine Rolle spielt, ob die Markupverfolgung aktiviert ist oder nicht) und muss auf WAHR festgelegt sein, damit die Kommentare in der Zeichnung sichtbar sind.</span><span class="sxs-lookup"><span data-stu-id="5d173-114">The ViewMarkup cell is also set to TRUE when comments are inserted in a drawing (whether or not markup tracking is turned on) and must be TRUE to see comments in the drawing.</span></span>
  
<span data-ttu-id="5d173-115">Diese Zelle entspricht dem Befehl **Markup anzeigen** in der Gruppe **Markup** der Registerkarte **Überprüfen**.</span><span class="sxs-lookup"><span data-stu-id="5d173-115">This cell corresponds to the **Show Markup** command in the **Markup** group on the **Review** tab.</span></span> 
  
<span data-ttu-id="5d173-116">Verwenden Sie zum Erhalten eines Verweises auf die Zelle ViewMarkup anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft:**</span><span class="sxs-lookup"><span data-stu-id="5d173-116">To get a reference to the ViewMarkup cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5d173-117">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="5d173-117">Cell name:</span></span>  <br/> |<span data-ttu-id="5d173-118">ViewMarkup</span><span class="sxs-lookup"><span data-stu-id="5d173-118">ViewMarkup</span></span>  <br/> |
   
<span data-ttu-id="5d173-119">Um einen Verweis auf die Zelle ViewMarkup nach Index aus einem Programm zu erhalten, verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="5d173-119">To get a reference to the ViewMarkup cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5d173-120">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="5d173-120">Section index:</span></span>  <br/> |<span data-ttu-id="5d173-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="5d173-121">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="5d173-122">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="5d173-122">Row index:</span></span>  <br/> |<span data-ttu-id="5d173-123">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="5d173-123">**visRowDoc**</span></span> <br/> |
|<span data-ttu-id="5d173-124">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="5d173-124">Cell index:</span></span>  <br/> |<span data-ttu-id="5d173-125">**visDocViewMarkup**</span><span class="sxs-lookup"><span data-stu-id="5d173-125">**visDocViewMarkup**</span></span> <br/> |
   

