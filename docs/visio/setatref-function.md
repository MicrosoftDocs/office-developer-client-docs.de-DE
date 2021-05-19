---
title: SETATREF-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60113
localization_priority: Normal
ms.assetid: 1ecfdb05-2533-470a-006b-e554026944d8
description: Leitet aktualisierte Werte, die sich aus Aktionen auf der Benutzeroberfläche oder Automatisierung ergeben, in eine andere Zelle um.
ms.openlocfilehash: c4f5fe94aba90ce0a69983d6637a5399b6e42707
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416804"
---
# <a name="setatref-function"></a><span data-ttu-id="ae997-103">SETATREF Function</span><span class="sxs-lookup"><span data-stu-id="ae997-103">SETATREF Function</span></span>

<span data-ttu-id="ae997-104">Leitet aktualisierte Werte, die sich aus Aktionen auf der Benutzeroberfläche oder Automatisierung ergeben, in eine andere Zelle um.</span><span class="sxs-lookup"><span data-stu-id="ae997-104">Redirects updated values resulting from actions in the user interface (UI) or Automation to another cell.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="ae997-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ae997-105">Syntax</span></span>

<span data-ttu-id="ae997-106">SETATREF(\*\* *reference* \*\* [, \*\* *set_expression* \*\* [, \*\* *ignore_eval* \*\* ]])</span><span class="sxs-lookup"><span data-stu-id="ae997-106">SETATREF(\*\* *reference* \*\* [, \*\* *set_expression* \*\* [, \*\* *ignore_eval* \*\* ]])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="ae997-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="ae997-107">Parameters</span></span>

|<span data-ttu-id="ae997-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="ae997-108">**Name**</span></span>|<span data-ttu-id="ae997-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="ae997-109">**Required/Optional**</span></span>|<span data-ttu-id="ae997-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="ae997-110">**Data Type**</span></span>|<span data-ttu-id="ae997-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ae997-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="ae997-112">_reference_</span><span class="sxs-lookup"><span data-stu-id="ae997-112">_reference_</span></span> <br/> |<span data-ttu-id="ae997-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="ae997-113">Required</span></span>  <br/> |<span data-ttu-id="ae997-114">**String**</span><span class="sxs-lookup"><span data-stu-id="ae997-114">**String**</span></span> <br/> |<span data-ttu-id="ae997-115">Ein Bezug auf die Zelle, in die Aktualisierungen umgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="ae997-115">A reference to the cell where updates are redirected.</span></span>  <br/> |
| <span data-ttu-id="ae997-116">_set_expression_</span><span class="sxs-lookup"><span data-stu-id="ae997-116">_set_expression_</span></span> <br/> |<span data-ttu-id="ae997-117">Optional</span><span class="sxs-lookup"><span data-stu-id="ae997-117">Optional</span></span>  <br/> |<span data-ttu-id="ae997-118">**String**</span><span class="sxs-lookup"><span data-stu-id="ae997-118">**String**</span></span> <br/> |<span data-ttu-id="ae997-119">Ein Ausdruck, der dem Verweis _zugewiesen ist._</span><span class="sxs-lookup"><span data-stu-id="ae997-119">An expression that is assigned to  _reference_.</span></span>  <br/> |
| <span data-ttu-id="ae997-120">_ignore_eval_</span><span class="sxs-lookup"><span data-stu-id="ae997-120">_ignore_eval_</span></span> <br/> |<span data-ttu-id="ae997-121">Optional</span><span class="sxs-lookup"><span data-stu-id="ae997-121">Optional</span></span>  <br/> |<span data-ttu-id="ae997-122">**Boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="ae997-122">**Boolean**</span></span> <br/> |<span data-ttu-id="ae997-123">Bei TRUE wird die SETATREF-Funktion als (0) Null ausgewertet. bei FALSE (Standardeinstellung) wird die SETATREF-Funktion zum Wert des Verweises _ausgewertet._</span><span class="sxs-lookup"><span data-stu-id="ae997-123">If TRUE, the SETATREF function evaluates to (0) zero; if FALSE (the default) the SETATREF function evaluates to the value of  _reference_.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ae997-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ae997-124">Remarks</span></span>

<span data-ttu-id="ae997-125">Wenn eine Benutzeraktion im Zeichnungsfenster oder eine Automatisierungsmethode bewirkt, dass Microsoft Visio eine Zelle mit einer SETATREF-Formel aktualisiert, wird der Wert stattdessen an die Zelle umgeleitet, auf die durch die SETATREF-Formel ( _Reference_) verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="ae997-125">When a user action in the drawing window, or an Automation method, causes Microsoft Visio to update a cell containing a SETATREF formula, the value is instead redirected to the cell referenced by the SETATREF formula ( _reference_).</span></span> <span data-ttu-id="ae997-126">Die Formel in der Zelle mit der SETATREF-Funktion bleibt erhalten.</span><span class="sxs-lookup"><span data-stu-id="ae997-126">The formula in the cell containing the SETATREF function remains intact.</span></span>
  
<span data-ttu-id="ae997-127">Wenn  _set_expression_ nicht angegeben wird, wird der in der Benutzeroberfläche oder mithilfe der Automatisierung festgelegte Wert der referenzierten Zelle zugewiesen. Andernfalls wird der Inhalt  _set_expression_ zelle zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="ae997-127">If  _set_expression_ is omitted, the value set in the UI or by using Automation is assigned to the referenced cell; otherwise, the contents of  _set_expression_ are assigned to the referenced cell.</span></span> <span data-ttu-id="ae997-128">Dadurch kann der neue Wert geändert oder transformiert werden, bevor er der referenzierten Zelle zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="ae997-128">This allows the new value to be modified or transformed before being assigned to the referenced cell.</span></span> 
  
<span data-ttu-id="ae997-129">Die SETATREF-Funktion besitzt zwei verwandte Funktionen:</span><span class="sxs-lookup"><span data-stu-id="ae997-129">The SETATREF function has two related functions:</span></span> 
  
- <span data-ttu-id="ae997-130">Die SETATREFEXPR-Funktion, mit der Sie den neuen Wert innerhalb von _set_expression._</span><span class="sxs-lookup"><span data-stu-id="ae997-130">The SETATREFEXPR function, which you can use to represent the new value within  _set_expression_.</span></span> <span data-ttu-id="ae997-131">Beispiel: eine  _set_expression_ SETATREFEXPR()-2 in.</span><span class="sxs-lookup"><span data-stu-id="ae997-131">For example, a  _set_expression_ of SETATREFEXPR()-2 in.</span></span> <span data-ttu-id="ae997-132">kann verwendet werden, um 2 Zoll vom SETATREFEXPR-Ergebnis zu subtrahieren.</span><span class="sxs-lookup"><span data-stu-id="ae997-132">could be used to subtract 2 inches from the SETATREFEXPR result.</span></span> 
    
- <span data-ttu-id="ae997-133">Die SETATREFEVAL-Funktion, mit der Sie angeben  können, dass ein Teil der set_expression ausgewertet und durch das Ergebnis ersetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ae997-133">The SETATREFEVAL function, which you can use to indicate that some portion of  _set_expression_ should be evaluated and replaced by its result.</span></span> 
    
<span data-ttu-id="ae997-134">Die SETATREF-Funktion ist für die Verwendung in Zellen konzipiert, die durch Benutzeraktionen im Zeichnungsfenster geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="ae997-134">The SETATREF function is designed for use in cells that can be changed by user actions in the drawing window.</span></span> <span data-ttu-id="ae997-135">Folgende Zellen werden unterstützt:</span><span class="sxs-lookup"><span data-stu-id="ae997-135">The following cells are supported:</span></span>
  
- <span data-ttu-id="ae997-136">Abschnitt ShapeTransform - Zelle Width, Height, Angle, PinX und PinY</span><span class="sxs-lookup"><span data-stu-id="ae997-136">ShapeTransform section—Width, Height, Angle, PinX, and PinY cells</span></span>
    
- <span data-ttu-id="ae997-137">Abschnitt Text Transform - Zelle TxtWidth, TxtHeight, TxtAngle, TxtPinX und TxtPinY</span><span class="sxs-lookup"><span data-stu-id="ae997-137">Text Transform section—TxtWidth, TxtHeight, TxtAngle, TxtPinX, and TxtPinY cells</span></span>
    
- <span data-ttu-id="ae997-138">Abschnitt 1-D Endpoints - Zelle BeginX, BeginY, EndX und EndY</span><span class="sxs-lookup"><span data-stu-id="ae997-138">1-D Endpoints section—BeginX, BeginY, EndX, and EndY cells</span></span>
    
- <span data-ttu-id="ae997-139">Abschnitt Controls - Zelle Controls.X und Controls.Y</span><span class="sxs-lookup"><span data-stu-id="ae997-139">Controls section—Controls.X and Controls.Y cells</span></span>
    
- <span data-ttu-id="ae997-140">Abschnitt Shape Data</span><span class="sxs-lookup"><span data-stu-id="ae997-140">Shape Data section</span></span>
    
<span data-ttu-id="ae997-141">Da SETATREF den Speicherort von Zellwertänderungen ändert, wird das Auslösen von Ereignissen beeinflusst.</span><span class="sxs-lookup"><span data-stu-id="ae997-141">Because SETATREF changes the location where cell values change, it affects event firing.</span></span> <span data-ttu-id="ae997-142">Wenn eine Zelle SETATREF enthält, werden das **FormulaChanged**-Ereignis und das **CellChanged**-Ereignis für die von SETATREF referenzierte Zelle ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="ae997-142">If a cell contains SETATREF, the **FormulaChanged** and **CellChanged** events fire for the cell that is referenced by SETATREF, not the cell containing SETATREF.</span></span> <span data-ttu-id="ae997-143">Wenn eine Zelle, die SETATREF enthält, auch SETATREFEXPR enthält, wird das **FormulaChanged-Ereignis** auch für die Zelle ausgelöst, die SETATREF enthält, da ein Funktionsparameter geändert wird.</span><span class="sxs-lookup"><span data-stu-id="ae997-143">If a cell containing SETATREF also contains SETATREFEXPR, the **FormulaChanged** event also fires for the cell containing SETATREF because a function parameter is changed.</span></span> 
  
<span data-ttu-id="ae997-144">Beachten Sie folgende weiteren wichtigen Hinweise zur SETATREF-Funktion:</span><span class="sxs-lookup"><span data-stu-id="ae997-144">Other important points to note about the SETATREF function include the following:</span></span>
  
- <span data-ttu-id="ae997-145">SETATREF-Funktionen können bis zu 10 Referenzen auf andere SETATREF-Funktionen verketten.</span><span class="sxs-lookup"><span data-stu-id="ae997-145">SETATREF functions can chain up to 10 references to other SETATREF functions.</span></span> 
    
- <span data-ttu-id="ae997-146">Zellen können zusätzlich zur SETATREF-Funktion andere Ausdrücke enthalten, einschließlich mehrerer Vorkommen von SETATREF in einer einzigen Zelle.</span><span class="sxs-lookup"><span data-stu-id="ae997-146">Cells can contain other expressions in addition to the SETATREF function, including multiple occurrences of SETATREF in a single cell.</span></span>
    
- <span data-ttu-id="ae997-147">Wenn Shapes verbunden werden, folgt Visio der SETATREF-Referenzkette innerhalb desselben Blatts und platziert Klebeformeln in der referenzierten Zelle.</span><span class="sxs-lookup"><span data-stu-id="ae997-147">If shapes are glued, Visio follows the SETATREF reference chain within the same sheet and places glue formulas in the referenced cell.</span></span> 
    
- <span data-ttu-id="ae997-148">Die Automatisierung erkennt die SETATREF-Funktion und folgt der Kette referenzierter Zellen.</span><span class="sxs-lookup"><span data-stu-id="ae997-148">Automation recognizes the SETATREF function and follows the chain of referenced cells.</span></span> 
    
- <span data-ttu-id="ae997-149">Ebenso wie GUARD schützt SETATREF die Zellen nicht vor Änderungen, die über die SETF-Funktion im ShapeSheet-Fenster vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="ae997-149">Like GUARD, SETATREF does not protect cells from changes made by using the SETF function in the ShapeSheet.</span></span>
    
## <a name="example1"></a><span data-ttu-id="ae997-150">Beispiel1</span><span class="sxs-lookup"><span data-stu-id="ae997-150">Example1</span></span>

<span data-ttu-id="ae997-151">Angenommen, ein Shape besitzt die benutzerdefinierte Eigenschaft Breite und die Zelle Width im Abschnitt Shape Transform enthält folgende Formel:</span><span class="sxs-lookup"><span data-stu-id="ae997-151">Let's say that a shape has a custom property called Width, and that the Width cell in the Shape Transform section contains the following formula:</span></span>
  
<span data-ttu-id="ae997-152">=SETATREF(Prop.Width)</span><span class="sxs-lookup"><span data-stu-id="ae997-152">=SETATREF(Prop.Width)</span></span>
  
<span data-ttu-id="ae997-153">Wenn ein Benutzer die Breite der Form in der Benutzeroberfläche ändern soll, wird der neue Wert der Zelle Prop.Width und nicht der Zelle Width im Abschnitt ShapeTransform zugewiesen. die Formel in der Zelle Width bleibt unverändert.</span><span class="sxs-lookup"><span data-stu-id="ae997-153">If a user were to change the shape's width in the UI, the new value is assigned to the Prop.Width cell, not to the Width cell in the ShapeTransform section; the formula in the Width cell remains unchanged.</span></span> <span data-ttu-id="ae997-154">Sie können die Breite des Shapes auch mithilfe von Formdaten festlegen.</span><span class="sxs-lookup"><span data-stu-id="ae997-154">You can also set the shape's width by using shape data.</span></span>
  
## <a name="example2"></a><span data-ttu-id="ae997-155">Beispiel2</span><span class="sxs-lookup"><span data-stu-id="ae997-155">Example2</span></span>

<span data-ttu-id="ae997-p107">Visio-Lösungen enthalten oft Shapes mit hierarchischen Beziehungen, bei denen untergeordnete Shapes verschoben werden müssen, wenn ein übergeordnetes Shape verschoben wird. Im folgenden Beispiel wird beschrieben, wie Sie diese Beziehung mithilfe der SETATREF-Funktion im ShapeSheet-Fenster verwalten können.</span><span class="sxs-lookup"><span data-stu-id="ae997-p107">Visio solutions often have shapes that have a hierarchical relationship, requiring child shapes to move when a parent shape is moved. Following is an example of how you might manage this relationship using the SETATREF function in the ShapeSheet.</span></span> 
  
<span data-ttu-id="ae997-p108">Folgende Formeln sind im Abschnitt Shape Transform des untergeordneten Shapes enthalten. Außerdem werden die benutzerdefinierten Zellen User.DeltaX und User.DeltaY definiert, die den Abstand von ParentShape verfolgen. Auf diese Weise kann das untergeordnete Shape verschoben werden, wenn das übergeordnete Shape verschoben wird, und die hierarchische Beziehung bleibt erhalten.</span><span class="sxs-lookup"><span data-stu-id="ae997-p108">The following formulas are contained in the Shape Transform section of the child shape. Also, we define user cells called User.DeltaX and User.DeltaY, which track the offset dimension from ParentShape. This allows the child shape to move when the parent shape is moved, and also to preserve the hierarchical relationship if the child shape is moved.</span></span>
  
<span data-ttu-id="ae997-161">PinX =SETATREF(User.DeltaX, SETATREFEVAL(SETATREFEXPR() - ParentShape!PinX)) + ParentShape!PinX</span><span class="sxs-lookup"><span data-stu-id="ae997-161">PinX =SETATREF(User.DeltaX, SETATREFEVAL(SETATREFEXPR() - ParentShape!PinX)) + ParentShape!PinX</span></span>
  
<span data-ttu-id="ae997-162">PinY =SETATREF(User.DeltaY, SETATREFEVAL(SETATREFEXPR() - ParentShape!PinY)) + ParentShape!PinY</span><span class="sxs-lookup"><span data-stu-id="ae997-162">PinY =SETATREF(User.DeltaY, SETATREFEVAL(SETATREFEXPR() - ParentShape!PinY)) + ParentShape!PinY</span></span>
  
<span data-ttu-id="ae997-163">Wenn das untergeordnete Shape mithilfe der Benutzeroberfläche verschoben wird, werden die neuen PinX- und PinY-Werte als Parameter in der SETATREFEXPR-Funktion festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ae997-163">When the child shape is moved using the UI, the new PinX and PinY values are set as the parameter in the SETATREFEXPR function.</span></span> <span data-ttu-id="ae997-164">Die SETATREF-Funktion wertet die in SETATREFEVAL eingeschlossene Formel aus und ersetzt PinX und PinY durch ihre Ergebnisse, und dann wird die resultierende Formel den Benutzerzellen zugewiesen, auf die in der SETATREF-Funktion verwiesen wird: User.DeltaX und User.DeltaY.</span><span class="sxs-lookup"><span data-stu-id="ae997-164">The SETATREF function evaluates the formula enclosed in SETATREFEVAL and replaces PinX and PinY with their results, and then the resulting formula is assigned to the user cells referenced in the SETATREF function—User.DeltaX and User.DeltaY.</span></span> <span data-ttu-id="ae997-165">Schließlich werden die von SETATREF (User.DeltaX oder User.DeltaY) zurückgegebenen Werte der Pinposition von ParentShape hinzugefügt, um die Pinposition des untergeordneten Shapes zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="ae997-165">Lastly, the values returned by SETATREF (User.DeltaX or User.DeltaY) are added to the pin location of ParentShape to calculate the child shape's pin location.</span></span>
  

