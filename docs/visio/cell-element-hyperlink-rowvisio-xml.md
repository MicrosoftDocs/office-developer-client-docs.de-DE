---
title: Zellenelement (Hyperlinkzeile) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d2089db4-39eb-06d3-d2f8-9465baef5c75
description: Enthält die Informationen für einen einzelnen Hyperlink, der einem Shape zugeordnet ist. Ein Shape enthält für jeden Hyperlink eine Hyperlink-Zeile.
ms.openlocfilehash: b664f5e0ac7cfe27b7198dd59b1b8be1af276db7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796584"
---
# <a name="cell-element-hyperlink-row-visio-xml"></a><span data-ttu-id="59e26-104">Zellenelement (Hyperlinkzeile) ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="59e26-104">Cell element (Hyperlink Row) ('Visio XML')</span></span>

<span data-ttu-id="59e26-105">Enthält die Informationen für einen einzelnen Hyperlink, der mit einer Form verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="59e26-105">Contains the information for a single hyperlink associated with a shape.</span></span> <span data-ttu-id="59e26-106">Ein Shape enthält **eine Zeile für jeden Hyperlink** .</span><span class="sxs-lookup"><span data-stu-id="59e26-106">A shape will contain one **Hyperlink** row for each hyperlink.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="59e26-107">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="59e26-107">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="59e26-108">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="59e26-108">**Element type**</span></span> <br/> |[<span data-ttu-id="59e26-109">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="59e26-109">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="59e26-110">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="59e26-110">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="59e26-111">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="59e26-111">**Schema file**</span></span> <br/> |<span data-ttu-id="59e26-112">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="59e26-112">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="59e26-113">**Dokumentbausteine**</span><span class="sxs-lookup"><span data-stu-id="59e26-113">**Document parts**</span></span> <br/> |<span data-ttu-id="59e26-114"># .xml Master, Seite # .xml</span><span class="sxs-lookup"><span data-stu-id="59e26-114">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="59e26-115">Definition</span><span class="sxs-lookup"><span data-stu-id="59e26-115">Definition</span></span>

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="59e26-116">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="59e26-116">Elements and attributes</span></span>

<span data-ttu-id="59e26-117">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="59e26-117">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="59e26-118">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="59e26-118">Parent elements</span></span>

|<span data-ttu-id="59e26-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="59e26-119">**Element**</span></span>|<span data-ttu-id="59e26-120">**Typ**</span><span class="sxs-lookup"><span data-stu-id="59e26-120">**Type**</span></span>|<span data-ttu-id="59e26-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="59e26-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="59e26-122">Row-Element (Abschnitt "Hyperlinks")</span><span class="sxs-lookup"><span data-stu-id="59e26-122">Row element (Hyperlink Section)</span></span>](row-element-hyperlink-sectionvisio-xml.md) <br/> |[<span data-ttu-id="59e26-123">HyperlinkRow_Type</span><span class="sxs-lookup"><span data-stu-id="59e26-123">HyperlinkRow_Type</span></span>](hyperlinkrow_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="59e26-124">Enthält die Informationen für einen einzelnen Hyperlink, der mit einer Form verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="59e26-124">Contains the information for a single hyperlink associated with a shape.</span></span> <span data-ttu-id="59e26-125">Ein Shape enthält **eine Zeile für jeden Hyperlink** .</span><span class="sxs-lookup"><span data-stu-id="59e26-125">A shape will contain one **Hyperlink** row for each hyperlink.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="59e26-126">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="59e26-126">Child elements</span></span>

|<span data-ttu-id="59e26-127">**Element**</span><span class="sxs-lookup"><span data-stu-id="59e26-127">**Element**</span></span>|<span data-ttu-id="59e26-128">**Typ**</span><span class="sxs-lookup"><span data-stu-id="59e26-128">**Type**</span></span>|<span data-ttu-id="59e26-129">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="59e26-129">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="59e26-130">RefBy</span><span class="sxs-lookup"><span data-stu-id="59e26-130">RefBy</span></span>](refby-element-cell_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="59e26-131">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="59e26-131">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="59e26-132">Gibt einen Verweis auf ein Zeichenblatt.</span><span class="sxs-lookup"><span data-stu-id="59e26-132">Specifies a reference to a drawing page.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="59e26-133">Attribute</span><span class="sxs-lookup"><span data-stu-id="59e26-133">Attributes</span></span>

|<span data-ttu-id="59e26-134">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="59e26-134">**Attribute**</span></span>|<span data-ttu-id="59e26-135">**Typ**</span><span class="sxs-lookup"><span data-stu-id="59e26-135">**Type**</span></span>|<span data-ttu-id="59e26-136">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="59e26-136">**Required**</span></span>|<span data-ttu-id="59e26-137">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="59e26-137">**Description**</span></span>|<span data-ttu-id="59e26-138">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="59e26-138">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="59e26-139">E</span><span class="sxs-lookup"><span data-stu-id="59e26-139">E</span></span>  <br/> |<span data-ttu-id="59e26-140">XSD: String</span><span class="sxs-lookup"><span data-stu-id="59e26-140">xsd:string</span></span>  <br/> |<span data-ttu-id="59e26-141">Optional</span><span class="sxs-lookup"><span data-stu-id="59e26-141">optional</span></span>  <br/> |<span data-ttu-id="59e26-142">Gibt an, dass die Formel einen Fehler zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="59e26-142">Indicates that the formula evaluates to an error.</span></span> <span data-ttu-id="59e26-143">Der Wert von **E** ist der aktuelle Wert (Zeichenfolge mit einer Fehlermeldung); der Wert des Attributs **V** ist der letzte gültige Wert.</span><span class="sxs-lookup"><span data-stu-id="59e26-143">The value of **E** is the current value (an error message string); the value of the **V** attribute is the last valid value.</span></span>  <br/> |<span data-ttu-id="59e26-144">Zeichenfolge mit einer Fehlermeldung.</span><span class="sxs-lookup"><span data-stu-id="59e26-144">An error message string.</span></span>  <br/> |
|<span data-ttu-id="59e26-145">F</span><span class="sxs-lookup"><span data-stu-id="59e26-145">F</span></span>  <br/> |<span data-ttu-id="59e26-146">XSD: String</span><span class="sxs-lookup"><span data-stu-id="59e26-146">xsd:string</span></span>  <br/> |<span data-ttu-id="59e26-147">Optional</span><span class="sxs-lookup"><span data-stu-id="59e26-147">optional</span></span>  <br/> | <span data-ttu-id="59e26-148">Formel für das Element darstellt.</span><span class="sxs-lookup"><span data-stu-id="59e26-148">Represents the element's formula.</span></span> <span data-ttu-id="59e26-149">Dieses Attribut kann eine der folgenden Zeichenfolgen enthalten:</span><span class="sxs-lookup"><span data-stu-id="59e26-149">This attribute can contain one of the following strings:</span></span>  <br/>  <span data-ttu-id="59e26-150">"(einige Formel)" Wenn die Formel lokal vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="59e26-150">'(some formula)' if the formula exists locally</span></span>  <br/>  <span data-ttu-id="59e26-151">`No Formula`Wenn die Formel lokal gelöscht oder blockiert ist.</span><span class="sxs-lookup"><span data-stu-id="59e26-151">`No Formula` if the formula is locally deleted or blocked</span></span>  <br/>  <span data-ttu-id="59e26-152">`Inh`Wenn die Formel geerbt wird.</span><span class="sxs-lookup"><span data-stu-id="59e26-152">`Inh` if the formula is inherited.</span></span>  <br/> |<span data-ttu-id="59e26-153">Eine Formel.</span><span class="sxs-lookup"><span data-stu-id="59e26-153">A formula.</span></span>  <br/> |
|<span data-ttu-id="59e26-154">N</span><span class="sxs-lookup"><span data-stu-id="59e26-154">N</span></span>  <br/> |<span data-ttu-id="59e26-155">XSD: String</span><span class="sxs-lookup"><span data-stu-id="59e26-155">xsd:string</span></span>  <br/> |<span data-ttu-id="59e26-156">erforderlich</span><span class="sxs-lookup"><span data-stu-id="59e26-156">required</span></span>  <br/> |<span data-ttu-id="59e26-157">Der Name der ShapeSheet-Zelle darstellt.</span><span class="sxs-lookup"><span data-stu-id="59e26-157">Represents the name of the ShapeSheet cell.</span></span>  <br/> |<span data-ttu-id="59e26-158">Der Name der ShapeSheet-Zelle.</span><span class="sxs-lookup"><span data-stu-id="59e26-158">The name of the ShapeSheet cell.</span></span>  <br/> <span data-ttu-id="59e26-159">Siehe Abschnitt "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="59e26-159">See the Remarks section below.</span></span>  <br/> |
|<span data-ttu-id="59e26-160">U</span><span class="sxs-lookup"><span data-stu-id="59e26-160">U</span></span>  <br/> |<span data-ttu-id="59e26-161">XSD: String</span><span class="sxs-lookup"><span data-stu-id="59e26-161">xsd:string</span></span>  <br/> |<span data-ttu-id="59e26-162">Optional</span><span class="sxs-lookup"><span data-stu-id="59e26-162">optional</span></span>  <br/> |<span data-ttu-id="59e26-163">Stellt eine Einheit der Messung der Standardwert ist DL.</span><span class="sxs-lookup"><span data-stu-id="59e26-163">Represents a unit of measure The default is DL.</span></span>  <br/> |<span data-ttu-id="59e26-164">Die Einheiten der Zelle.</span><span class="sxs-lookup"><span data-stu-id="59e26-164">The units of the cell.</span></span>  <br/> |
|<span data-ttu-id="59e26-165">V</span><span class="sxs-lookup"><span data-stu-id="59e26-165">V</span></span>  <br/> |<span data-ttu-id="59e26-166">XSD: String</span><span class="sxs-lookup"><span data-stu-id="59e26-166">xsd:string</span></span>  <br/> |<span data-ttu-id="59e26-167">Optional</span><span class="sxs-lookup"><span data-stu-id="59e26-167">optional</span></span>  <br/> |<span data-ttu-id="59e26-168">Den Wert der Zelle darstellt.</span><span class="sxs-lookup"><span data-stu-id="59e26-168">Represents the value of the cell.</span></span>  <br/> |<span data-ttu-id="59e26-169">Der Wert der ShapeSheet-Zelle.</span><span class="sxs-lookup"><span data-stu-id="59e26-169">The value of the ShapeSheet cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="59e26-170">Hinweise</span><span class="sxs-lookup"><span data-stu-id="59e26-170">Remarks</span></span>

<span data-ttu-id="59e26-171">Das **N** -Attribut dieses Elements **Zelle** muss eine der eine begrenzte Auswahl von Werten sein, die ShapeSheet-Zellen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="59e26-171">The **N** attribute of this **Cell** element must be one of a limited set of values that correspond to ShapeSheet cells.</span></span> <span data-ttu-id="59e26-172">Finden Sie in der Tabelle unten, um die Werte der **N** -Attribut zu bestimmen, die für diese **Zelle** Element zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="59e26-172">Refer to the table below to determine the values of the **N** attribute that are permitted for this **Cell** element.</span></span> 
  
|<span data-ttu-id="59e26-173">**Wert**</span><span class="sxs-lookup"><span data-stu-id="59e26-173">**Value**</span></span>|<span data-ttu-id="59e26-174">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="59e26-174">**Description**</span></span>|<span data-ttu-id="59e26-175">**Weitere Informationen**</span><span class="sxs-lookup"><span data-stu-id="59e26-175">**More information**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="59e26-176">Adresse</span><span class="sxs-lookup"><span data-stu-id="59e26-176">Address</span></span>  <br/> |<span data-ttu-id="59e26-177">Legt eine aufzurufende URL-Adresse, einen Dateinamen oder einen UNC-Pfad fest.</span><span class="sxs-lookup"><span data-stu-id="59e26-177">Specifies a URL address, file name, or UNC path to which to jump.</span></span>  <br/> |[<span data-ttu-id="59e26-178">Zelle "Address" (Abschnitt "Hyperlinks")</span><span class="sxs-lookup"><span data-stu-id="59e26-178">Address Cell (Hyperlinks Section)</span></span>](address-cell-hyperlinks-section.md) <br/> |
|<span data-ttu-id="59e26-179">Standard</span><span class="sxs-lookup"><span data-stu-id="59e26-179">Default</span></span>  <br/> |<span data-ttu-id="59e26-180">Legt den Standardhyperlink für ein Shape oder Zeichenblatt.</span><span class="sxs-lookup"><span data-stu-id="59e26-180">Determines the default hyperlink for a shape or page.</span></span>  <br/> |[<span data-ttu-id="59e26-181">Zelle "Default" (Abschnitt "Hyperlinks")</span><span class="sxs-lookup"><span data-stu-id="59e26-181">Default Cell (Hyperlinks Section)</span></span>](default-cell-hyperlinks-section.md) <br/> |
|<span data-ttu-id="59e26-182">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="59e26-182">Description</span></span>  <br/> |<span data-ttu-id="59e26-183">Stellt eine beschreibende Textzeichenfolge für einen Hyperlink dar.</span><span class="sxs-lookup"><span data-stu-id="59e26-183">Represents a descriptive text string for a hyperlink.</span></span>  <br/> |[<span data-ttu-id="59e26-184">Zelle "Description" (Abschnitt "Hyperlinks")</span><span class="sxs-lookup"><span data-stu-id="59e26-184">Description Cell (Hyperlinks Section)</span></span>](description-cell-hyperlinks-section.md) <br/> |
|<span data-ttu-id="59e26-185">ExtraInfo</span><span class="sxs-lookup"><span data-stu-id="59e26-185">ExtraInfo</span></span>  <br/> |<span data-ttu-id="59e26-186">Stellt eine Zeichenfolge, die Informationen für die Auflösung einer URL, beispielsweise die Koordinaten einer Imagemap übergibt.</span><span class="sxs-lookup"><span data-stu-id="59e26-186">Represents a string that passes information to be used in resolving a URL, such as the coordinates of an image map.</span></span>  <br/> |[<span data-ttu-id="59e26-187">Zelle "ExtraInfo" (Abschnitt "Hyperlinks")</span><span class="sxs-lookup"><span data-stu-id="59e26-187">ExtraInfo Cell (Hyperlinks Section)</span></span>](extrainfo-cell-hyperlinks-section.md) <br/> |
|<span data-ttu-id="59e26-188">Frame</span><span class="sxs-lookup"><span data-stu-id="59e26-188">Frame</span></span>  <br/> |<span data-ttu-id="59e26-p107">Stellt den Namen eines Zielframes dar, wenn die Anwendung als aktives Dokument in einer Containeranwendung geöffnet ist. Der Standardwert ist eine leere Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="59e26-p107">Represents the name of a frame to target when the application is open as an Active document in a container application. The default is an empty string.</span></span>  <br/> |[<span data-ttu-id="59e26-191">Zelle "Frame" (Abschnitt "Hyperlinks")</span><span class="sxs-lookup"><span data-stu-id="59e26-191">Frame Cell (Hyperlinks Section)</span></span>](frame-cell-hyperlinks-section.md) <br/> |
|<span data-ttu-id="59e26-192">Nicht sichtbare</span><span class="sxs-lookup"><span data-stu-id="59e26-192">Invisible</span></span>  <br/> |<span data-ttu-id="59e26-193">Gibt an, ob im Kontextmenü eines Shapes oder einer Seite ein Hyperlink angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="59e26-193">Indicates whether a hyperlink appears on the shortcut menu for a shape or page.</span></span>  <br/> |[<span data-ttu-id="59e26-194">Zelle "Invisible" (Abschnitt "Hyperlinks")</span><span class="sxs-lookup"><span data-stu-id="59e26-194">Invisible Cell (Hyperlinks Section)</span></span>](invisible-cell-hyperlinks-section.md) <br/> |
|<span data-ttu-id="59e26-195">NewWindow</span><span class="sxs-lookup"><span data-stu-id="59e26-195">NewWindow</span></span>  <br/> |<span data-ttu-id="59e26-196">Gibt an, ob der Hyperlink in einem neuen Fenster geöffnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="59e26-196">Specifies whether to open the hyperlink in a new window.</span></span>  <br/> |[<span data-ttu-id="59e26-197">Zelle "NewWindow" (Abschnitt "Hyperlinks")</span><span class="sxs-lookup"><span data-stu-id="59e26-197">NewWindow Cell (Hyperlinks Section)</span></span>](newwindow-cell-hyperlinks-section.md) <br/> |
|<span data-ttu-id="59e26-198">SortKey</span><span class="sxs-lookup"><span data-stu-id="59e26-198">SortKey</span></span>  <br/> |<span data-ttu-id="59e26-199">Eine Nummer, mit der die Reihenfolge der Hyperlinks im Kontextmenü angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="59e26-199">A number that determines the order of hyperlinks that appear on a shortcut menu.</span></span>  <br/> |[<span data-ttu-id="59e26-200">Zelle "SortKey" (Abschnitt "Hyperlinks")</span><span class="sxs-lookup"><span data-stu-id="59e26-200">SortKey Cell (Hyperlinks Section)</span></span>](sortkey-cell-hyperlinks-section.md) <br/> |
|<span data-ttu-id="59e26-201">SubAddress</span><span class="sxs-lookup"><span data-stu-id="59e26-201">SubAddress</span></span>  <br/> |<span data-ttu-id="59e26-202">Gibt eine Position im Zieldokument an, mit der eine Verknüpfung hergestellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="59e26-202">Specifies a location within the target document to link to.</span></span>  <br/> |[<span data-ttu-id="59e26-203">Zelle "SubAddress" (Abschnitt "Hyperlinks")</span><span class="sxs-lookup"><span data-stu-id="59e26-203">SubAddress Cell (Hyperlinks Section)</span></span>](subaddress-cell-hyperlinks-section.md) <br/> |
   
