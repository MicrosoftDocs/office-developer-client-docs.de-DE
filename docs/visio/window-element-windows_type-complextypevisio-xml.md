---
title: Window-Element (Windows_Type ComplexType) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: da776276-e8c2-085b-9b23-e5b1f5ba64cd
description: Repräsentiert ein geöffnetes Fenster in einer Microsoft Visio-Instanz. Dieses Element enthält die erforderlichen Informationen, um ein Fenster auf der Benutzeroberfläche im Anwendungsarbeitsbereich genau neu erstellen, wenn die Datei Anfangs von Visio geöffnet wird.
ms.openlocfilehash: 762b689d625c7865696a0bf8bb8c4acc25e3d8eb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798418"
---
# <a name="window-element-windowstype-complextype-visio-xml"></a><span data-ttu-id="8ddf1-104">Window-Element (Windows_Type ComplexType) ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="8ddf1-104">Window element (Windows_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="8ddf1-105">Repräsentiert ein geöffnetes Fenster in einer Microsoft Visio-Instanz.</span><span class="sxs-lookup"><span data-stu-id="8ddf1-105">Represents an open window in a Microsoft Visio instance.</span></span> <span data-ttu-id="8ddf1-106">Dieses Element enthält die erforderlichen Informationen, um ein Fenster auf der Benutzeroberfläche im Anwendungsarbeitsbereich genau neu erstellen, wenn die Datei Anfangs von Visio geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="8ddf1-106">This element contains information necessary to exactly re-create a user interface window in the application workspace when the file is initially opened by Visio.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8ddf1-107">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="8ddf1-107">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8ddf1-108">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="8ddf1-108">**Element type**</span></span> <br/> |[<span data-ttu-id="8ddf1-109">Window_Type</span><span class="sxs-lookup"><span data-stu-id="8ddf1-109">Window_Type</span></span>](window_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="8ddf1-110">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="8ddf1-110">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="8ddf1-111">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="8ddf1-111">**Schema file**</span></span> <br/> |<span data-ttu-id="8ddf1-112">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="8ddf1-112">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="8ddf1-113">**Dokumentbausteine**</span><span class="sxs-lookup"><span data-stu-id="8ddf1-113">**Document parts**</span></span> <br/> |<span data-ttu-id="8ddf1-114">Windows.Xml</span><span class="sxs-lookup"><span data-stu-id="8ddf1-114">windows.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="8ddf1-115">Definition</span><span class="sxs-lookup"><span data-stu-id="8ddf1-115">Definition</span></span>

```XML
< xs:element name="Window" type="Window_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="8ddf1-116">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="8ddf1-116">Elements and attributes</span></span>

<span data-ttu-id="8ddf1-117">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="8ddf1-117">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="8ddf1-118">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8ddf1-118">Parent elements</span></span>

|<span data-ttu-id="8ddf1-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="8ddf1-119">**Element**</span></span>|<span data-ttu-id="8ddf1-120">**Typ**</span><span class="sxs-lookup"><span data-stu-id="8ddf1-120">**Type**</span></span>|<span data-ttu-id="8ddf1-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8ddf1-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="8ddf1-122">Windows</span><span class="sxs-lookup"><span data-stu-id="8ddf1-122">Windows</span></span>](windows-elementvisio-xml.md) <br/> |[<span data-ttu-id="8ddf1-123">Windows_Type</span><span class="sxs-lookup"><span data-stu-id="8ddf1-123">Windows_Type</span></span>](windows_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8ddf1-124">Enthält die Elemente des **Fensters** für ein Dokument an.</span><span class="sxs-lookup"><span data-stu-id="8ddf1-124">Contains the **Window** elements for a document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="8ddf1-125">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8ddf1-125">Child elements</span></span>

|<span data-ttu-id="8ddf1-126">**Element**</span><span class="sxs-lookup"><span data-stu-id="8ddf1-126">**Element**</span></span>|<span data-ttu-id="8ddf1-127">**Typ**</span><span class="sxs-lookup"><span data-stu-id="8ddf1-127">**Type**</span></span>|<span data-ttu-id="8ddf1-128">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8ddf1-128">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="8ddf1-129">DynamicGridEnabled</span><span class="sxs-lookup"><span data-stu-id="8ddf1-129">DynamicGridEnabled</span></span>](dynamicgridenabled-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8ddf1-130">DynamicGridEnabled_Type</span><span class="sxs-lookup"><span data-stu-id="8ddf1-130">DynamicGridEnabled_Type</span></span>](dynamicgridenabled_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8ddf1-131">Gibt an, ob das dynamische Gitter-Feature für ein Dokument oder Fenster aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="8ddf1-131">Specifies whether the dynamic grid feature is enabled for a document or window.</span></span>  <br/> |
|[<span data-ttu-id="8ddf1-132">GlueSettings</span><span class="sxs-lookup"><span data-stu-id="8ddf1-132">GlueSettings</span></span>](gluesettings-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8ddf1-133">GlueSettings_Type</span><span class="sxs-lookup"><span data-stu-id="8ddf1-133">GlueSettings_Type</span></span>](gluesettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8ddf1-134">Gibt die Objekte, denen Shapes verbunden werden, wenn die Klebefunktion im Dokument aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="8ddf1-134">Specifies the objects that shapes glue to when glue is enabled in the document.</span></span>  <br/> |
|[<span data-ttu-id="8ddf1-135">ShowConnectionPoints</span><span class="sxs-lookup"><span data-stu-id="8ddf1-135">ShowConnectionPoints</span></span>](showconnectionpoints-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8ddf1-136">ShowConnectionPoints_Type</span><span class="sxs-lookup"><span data-stu-id="8ddf1-136">ShowConnectionPoints_Type</span></span>](showconnectionpoints_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8ddf1-137">Gibt an, ob Verbindungspunkte in einem Fenster angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="8ddf1-137">Specifies whether connection points are shown in a window.</span></span>  <br/> |
|[<span data-ttu-id="8ddf1-138">ShowGrid</span><span class="sxs-lookup"><span data-stu-id="8ddf1-138">ShowGrid</span></span>](showgrid-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8ddf1-139">ShowGrid_Type</span><span class="sxs-lookup"><span data-stu-id="8ddf1-139">ShowGrid_Type</span></span>](showgrid_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8ddf1-140">Gibt an, ob ein Raster im Zeichnungsfenster angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="8ddf1-140">Specifies whether a grid is shown in the drawing window.</span></span>  <br/> |
|[<span data-ttu-id="8ddf1-141">ShowGuides</span><span class="sxs-lookup"><span data-stu-id="8ddf1-141">ShowGuides</span></span>](showguides-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8ddf1-142">ShowGuides_Type</span><span class="sxs-lookup"><span data-stu-id="8ddf1-142">ShowGuides_Type</span></span>](showguides_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8ddf1-143">Gibt an, ob Führungslinien im Zeichnungsfenster angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="8ddf1-143">Specifies whether guides are shown in the drawing window.</span></span>  <br/> |
|[<span data-ttu-id="8ddf1-144">ShowPageBreaks</span><span class="sxs-lookup"><span data-stu-id="8ddf1-144">ShowPageBreaks</span></span>](showpagebreaks-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8ddf1-145">ShowPageBreaks_Type</span><span class="sxs-lookup"><span data-stu-id="8ddf1-145">ShowPageBreaks_Type</span></span>](showpagebreaks_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8ddf1-146">Gibt an, ob Seitenumbrüche in einem Fenster angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="8ddf1-146">Specifies whether page breaks are shown in a window.</span></span>  <br/> |
|[<span data-ttu-id="8ddf1-147">ShowRulers</span><span class="sxs-lookup"><span data-stu-id="8ddf1-147">ShowRulers</span></span>](showrulers-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8ddf1-148">ShowRulers_Type</span><span class="sxs-lookup"><span data-stu-id="8ddf1-148">ShowRulers_Type</span></span>](showrulers_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8ddf1-149">Gibt an, ob Lineale im Zeichnungsfenster angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="8ddf1-149">Specifies whether rulers are shown in the drawing window.</span></span>  <br/> |
|[<span data-ttu-id="8ddf1-150">SnapAngles</span><span class="sxs-lookup"><span data-stu-id="8ddf1-150">SnapAngles</span></span>](snapangles-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8ddf1-151">SnapAngles_Type</span><span class="sxs-lookup"><span data-stu-id="8ddf1-151">SnapAngles_Type</span></span>](snapangles_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8ddf1-152">Enthält eine Auflistung von **SnapAngle** -Elementen.</span><span class="sxs-lookup"><span data-stu-id="8ddf1-152">Contains a collection of **SnapAngle** elements.</span></span>  <br/> |
|[<span data-ttu-id="8ddf1-153">SnapExtensions</span><span class="sxs-lookup"><span data-stu-id="8ddf1-153">SnapExtensions</span></span>](snapextensions-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8ddf1-154">SnapExtensions_Type</span><span class="sxs-lookup"><span data-stu-id="8ddf1-154">SnapExtensions_Type</span></span>](snapextensions_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8ddf1-155">Gibt an, ob eine Einstellung für bestimmte Snap-In-Erweiterung aktiviert oder für das aktive Fenster deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="8ddf1-155">Specifies whether a specific snap extension setting is enabled or disabled for the active window.</span></span>  <br/> |
|[<span data-ttu-id="8ddf1-156">SnapSettings</span><span class="sxs-lookup"><span data-stu-id="8ddf1-156">SnapSettings</span></span>](snapsettings-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8ddf1-157">SnapSettings_Type</span><span class="sxs-lookup"><span data-stu-id="8ddf1-157">SnapSettings_Type</span></span>](snapsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8ddf1-158">Gibt die Objekte, die Shapes einrasten, um beim Ausrichten aktiv in das Fenster ist.</span><span class="sxs-lookup"><span data-stu-id="8ddf1-158">Specifies the objects that shapes snap to when snap is active in the window.</span></span>  <br/> |
|[<span data-ttu-id="8ddf1-159">StencilGroup</span><span class="sxs-lookup"><span data-stu-id="8ddf1-159">StencilGroup</span></span>](stencilgroup-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8ddf1-160">StencilGroup_Type</span><span class="sxs-lookup"><span data-stu-id="8ddf1-160">StencilGroup_Type</span></span>](stencilgroup_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8ddf1-161">Gibt die Gruppe der zusammengeführten Schablonenfenster, das Fenster Mitglied ist.</span><span class="sxs-lookup"><span data-stu-id="8ddf1-161">Specifies the group of merged stencil windows of which the window is a member.</span></span>  <br/> |
|[<span data-ttu-id="8ddf1-162">StencilGroupPos</span><span class="sxs-lookup"><span data-stu-id="8ddf1-162">StencilGroupPos</span></span>](stencilgrouppos-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8ddf1-163">StencilGroupPos_Type</span><span class="sxs-lookup"><span data-stu-id="8ddf1-163">StencilGroupPos_Type</span></span>](stencilgrouppos_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8ddf1-164">Enthält eine ganze Zahl, die die relative Position einer Schablone innerhalb einer Gruppe in einem Fenster angibt.</span><span class="sxs-lookup"><span data-stu-id="8ddf1-164">Contains an integer that specifies the relative position of a stencil within a group in a window.</span></span>  <br/> |
|[<span data-ttu-id="8ddf1-165">TabSplitterPos</span><span class="sxs-lookup"><span data-stu-id="8ddf1-165">TabSplitterPos</span></span>](tabsplitterpos-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8ddf1-166">TabSplitterPos_Type</span><span class="sxs-lookup"><span data-stu-id="8ddf1-166">TabSplitterPos_Type</span></span>](tabsplitterpos_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8ddf1-167">Gibt die Breite des Registersteuerelements Seite eines Zeichnungsfenster (als Prozentsatz der Breite des Zeichnungsfensters) an.</span><span class="sxs-lookup"><span data-stu-id="8ddf1-167">Specifies the width of the page tab control of a drawing window (as a fraction of the total width of the drawing window).</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="8ddf1-168">Attribute</span><span class="sxs-lookup"><span data-stu-id="8ddf1-168">Attributes</span></span>

|<span data-ttu-id="8ddf1-169">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="8ddf1-169">**Attribute**</span></span>|<span data-ttu-id="8ddf1-170">**Typ**</span><span class="sxs-lookup"><span data-stu-id="8ddf1-170">**Type**</span></span>|<span data-ttu-id="8ddf1-171">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="8ddf1-171">**Required**</span></span>|<span data-ttu-id="8ddf1-172">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8ddf1-172">**Description**</span></span>|<span data-ttu-id="8ddf1-173">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="8ddf1-173">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="8ddf1-174">Container</span><span class="sxs-lookup"><span data-stu-id="8ddf1-174">Container</span></span>  <br/> |<span data-ttu-id="8ddf1-175">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="8ddf1-175">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="8ddf1-176">Optional</span><span class="sxs-lookup"><span data-stu-id="8ddf1-176">optional</span></span>  <br/> |<span data-ttu-id="8ddf1-177">ID des Containers: Seite, Blatt oder Master-Shape.</span><span class="sxs-lookup"><span data-stu-id="8ddf1-177">ID of container: Page, Sheet, or Master.</span></span> <span data-ttu-id="8ddf1-178">Nur relevant und erforderlich, wenn **ContainerType** angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="8ddf1-178">Only relevant and necessary if **ContainerType** is specified.</span></span>  <br/> |<span data-ttu-id="8ddf1-179">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="8ddf1-179">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="8ddf1-180">ContainerType</span><span class="sxs-lookup"><span data-stu-id="8ddf1-180">ContainerType</span></span>  <br/> |<span data-ttu-id="8ddf1-181">XSD:Token</span><span class="sxs-lookup"><span data-stu-id="8ddf1-181">xsd:token</span></span>  <br/> |<span data-ttu-id="8ddf1-182">Optional</span><span class="sxs-lookup"><span data-stu-id="8ddf1-182">optional</span></span>  <br/> |<span data-ttu-id="8ddf1-183">Kann eine der folgenden Werte sein: Dokument, Page- oder Master.</span><span class="sxs-lookup"><span data-stu-id="8ddf1-183">May be one of the following values: Document, Page, or Master.</span></span> <span data-ttu-id="8ddf1-184">Nur relevant, wenn **Fenstertyp** als Zeichnung oder Blatt angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="8ddf1-184">Only relevant when **WindowType** is specified as Drawing or Sheet.</span></span>  <br/> |<span data-ttu-id="8ddf1-185">Werte des Typs Xsd:token.</span><span class="sxs-lookup"><span data-stu-id="8ddf1-185">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="8ddf1-186">Document</span><span class="sxs-lookup"><span data-stu-id="8ddf1-186">Document</span></span>  <br/> |<span data-ttu-id="8ddf1-187">XSD: String</span><span class="sxs-lookup"><span data-stu-id="8ddf1-187">xsd:string</span></span>  <br/> |<span data-ttu-id="8ddf1-188">Optional</span><span class="sxs-lookup"><span data-stu-id="8ddf1-188">optional</span></span>  <br/> |<span data-ttu-id="8ddf1-189">Dateipfad der in diesem Fenster angezeigte Dokument.</span><span class="sxs-lookup"><span data-stu-id="8ddf1-189">File path of the document displayed in this window.</span></span>  <br/> |<span data-ttu-id="8ddf1-190">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="8ddf1-190">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="8ddf1-191">ID</span><span class="sxs-lookup"><span data-stu-id="8ddf1-191">ID</span></span>  <br/> |<span data-ttu-id="8ddf1-192">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="8ddf1-192">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="8ddf1-193">erforderlich</span><span class="sxs-lookup"><span data-stu-id="8ddf1-193">required</span></span>  <br/> |<span data-ttu-id="8ddf1-194">Die eindeutige ID des Elements in seinem übergeordneten Element.</span><span class="sxs-lookup"><span data-stu-id="8ddf1-194">The unique ID of the element within its parent element.</span></span>  <br/> |<span data-ttu-id="8ddf1-195">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="8ddf1-195">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="8ddf1-196">Master</span><span class="sxs-lookup"><span data-stu-id="8ddf1-196">Master</span></span>  <br/> |<span data-ttu-id="8ddf1-197">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="8ddf1-197">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="8ddf1-198">Optional</span><span class="sxs-lookup"><span data-stu-id="8ddf1-198">optional</span></span>  <br/> |<span data-ttu-id="8ddf1-199">Master-Shape-ID, wenn in diesem Fenster ein Master-Shape angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="8ddf1-199">Master ID if this window is displaying a master.</span></span>  <br/> |<span data-ttu-id="8ddf1-200">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="8ddf1-200">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="8ddf1-201">Page</span><span class="sxs-lookup"><span data-stu-id="8ddf1-201">Page</span></span>  <br/> |<span data-ttu-id="8ddf1-202">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="8ddf1-202">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="8ddf1-203">Optional</span><span class="sxs-lookup"><span data-stu-id="8ddf1-203">optional</span></span>  <br/> |<span data-ttu-id="8ddf1-204">Seiten-ID, wenn dieses Fenster auf eine Seite angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="8ddf1-204">Page ID if this window is displaying a page.</span></span> <span data-ttu-id="8ddf1-205">Relevante, nur wenn **Fenstertyp** als Zeichen- und **ContainerType** angegeben wird als Seite angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="8ddf1-205">Relevant only when **WindowType** is specified as Drawing and **ContainerType** is specified as Page.</span></span>  <br/> |<span data-ttu-id="8ddf1-206">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="8ddf1-206">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="8ddf1-207">ParentWindow</span><span class="sxs-lookup"><span data-stu-id="8ddf1-207">ParentWindow</span></span>  <br/> |<span data-ttu-id="8ddf1-208">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="8ddf1-208">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="8ddf1-209">Optional</span><span class="sxs-lookup"><span data-stu-id="8ddf1-209">optional</span></span>  <br/> |<span data-ttu-id="8ddf1-210">ID des Fensters, in dem diese Schablonenfenster enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="8ddf1-210">ID of window in which this stencil window is contained.</span></span> <span data-ttu-id="8ddf1-211">Nur relevant, wenn **Fenstertyp** als Schablone angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="8ddf1-211">Relevant only when **WindowType** is specified as Stencil.</span></span>  <br/> |<span data-ttu-id="8ddf1-212">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="8ddf1-212">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="8ddf1-213">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="8ddf1-213">ReadOnly</span></span>  <br/> |<span data-ttu-id="8ddf1-214">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="8ddf1-214">xsd:boolean</span></span>  <br/> |<span data-ttu-id="8ddf1-215">Optional</span><span class="sxs-lookup"><span data-stu-id="8ddf1-215">optional</span></span>  <br/> |<span data-ttu-id="8ddf1-216">Schreibschutzflag Wenn die Schablone keiner Dokumentschablone ist.</span><span class="sxs-lookup"><span data-stu-id="8ddf1-216">Read-only flag if this stencil is not a document stencil.</span></span>  <br/> |<span data-ttu-id="8ddf1-217">Werte des Typs xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="8ddf1-217">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="8ddf1-218">Blatt</span><span class="sxs-lookup"><span data-stu-id="8ddf1-218">Sheet</span></span>  <br/> |<span data-ttu-id="8ddf1-219">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="8ddf1-219">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="8ddf1-220">Optional</span><span class="sxs-lookup"><span data-stu-id="8ddf1-220">optional</span></span>  <br/> |<span data-ttu-id="8ddf1-221">ID des Blatts im Container.</span><span class="sxs-lookup"><span data-stu-id="8ddf1-221">ID of sheet in container.</span></span> <span data-ttu-id="8ddf1-222">Nur relevant, wenn Container als Blatt angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="8ddf1-222">Relevant only when Container is specified as Sheet.</span></span>  <br/> |<span data-ttu-id="8ddf1-223">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="8ddf1-223">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="8ddf1-224">ViewCenterX</span><span class="sxs-lookup"><span data-stu-id="8ddf1-224">ViewCenterX</span></span>  <br/> |<span data-ttu-id="8ddf1-225">XSD: Double</span><span class="sxs-lookup"><span data-stu-id="8ddf1-225">xsd:double</span></span>  <br/> |<span data-ttu-id="8ddf1-226">Optional</span><span class="sxs-lookup"><span data-stu-id="8ddf1-226">optional</span></span>  <br/> |<span data-ttu-id="8ddf1-227">**ViewCenterX** und **ViewCenterY** geben einen Mittelpunkt auf einer Seite, die eine neue Ansicht (Fenster) geht davon aus, wenn es zunächst geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="8ddf1-227">**ViewCenterX** and **ViewCenterY** specify a center point on a page that a new view (window) assumes when it is opened initially.</span></span>  <br/> |<span data-ttu-id="8ddf1-228">Werte des Typs xsd: Double.</span><span class="sxs-lookup"><span data-stu-id="8ddf1-228">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="8ddf1-229">ViewCenterY</span><span class="sxs-lookup"><span data-stu-id="8ddf1-229">ViewCenterY</span></span>  <br/> |<span data-ttu-id="8ddf1-230">XSD: Double</span><span class="sxs-lookup"><span data-stu-id="8ddf1-230">xsd:double</span></span>  <br/> |<span data-ttu-id="8ddf1-231">Optional</span><span class="sxs-lookup"><span data-stu-id="8ddf1-231">optional</span></span>  <br/> |<span data-ttu-id="8ddf1-232">**ViewCenterX** und **ViewCenterY** geben einen Mittelpunkt auf einer Seite, die eine neue Ansicht (Fenster) geht davon aus, wenn es zunächst geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="8ddf1-232">**ViewCenterX** and **ViewCenterY** specify a center point on a page that a new view (window) assumes when it is opened initially.</span></span>  <br/> |<span data-ttu-id="8ddf1-233">Werte des Typs xsd: Double.</span><span class="sxs-lookup"><span data-stu-id="8ddf1-233">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="8ddf1-234">ViewScale</span><span class="sxs-lookup"><span data-stu-id="8ddf1-234">ViewScale</span></span>  <br/> |<span data-ttu-id="8ddf1-235">XSD: Double</span><span class="sxs-lookup"><span data-stu-id="8ddf1-235">xsd:double</span></span>  <br/> |<span data-ttu-id="8ddf1-236">Optional</span><span class="sxs-lookup"><span data-stu-id="8ddf1-236">optional</span></span>  <br/> |<span data-ttu-id="8ddf1-237">Der Standardwert Vergrößerungsfaktor verwendet, wenn eine neue Ansicht (Fenster) auf der Seite geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="8ddf1-237">The default magnification factor to use when a new view (window) of the page is opened.</span></span> <span data-ttu-id="8ddf1-238">Beispiel: 1 = 100 %; 1,5 = 150 % und So weiter.</span><span class="sxs-lookup"><span data-stu-id="8ddf1-238">For example, 1 = 100%; 1.5 = 150%, and so on.</span></span>  <br/> |<span data-ttu-id="8ddf1-239">Werte des Typs xsd: Double.</span><span class="sxs-lookup"><span data-stu-id="8ddf1-239">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="8ddf1-240">WindowHeight</span><span class="sxs-lookup"><span data-stu-id="8ddf1-240">WindowHeight</span></span>  <br/> |<span data-ttu-id="8ddf1-241">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="8ddf1-241">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="8ddf1-242">Optional</span><span class="sxs-lookup"><span data-stu-id="8ddf1-242">optional</span></span>  <br/> |<span data-ttu-id="8ddf1-243">Die Höhe des Rechtecks Fenster.</span><span class="sxs-lookup"><span data-stu-id="8ddf1-243">Height of the window rectangle.</span></span>  <br/> |<span data-ttu-id="8ddf1-244">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="8ddf1-244">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="8ddf1-245">WindowLeft</span><span class="sxs-lookup"><span data-stu-id="8ddf1-245">WindowLeft</span></span>  <br/> |<span data-ttu-id="8ddf1-246">XSD:Short</span><span class="sxs-lookup"><span data-stu-id="8ddf1-246">xsd:short</span></span>  <br/> |<span data-ttu-id="8ddf1-247">Optional</span><span class="sxs-lookup"><span data-stu-id="8ddf1-247">optional</span></span>  <br/> |<span data-ttu-id="8ddf1-248">Linke Koordinate des Rechtecks Fenster.</span><span class="sxs-lookup"><span data-stu-id="8ddf1-248">Left coordinate of the window rectangle.</span></span>  <br/> |<span data-ttu-id="8ddf1-249">Werte des Typs Xsd:short.</span><span class="sxs-lookup"><span data-stu-id="8ddf1-249">Values of the xsd:short type.</span></span>  <br/> |
|<span data-ttu-id="8ddf1-250">WindowState</span><span class="sxs-lookup"><span data-stu-id="8ddf1-250">WindowState</span></span>  <br/> |<span data-ttu-id="8ddf1-251">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="8ddf1-251">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="8ddf1-252">Optional</span><span class="sxs-lookup"><span data-stu-id="8ddf1-252">optional</span></span>  <br/> |<span data-ttu-id="8ddf1-253">Eine ganze Zahl angeben bit Kennzeichen.</span><span class="sxs-lookup"><span data-stu-id="8ddf1-253">An integer specifying bit flags.</span></span>  <br/> |<span data-ttu-id="8ddf1-254">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="8ddf1-254">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="8ddf1-255">WindowTop</span><span class="sxs-lookup"><span data-stu-id="8ddf1-255">WindowTop</span></span>  <br/> |<span data-ttu-id="8ddf1-256">XSD:Short</span><span class="sxs-lookup"><span data-stu-id="8ddf1-256">xsd:short</span></span>  <br/> |<span data-ttu-id="8ddf1-257">Optional</span><span class="sxs-lookup"><span data-stu-id="8ddf1-257">optional</span></span>  <br/> |<span data-ttu-id="8ddf1-258">Oberste Koordinate des Rechtecks Fenster.</span><span class="sxs-lookup"><span data-stu-id="8ddf1-258">Top coordinate of the window rectangle.</span></span>  <br/> |<span data-ttu-id="8ddf1-259">Werte des Typs Xsd:short.</span><span class="sxs-lookup"><span data-stu-id="8ddf1-259">Values of the xsd:short type.</span></span>  <br/> |
|<span data-ttu-id="8ddf1-260">Fenstertyp</span><span class="sxs-lookup"><span data-stu-id="8ddf1-260">WindowType</span></span>  <br/> |<span data-ttu-id="8ddf1-261">XSD:Token</span><span class="sxs-lookup"><span data-stu-id="8ddf1-261">xsd:token</span></span>  <br/> |<span data-ttu-id="8ddf1-262">erforderlich</span><span class="sxs-lookup"><span data-stu-id="8ddf1-262">required</span></span>  <br/> |<span data-ttu-id="8ddf1-263">Ein Aufzählungswert, der eine der folgenden möglicherweise: Zeichnung, Blatt, Schablone oder Symbol.</span><span class="sxs-lookup"><span data-stu-id="8ddf1-263">An enumerated value that may be one of the following: Drawing, Sheet, Stencil, or Icon.</span></span>  <br/> |<span data-ttu-id="8ddf1-264">Werte des Typs Xsd:token.</span><span class="sxs-lookup"><span data-stu-id="8ddf1-264">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="8ddf1-265">WindowWidth</span><span class="sxs-lookup"><span data-stu-id="8ddf1-265">WindowWidth</span></span>  <br/> |<span data-ttu-id="8ddf1-266">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="8ddf1-266">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="8ddf1-267">Optional</span><span class="sxs-lookup"><span data-stu-id="8ddf1-267">optional</span></span>  <br/> |<span data-ttu-id="8ddf1-268">Die Breite des Rechtecks Fenster.</span><span class="sxs-lookup"><span data-stu-id="8ddf1-268">Width of the window rectangle.</span></span>  <br/> |<span data-ttu-id="8ddf1-269">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="8ddf1-269">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   
