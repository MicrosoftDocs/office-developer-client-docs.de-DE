---
title: Zellenelement (Zeile EllipticalArcTo) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3c0aa7a3-cc54-ffac-2c62-917b3d0a357e
description: Enthält x- oder y-Koordinaten des Endpunkts eines elliptischen Bogens, x- oder y-Koordinaten des Steuerelements des Bogens, Winkel zwischen der x-Achse großen Achse der Ellipse oder das Verhältnis zwischen der Ellipse Haupt- und Hilfsintervalle Achsen verweist.
ms.openlocfilehash: 01d28fae5943251b61d0d26211ee91f09f25b9cc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796589"
---
# <a name="cell-element-ellipticalarcto-row-visio-xml"></a><span data-ttu-id="0f58b-103">Zellenelement (Zeile EllipticalArcTo) ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="0f58b-103">Cell element (EllipticalArcTo Row) ('Visio XML')</span></span>

<span data-ttu-id="0f58b-104">Enthält x- oder y-Koordinaten des Endpunkts eines elliptischen Bogens, x- oder y-Koordinaten des Steuerelements des Bogens, Winkel zwischen der x-Achse großen Achse der Ellipse oder das Verhältnis zwischen der Ellipse Haupt- und Hilfsintervalle Achsen verweist.</span><span class="sxs-lookup"><span data-stu-id="0f58b-104">Contains x- or y-coordinates of an elliptical arc's endpoint, x- or y-coordinates of the control points on the arc, angle from the x-axis to the ellipse's major axis, or ratio between the ellipse's major and minor axes.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0f58b-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="0f58b-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0f58b-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="0f58b-106">**Element type**</span></span> <br/> |[<span data-ttu-id="0f58b-107">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="0f58b-107">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="0f58b-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="0f58b-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="0f58b-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="0f58b-109">**Schema file**</span></span> <br/> |<span data-ttu-id="0f58b-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="0f58b-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="0f58b-111">**Dokumentbausteine**</span><span class="sxs-lookup"><span data-stu-id="0f58b-111">**Document parts**</span></span> <br/> |<span data-ttu-id="0f58b-112"># .xml Master, Seite # .xml</span><span class="sxs-lookup"><span data-stu-id="0f58b-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="0f58b-113">Definition</span><span class="sxs-lookup"><span data-stu-id="0f58b-113">Definition</span></span>

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="0f58b-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="0f58b-114">Elements and attributes</span></span>

<span data-ttu-id="0f58b-115">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="0f58b-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="0f58b-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0f58b-116">Parent elements</span></span>

|<span data-ttu-id="0f58b-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="0f58b-117">**Element**</span></span>|<span data-ttu-id="0f58b-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="0f58b-118">**Type**</span></span>|<span data-ttu-id="0f58b-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0f58b-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="0f58b-120">Row-Element ("Geometry")</span><span class="sxs-lookup"><span data-stu-id="0f58b-120">Row element (Geometry)</span></span>](row-element-geometry-sectionvisio-xml.md) <br/> |[<span data-ttu-id="0f58b-121">EllipticalArcTo_Type</span><span class="sxs-lookup"><span data-stu-id="0f58b-121">EllipticalArcTo_Type</span></span>](ellipticalarcto_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="0f58b-122">Enthält x- oder y-Koordinaten des Endpunkts eines elliptischen Bogens, x- oder y-Koordinaten des Steuerelements des Bogens, Winkel zwischen der x-Achse großen Achse der Ellipse oder das Verhältnis zwischen der Ellipse Haupt- und Hilfsintervalle Achsen verweist.</span><span class="sxs-lookup"><span data-stu-id="0f58b-122">Contains x- or y-coordinates of an elliptical arc's endpoint, x- or y-coordinates of the control points on the arc, angle from the x-axis to the ellipse's major axis, or ratio between the ellipse's major and minor axes.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="0f58b-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0f58b-123">Child elements</span></span>

|<span data-ttu-id="0f58b-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="0f58b-124">**Element**</span></span>|<span data-ttu-id="0f58b-125">**Typ**</span><span class="sxs-lookup"><span data-stu-id="0f58b-125">**Type**</span></span>|<span data-ttu-id="0f58b-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0f58b-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="0f58b-127">RefBy</span><span class="sxs-lookup"><span data-stu-id="0f58b-127">RefBy</span></span>](refby-element-cell_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="0f58b-128">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="0f58b-128">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="0f58b-129">Gibt einen Verweis auf ein Zeichenblatt.</span><span class="sxs-lookup"><span data-stu-id="0f58b-129">Specifies a reference to a drawing page.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="0f58b-130">Attribute</span><span class="sxs-lookup"><span data-stu-id="0f58b-130">Attributes</span></span>

|<span data-ttu-id="0f58b-131">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="0f58b-131">**Attribute**</span></span>|<span data-ttu-id="0f58b-132">**Typ**</span><span class="sxs-lookup"><span data-stu-id="0f58b-132">**Type**</span></span>|<span data-ttu-id="0f58b-133">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="0f58b-133">**Required**</span></span>|<span data-ttu-id="0f58b-134">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0f58b-134">**Description**</span></span>|<span data-ttu-id="0f58b-135">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="0f58b-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="0f58b-136">E</span><span class="sxs-lookup"><span data-stu-id="0f58b-136">E</span></span>  <br/> |<span data-ttu-id="0f58b-137">XSD: String</span><span class="sxs-lookup"><span data-stu-id="0f58b-137">xsd:string</span></span>  <br/> |<span data-ttu-id="0f58b-138">Optional</span><span class="sxs-lookup"><span data-stu-id="0f58b-138">optional</span></span>  <br/> |<span data-ttu-id="0f58b-139">Gibt an, dass die Formel einen Fehler zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="0f58b-139">Indicates that the formula evaluates to an error.</span></span> <span data-ttu-id="0f58b-140">Der Wert von **E** ist der aktuelle Wert (Zeichenfolge mit einer Fehlermeldung); der Wert des Attributs **V** ist der letzte gültige Wert.</span><span class="sxs-lookup"><span data-stu-id="0f58b-140">The value of **E** is the current value (an error message string); the value of the **V** attribute is the last valid value.</span></span>  <br/> |<span data-ttu-id="0f58b-141">Zeichenfolge mit einer Fehlermeldung.</span><span class="sxs-lookup"><span data-stu-id="0f58b-141">An error message string.</span></span>  <br/> |
|<span data-ttu-id="0f58b-142">F</span><span class="sxs-lookup"><span data-stu-id="0f58b-142">F</span></span>  <br/> |<span data-ttu-id="0f58b-143">XSD: String</span><span class="sxs-lookup"><span data-stu-id="0f58b-143">xsd:string</span></span>  <br/> |<span data-ttu-id="0f58b-144">Optional</span><span class="sxs-lookup"><span data-stu-id="0f58b-144">optional</span></span>  <br/> | <span data-ttu-id="0f58b-145">Formel für das Element darstellt.</span><span class="sxs-lookup"><span data-stu-id="0f58b-145">Represents the element's formula.</span></span> <span data-ttu-id="0f58b-146">Dieses Attribut kann eine der folgenden Zeichenfolgen enthalten:</span><span class="sxs-lookup"><span data-stu-id="0f58b-146">This attribute can contain one of the following strings:</span></span>  <br/>  <span data-ttu-id="0f58b-147">"(einige Formel)" Wenn die Formel lokal vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="0f58b-147">'(some formula)' if the formula exists locally</span></span>  <br/>  <span data-ttu-id="0f58b-148">`No Formula`Wenn die Formel lokal gelöscht oder blockiert ist.</span><span class="sxs-lookup"><span data-stu-id="0f58b-148">`No Formula` if the formula is locally deleted or blocked</span></span>  <br/>  <span data-ttu-id="0f58b-149">`Inh`Wenn die Formel geerbt wird.</span><span class="sxs-lookup"><span data-stu-id="0f58b-149">`Inh` if the formula is inherited.</span></span>  <br/> |<span data-ttu-id="0f58b-150">Eine Formel.</span><span class="sxs-lookup"><span data-stu-id="0f58b-150">A formula.</span></span>  <br/> |
|<span data-ttu-id="0f58b-151">N</span><span class="sxs-lookup"><span data-stu-id="0f58b-151">N</span></span>  <br/> |<span data-ttu-id="0f58b-152">XSD: String</span><span class="sxs-lookup"><span data-stu-id="0f58b-152">xsd:string</span></span>  <br/> |<span data-ttu-id="0f58b-153">erforderlich</span><span class="sxs-lookup"><span data-stu-id="0f58b-153">required</span></span>  <br/> |<span data-ttu-id="0f58b-154">Der Name der ShapeSheet-Zelle darstellt.</span><span class="sxs-lookup"><span data-stu-id="0f58b-154">Represents the name of the ShapeSheet cell.</span></span>  <br/> |<span data-ttu-id="0f58b-155">Der Name der ShapeSheet-Zelle.</span><span class="sxs-lookup"><span data-stu-id="0f58b-155">The name of the ShapeSheet cell.</span></span>  <br/> <span data-ttu-id="0f58b-156">Siehe Abschnitt "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="0f58b-156">See the Remarks section below.</span></span>  <br/> |
|<span data-ttu-id="0f58b-157">U</span><span class="sxs-lookup"><span data-stu-id="0f58b-157">U</span></span>  <br/> |<span data-ttu-id="0f58b-158">XSD: String</span><span class="sxs-lookup"><span data-stu-id="0f58b-158">xsd:string</span></span>  <br/> |<span data-ttu-id="0f58b-159">Optional</span><span class="sxs-lookup"><span data-stu-id="0f58b-159">optional</span></span>  <br/> |<span data-ttu-id="0f58b-160">Stellt eine Einheit der Messung der Standardwert ist DL.</span><span class="sxs-lookup"><span data-stu-id="0f58b-160">Represents a unit of measure The default is DL.</span></span>  <br/> |<span data-ttu-id="0f58b-161">Die Einheiten der Zelle.</span><span class="sxs-lookup"><span data-stu-id="0f58b-161">The units of the cell.</span></span>  <br/> |
|<span data-ttu-id="0f58b-162">V</span><span class="sxs-lookup"><span data-stu-id="0f58b-162">V</span></span>  <br/> |<span data-ttu-id="0f58b-163">XSD: String</span><span class="sxs-lookup"><span data-stu-id="0f58b-163">xsd:string</span></span>  <br/> |<span data-ttu-id="0f58b-164">Optional</span><span class="sxs-lookup"><span data-stu-id="0f58b-164">optional</span></span>  <br/> |<span data-ttu-id="0f58b-165">Den Wert der Zelle darstellt.</span><span class="sxs-lookup"><span data-stu-id="0f58b-165">Represents the value of the cell.</span></span>  <br/> |<span data-ttu-id="0f58b-166">Der Wert der ShapeSheet-Zelle.</span><span class="sxs-lookup"><span data-stu-id="0f58b-166">The value of the ShapeSheet cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0f58b-167">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0f58b-167">Remarks</span></span>

<span data-ttu-id="0f58b-168">Das **N** -Attribut dieses Elements **Zelle** muss eine der eine begrenzte Auswahl von Werten sein, die ShapeSheet-Zellen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="0f58b-168">The **N** attribute of this **Cell** element must be one of a limited set of values that correspond to ShapeSheet cells.</span></span> <span data-ttu-id="0f58b-169">Finden Sie in der Tabelle unten, um die Werte der **N** -Attribut zu bestimmen, die für diese **Zelle** Element zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="0f58b-169">Refer to the table below to determine the values of the **N** attribute that are permitted for this **Cell** element.</span></span> 
  
|<span data-ttu-id="0f58b-170">**Wert**</span><span class="sxs-lookup"><span data-stu-id="0f58b-170">**Value**</span></span>|<span data-ttu-id="0f58b-171">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0f58b-171">**Description**</span></span>|<span data-ttu-id="0f58b-172">**Weitere Informationen**</span><span class="sxs-lookup"><span data-stu-id="0f58b-172">**More information**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="0f58b-173">X</span><span class="sxs-lookup"><span data-stu-id="0f58b-173">X</span></span>  <br/> |<span data-ttu-id="0f58b-174">Die X-Koordinate des Endscheitelpunkts eines Bogens.</span><span class="sxs-lookup"><span data-stu-id="0f58b-174">The x-coordinate of the ending vertex on an arc.</span></span>  <br/> |[<span data-ttu-id="0f58b-175">Zeile "EllipticalArcTo" (Abschnitt "Geometry")</span><span class="sxs-lookup"><span data-stu-id="0f58b-175">EllipticalArcTo Row (Geometry Section)</span></span>](ellipticalarcto-row-geometry-section.md) <br/> |
|<span data-ttu-id="0f58b-176">v</span><span class="sxs-lookup"><span data-stu-id="0f58b-176">Y</span></span>  <br/> |<span data-ttu-id="0f58b-177">Die y-Koordinate des Endscheitelpunkts eines Bogens.</span><span class="sxs-lookup"><span data-stu-id="0f58b-177">The y-coordinate of the ending vertex on an arc.</span></span>  <br/> |[<span data-ttu-id="0f58b-178">Zeile "EllipticalArcTo" (Abschnitt "Geometry")</span><span class="sxs-lookup"><span data-stu-id="0f58b-178">EllipticalArcTo Row (Geometry Section)</span></span>](ellipticalarcto-row-geometry-section.md) <br/> |
|<span data-ttu-id="0f58b-179">A</span><span class="sxs-lookup"><span data-stu-id="0f58b-179">A</span></span>  <br/> |<span data-ttu-id="0f58b-180">Zeigen Sie die X-Koordinate des des Bogens. ein Punkt auf dem Bogen. Kontrollpunkts ist die beste in der Mitte zwischen dem ersten und letzten Scheitelpunkt des Bogens. Andernfalls kann Bogens extrem große anwachsen, um passieren Kontrollpunkts weitergibt.</span><span class="sxs-lookup"><span data-stu-id="0f58b-180">The x-coordinate of the arc's control point; a point on the arc. The control point is best located about halfway between the beginning and ending vertices of the arc. Otherwise, the arc may grow to an extreme size in order to pass through the control point, with unpredictable results.</span></span>  <br/> |[<span data-ttu-id="0f58b-181">Zeile "EllipticalArcTo" (Abschnitt "Geometry")</span><span class="sxs-lookup"><span data-stu-id="0f58b-181">EllipticalArcTo Row (Geometry Section)</span></span>](ellipticalarcto-row-geometry-section.md) <br/> |
|<span data-ttu-id="0f58b-182">B</span><span class="sxs-lookup"><span data-stu-id="0f58b-182">B</span></span>  <br/> |<span data-ttu-id="0f58b-183">Die y-Koordinate des Kontrollpunkts des Bogens.</span><span class="sxs-lookup"><span data-stu-id="0f58b-183">The y-coordinate of an arc's control point.</span></span>  <br/> |[<span data-ttu-id="0f58b-184">Zeile "EllipticalArcTo" (Abschnitt "Geometry")</span><span class="sxs-lookup"><span data-stu-id="0f58b-184">EllipticalArcTo Row (Geometry Section)</span></span>](ellipticalarcto-row-geometry-section.md) <br/> |
|<span data-ttu-id="0f58b-185">C</span><span class="sxs-lookup"><span data-stu-id="0f58b-185">C</span></span>  <br/> |<span data-ttu-id="0f58b-186">Der Winkel der Größenachse des Bogens relativ zur x-Achse der das übergeordnete Shape.</span><span class="sxs-lookup"><span data-stu-id="0f58b-186">The angle of an arc's major axis relative to the x-axis of its parent shape.</span></span>  <br/> |[<span data-ttu-id="0f58b-187">Zeile "EllipticalArcTo" (Abschnitt "Geometry")</span><span class="sxs-lookup"><span data-stu-id="0f58b-187">EllipticalArcTo Row (Geometry Section)</span></span>](ellipticalarcto-row-geometry-section.md) <br/> |
|<span data-ttu-id="0f58b-188">D</span><span class="sxs-lookup"><span data-stu-id="0f58b-188">D</span></span>  <br/> |<span data-ttu-id="0f58b-p104">Das Verhältnis der größeren zur kleineren Achse eines Bogens. Im Gegensatz zu der normalen Bedeutung der Bezeichnungen muss die als "große" Achse bezeichnete Achse nicht unbedingt größer als die "kleine" Achse sein, sodass das Größenverhältnis nicht größer als 1 sein muss. Beim Festlegen des Zellwerts gleich 0 bzw. größer als 1000 können unvorhergesehene Ergebnisse auftreten.</span><span class="sxs-lookup"><span data-stu-id="0f58b-p104">The ratio of an arc's major axis to its minor axis. Despite the usual meaning of these words, the "major" axis does not have to be greater than the "minor" axis, so this ratio does not have to be greater than 1. Setting this cell to a value less than or equal to 0 or greater than 1000 can lead to unpredictable results.</span></span>  <br/> |[<span data-ttu-id="0f58b-192">Zeile "EllipticalArcTo" (Abschnitt "Geometry")</span><span class="sxs-lookup"><span data-stu-id="0f58b-192">EllipticalArcTo Row (Geometry Section)</span></span>](ellipticalarcto-row-geometry-section.md) <br/> |
   
