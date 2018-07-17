---
title: Zellenelement (Aktionstag Abschnitt) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6210ff71-fbcd-2c97-6dde-1e334891e08d
description: Eine Eigenschaft für ein Aktionstag definiert auf ein Shape oder Zeichenblatt.
ms.openlocfilehash: 0945235c49e77210564e50e5c111579ab37f3e31
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796559"
---
# <a name="cell-element-action-tag-section-visio-xml"></a><span data-ttu-id="bea63-103">Zellenelement (Aktionstag Abschnitt) ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="bea63-103">Cell element (Action Tag Section) ('Visio XML')</span></span>

<span data-ttu-id="bea63-104">Eine Eigenschaft für ein Aktionstag definiert auf ein Shape oder Zeichenblatt.</span><span class="sxs-lookup"><span data-stu-id="bea63-104">Defines one property for an action tag on a shape or page.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="bea63-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="bea63-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bea63-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="bea63-106">**Element type**</span></span> <br/> |[<span data-ttu-id="bea63-107">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="bea63-107">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="bea63-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="bea63-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="bea63-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="bea63-109">**Schema file**</span></span> <br/> |<span data-ttu-id="bea63-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="bea63-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="bea63-111">**Dokumentbausteine**</span><span class="sxs-lookup"><span data-stu-id="bea63-111">**Document parts**</span></span> <br/> |<span data-ttu-id="bea63-112">Masters.XML, Master-Shape # .xml, pages.xml, Seite # .xml</span><span class="sxs-lookup"><span data-stu-id="bea63-112">masters.xml, master#.xml, pages.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="bea63-113">Definition</span><span class="sxs-lookup"><span data-stu-id="bea63-113">Definition</span></span>

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="bea63-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="bea63-114">Elements and attributes</span></span>

<span data-ttu-id="bea63-115">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="bea63-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="bea63-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="bea63-116">Parent elements</span></span>

|<span data-ttu-id="bea63-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="bea63-117">**Element**</span></span>|<span data-ttu-id="bea63-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="bea63-118">**Type**</span></span>|<span data-ttu-id="bea63-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="bea63-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="bea63-120">Row-Element (ActionTag Abschnitt)</span><span class="sxs-lookup"><span data-stu-id="bea63-120">Row element (ActionTag Section)</span></span>](row-element-action-tag-sectionvisio-xml.md) <br/> |[<span data-ttu-id="bea63-121">ActionTagRow_Type</span><span class="sxs-lookup"><span data-stu-id="bea63-121">ActionTagRow_Type</span></span>](actiontag_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="bea63-122">Ein Shape oder Zeichenblatt definiert ein Aktionstag.</span><span class="sxs-lookup"><span data-stu-id="bea63-122">Defines an action tag on a shape or page.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="bea63-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="bea63-123">Child elements</span></span>

|<span data-ttu-id="bea63-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="bea63-124">**Element**</span></span>|<span data-ttu-id="bea63-125">**Typ**</span><span class="sxs-lookup"><span data-stu-id="bea63-125">**Type**</span></span>|<span data-ttu-id="bea63-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="bea63-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="bea63-127">RefBy</span><span class="sxs-lookup"><span data-stu-id="bea63-127">RefBy</span></span>](refby-element-cell_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="bea63-128">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="bea63-128">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="bea63-129">Gibt einen Verweis auf ein Zeichenblatt.</span><span class="sxs-lookup"><span data-stu-id="bea63-129">Specifies a reference to a drawing page.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="bea63-130">Attribute</span><span class="sxs-lookup"><span data-stu-id="bea63-130">Attributes</span></span>

|<span data-ttu-id="bea63-131">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="bea63-131">**Attribute**</span></span>|<span data-ttu-id="bea63-132">**Typ**</span><span class="sxs-lookup"><span data-stu-id="bea63-132">**Type**</span></span>|<span data-ttu-id="bea63-133">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="bea63-133">**Required**</span></span>|<span data-ttu-id="bea63-134">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="bea63-134">**Description**</span></span>|<span data-ttu-id="bea63-135">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="bea63-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="bea63-136">E</span><span class="sxs-lookup"><span data-stu-id="bea63-136">E</span></span>  <br/> |<span data-ttu-id="bea63-137">XSD: String</span><span class="sxs-lookup"><span data-stu-id="bea63-137">xsd:string</span></span>  <br/> |<span data-ttu-id="bea63-138">Optional</span><span class="sxs-lookup"><span data-stu-id="bea63-138">optional</span></span>  <br/> |<span data-ttu-id="bea63-139">Gibt an, dass die Formel einen Fehler zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="bea63-139">Indicates that the formula evaluates to an error.</span></span> <span data-ttu-id="bea63-140">Der Wert von **E** ist der aktuelle Wert (Zeichenfolge mit einer Fehlermeldung); der Wert des Attributs **V** ist der letzte gültige Wert.</span><span class="sxs-lookup"><span data-stu-id="bea63-140">The value of **E** is the current value (an error message string); the value of the **V** attribute is the last valid value.</span></span>  <br/> |<span data-ttu-id="bea63-141">Zeichenfolge mit einer Fehlermeldung.</span><span class="sxs-lookup"><span data-stu-id="bea63-141">An error message string.</span></span>  <br/> |
|<span data-ttu-id="bea63-142">F</span><span class="sxs-lookup"><span data-stu-id="bea63-142">F</span></span>  <br/> |<span data-ttu-id="bea63-143">XSD: String</span><span class="sxs-lookup"><span data-stu-id="bea63-143">xsd:string</span></span>  <br/> |<span data-ttu-id="bea63-144">Optional</span><span class="sxs-lookup"><span data-stu-id="bea63-144">optional</span></span>  <br/> | <span data-ttu-id="bea63-145">Formel für das Element darstellt.</span><span class="sxs-lookup"><span data-stu-id="bea63-145">Represents the element's formula.</span></span> <span data-ttu-id="bea63-146">Dieses Attribut kann eine der folgenden Zeichenfolgen enthalten:</span><span class="sxs-lookup"><span data-stu-id="bea63-146">This attribute can contain one of the following strings:</span></span>  <br/>  <span data-ttu-id="bea63-147">"(einige Formel)" Wenn die Formel lokal vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="bea63-147">'(some formula)' if the formula exists locally</span></span>  <br/>  <span data-ttu-id="bea63-148">`No Formula`Wenn die Formel lokal gelöscht oder blockiert ist.</span><span class="sxs-lookup"><span data-stu-id="bea63-148">`No Formula` if the formula is locally deleted or blocked</span></span>  <br/>  <span data-ttu-id="bea63-149">`Inh`Wenn die Formel geerbt wird.</span><span class="sxs-lookup"><span data-stu-id="bea63-149">`Inh` if the formula is inherited.</span></span>  <br/> |<span data-ttu-id="bea63-150">Eine Formel.</span><span class="sxs-lookup"><span data-stu-id="bea63-150">A formula.</span></span>  <br/> |
|<span data-ttu-id="bea63-151">N</span><span class="sxs-lookup"><span data-stu-id="bea63-151">N</span></span>  <br/> |<span data-ttu-id="bea63-152">XSD: String</span><span class="sxs-lookup"><span data-stu-id="bea63-152">xsd:string</span></span>  <br/> |<span data-ttu-id="bea63-153">erforderlich</span><span class="sxs-lookup"><span data-stu-id="bea63-153">required</span></span>  <br/> |<span data-ttu-id="bea63-154">Der Name der ShapeSheet-Zelle darstellt.</span><span class="sxs-lookup"><span data-stu-id="bea63-154">Represents the name of the ShapeSheet cell.</span></span>  <br/> |<span data-ttu-id="bea63-155">Der Name der ShapeSheet-Zelle.</span><span class="sxs-lookup"><span data-stu-id="bea63-155">The name of the ShapeSheet cell.</span></span>  <br/> <span data-ttu-id="bea63-156">Siehe Abschnitt "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="bea63-156">See the Remarks section below.</span></span>  <br/> |
|<span data-ttu-id="bea63-157">U</span><span class="sxs-lookup"><span data-stu-id="bea63-157">U</span></span>  <br/> |<span data-ttu-id="bea63-158">XSD: String</span><span class="sxs-lookup"><span data-stu-id="bea63-158">xsd:string</span></span>  <br/> |<span data-ttu-id="bea63-159">Optional</span><span class="sxs-lookup"><span data-stu-id="bea63-159">optional</span></span>  <br/> |<span data-ttu-id="bea63-160">Stellt eine Einheit der Messung der Standardwert ist DL.</span><span class="sxs-lookup"><span data-stu-id="bea63-160">Represents a unit of measure The default is DL.</span></span>  <br/> |<span data-ttu-id="bea63-161">Die Einheiten der Zelle.</span><span class="sxs-lookup"><span data-stu-id="bea63-161">The units of the cell.</span></span>  <br/> |
|<span data-ttu-id="bea63-162">V</span><span class="sxs-lookup"><span data-stu-id="bea63-162">V</span></span>  <br/> |<span data-ttu-id="bea63-163">XSD: String</span><span class="sxs-lookup"><span data-stu-id="bea63-163">xsd:string</span></span>  <br/> |<span data-ttu-id="bea63-164">Optional</span><span class="sxs-lookup"><span data-stu-id="bea63-164">optional</span></span>  <br/> |<span data-ttu-id="bea63-165">Den Wert der Zelle darstellt.</span><span class="sxs-lookup"><span data-stu-id="bea63-165">Represents the value of the cell.</span></span>  <br/> |<span data-ttu-id="bea63-166">Der Wert der ShapeSheet-Zelle.</span><span class="sxs-lookup"><span data-stu-id="bea63-166">The value of the ShapeSheet cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bea63-167">Hinweise</span><span class="sxs-lookup"><span data-stu-id="bea63-167">Remarks</span></span>

<span data-ttu-id="bea63-168">Das **N** -Attribut dieses Elements **Zelle** muss eine der eine begrenzte Auswahl von Werten sein, die ShapeSheet-Zellen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="bea63-168">The **N** attribute of this **Cell** element must be one of a limited set of values that correspond to ShapeSheet cells.</span></span> <span data-ttu-id="bea63-169">Finden Sie in der Tabelle unten, um die Werte der **N** -Attribut zu bestimmen, die für diese **Zelle** Element zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="bea63-169">Refer to the table below to determine the values of the **N** attribute that are permitted for this **Cell** element.</span></span> 
  
|<span data-ttu-id="bea63-170">**Wert**</span><span class="sxs-lookup"><span data-stu-id="bea63-170">**Value**</span></span>|<span data-ttu-id="bea63-171">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="bea63-171">**Description**</span></span>|<span data-ttu-id="bea63-172">**Weitere Informationen**</span><span class="sxs-lookup"><span data-stu-id="bea63-172">**More information**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="bea63-173">ButtonFace</span><span class="sxs-lookup"><span data-stu-id="bea63-173">ButtonFace</span></span>  <br/> |<span data-ttu-id="bea63-174">Enthält die ID der Schaltflächenoberseite, die auf der Schaltfläche Aktionstag angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="bea63-174">Contains the ID of the button face image that appears on the action tag button.</span></span>  <br/> |[<span data-ttu-id="bea63-175">Zelle "ButtonFace" (Abschnitt "Action Tags")</span><span class="sxs-lookup"><span data-stu-id="bea63-175">ButtonFace Cell (Action Tags Section)</span></span>](buttonface-cell-action-tags-section.md) <br/> |
|<span data-ttu-id="bea63-176">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bea63-176">Description</span></span>  <br/> |<span data-ttu-id="bea63-177">Enthält eine Zeichenfolge als Beschreibung des Aktionstags, die als QuickInfo angezeigt wird, wenn der Zeiger über dem Tag platziert wird.</span><span class="sxs-lookup"><span data-stu-id="bea63-177">Contains a string that describes the action tag, which appears as a tool tip when users place their pointer over the tag.</span></span>  <br/> |[<span data-ttu-id="bea63-178">Zelle "Description" (Abschnitt "Action Tags")</span><span class="sxs-lookup"><span data-stu-id="bea63-178">Description Cell (Action Tags Section)</span></span>](description-cell-action-tags-section.md) <br/> |
|<span data-ttu-id="bea63-179">Deaktiviert</span><span class="sxs-lookup"><span data-stu-id="bea63-179">Disabled</span></span>  <br/> |<span data-ttu-id="bea63-180">Gibt an, ob das Aktionstag im Zeichnungsfenster angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="bea63-180">Indicates whether the action tag appears in the drawing window.</span></span>  <br/> |[<span data-ttu-id="bea63-181">Zelle "Disabled" (Abschnitt "Action Tags")</span><span class="sxs-lookup"><span data-stu-id="bea63-181">Disabled Cell (Action Tags Section)</span></span>](disabled-cell-action-tags-section.md) <br/> |
|<span data-ttu-id="bea63-182">DisplayMode</span><span class="sxs-lookup"><span data-stu-id="bea63-182">DisplayMode</span></span>  <br/> |<span data-ttu-id="bea63-183">Bestimmt, ob das Aktionstag angezeigt wird, wenn der Zeiger über das Tag bewegt wird, wenn das Shape ausgewählt ist oder immer.</span><span class="sxs-lookup"><span data-stu-id="bea63-183">Determines whether the action tag appears when the user moves the pointer over the tag, when the shape is selected, or all the time.</span></span>  <br/> |[<span data-ttu-id="bea63-184">DisplayMode Zelle (Abschnitt "Action Tags")</span><span class="sxs-lookup"><span data-stu-id="bea63-184">DisplayMode Cell (Action Tags Section)</span></span>](displaymode-cell-action-tags-section.md) <br/> |
|<span data-ttu-id="bea63-185">TagName</span><span class="sxs-lookup"><span data-stu-id="bea63-185">TagName</span></span>  <br/> |<span data-ttu-id="bea63-186">Der Name des Aktionstags, das als Schlüssel verwendet wird, um das Aktionstag seinen Aktionen zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="bea63-186">Name of the action tag that is used as a key to associate the action tag with its actions.</span></span>  <br/> |[<span data-ttu-id="bea63-187">Zelle "TagName" (Abschnitt "Action Tags")</span><span class="sxs-lookup"><span data-stu-id="bea63-187">TagName Cell (Action Tags Section)</span></span>](tagname-cell-action-tags-section.md) <br/> |
|<span data-ttu-id="bea63-188">X</span><span class="sxs-lookup"><span data-stu-id="bea63-188">X</span></span>  <br/> |<span data-ttu-id="bea63-189">Die X-Koordinate in lokalen Koordinaten des Shapes, um die herum die Schaltfläche Aktionstag, platziert wird.</span><span class="sxs-lookup"><span data-stu-id="bea63-189">The x-coordinate position in the shape's local coordinates around which the action tag button is placed.</span></span>  <br/> |[<span data-ttu-id="bea63-190">Zelle "X" (Abschnitt "Action Tags")</span><span class="sxs-lookup"><span data-stu-id="bea63-190">X Cell (Action Tags Section)</span></span>](x-cell-action-tags-section.md) <br/> |
|<span data-ttu-id="bea63-191">XJustify</span><span class="sxs-lookup"><span data-stu-id="bea63-191">XJustify</span></span>  <br/> |<span data-ttu-id="bea63-192">Die X-Abstand der Schaltfläche Aktionstag in Bezug auf den Punkt, der durch die Zellen X und Y definiert ist.</span><span class="sxs-lookup"><span data-stu-id="bea63-192">The x-offset of the action tag button relative to the point defined by the X and Y cells.</span></span>  <br/> |[<span data-ttu-id="bea63-193">Zelle "X Justify" (Abschnitt "Action Tags")</span><span class="sxs-lookup"><span data-stu-id="bea63-193">X Justify Cell (Action Tags Section)</span></span>](x-justify-cell-action-tags-section.md) <br/> |
|<span data-ttu-id="bea63-194">v</span><span class="sxs-lookup"><span data-stu-id="bea63-194">Y</span></span>  <br/> |<span data-ttu-id="bea63-195">Die y-Koordinate in lokalen Koordinaten des Shapes, um die herum die Schaltfläche Aktionstag, platziert wird.</span><span class="sxs-lookup"><span data-stu-id="bea63-195">The y-coordinate position in the shape's local coordinates around which the action tag button is placed.</span></span>  <br/> |[<span data-ttu-id="bea63-196">Zelle "Y" (Abschnitt "Action Tags")</span><span class="sxs-lookup"><span data-stu-id="bea63-196">Y Cell (Action Tags Section)</span></span>](y-cell-action-tags-section.md) <br/> |
|<span data-ttu-id="bea63-197">YJustify</span><span class="sxs-lookup"><span data-stu-id="bea63-197">YJustify</span></span>  <br/> |<span data-ttu-id="bea63-198">Die y-Abstand der Schaltfläche Aktionstag in Bezug auf den Punkt, der durch die Zellen X und Y definiert ist.</span><span class="sxs-lookup"><span data-stu-id="bea63-198">The y-offset of the action tag button relative to the point defined by the X and Y cells.</span></span>  <br/> |[<span data-ttu-id="bea63-199">Zelle "Y Justify" (Abschnitt "Action Tags")</span><span class="sxs-lookup"><span data-stu-id="bea63-199">Y Justify Cell (Action Tags Section)</span></span>](y-justify-cell-action-tags-section.md) <br/> |
   
