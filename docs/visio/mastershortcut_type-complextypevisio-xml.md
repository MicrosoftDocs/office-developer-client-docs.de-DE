---
title: MasterShortcut_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0192c733-09b8-d9ce-1d88-b4d97e2e1a36
ms.openlocfilehash: ed8dd8ef985c814e41017526144bd7ec8cb63424
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538060"
---
# <a name="mastershortcut_type-complextype-visio-xml"></a><span data-ttu-id="41c18-102">MasterShortcut_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="41c18-102">MasterShortcut_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="41c18-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="41c18-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="41c18-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="41c18-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="41c18-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="41c18-105">**Schema file**</span></span> <br/> |<span data-ttu-id="41c18-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="41c18-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="41c18-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="41c18-107">**Extension base**</span></span> <br/> |<span data-ttu-id="41c18-108">Keine</span><span class="sxs-lookup"><span data-stu-id="41c18-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="41c18-109">Definition</span><span class="sxs-lookup"><span data-stu-id="41c18-109">Definition</span></span>

```XML
          <xs:complexType name="MasterShortcut_Type">
          
          <xs:all>
    <xs:element name="Icon"  type="Icon_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:all>
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="Name"
  type="xsd:string"
    />
    <xs:attribute name="NameU"
  type="xsd:string"
    />
    <xs:attribute name="IsCustomName"
  type="xsd:boolean"
    />
    <xs:attribute name="IsCustomNameU"
  type="xsd:boolean"
    />
    <xs:attribute name="IconSize"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="PatternFlags"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="Prompt"
  type="xsd:string"
    />
    <xs:attribute name="ShortcutURL"
  type="xsd:string"
    />
    <xs:attribute name="ShortcutHelp"
  type="xsd:string"
    />
    <xs:attribute name="AlignName"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="MasterType"
  type="xsd:unsignedShort"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="41c18-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="41c18-110">Elements and attributes</span></span>

<span data-ttu-id="41c18-111">Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="41c18-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="41c18-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="41c18-112">Child elements</span></span>

|<span data-ttu-id="41c18-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="41c18-113">**Element**</span></span>|<span data-ttu-id="41c18-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="41c18-114">**Type**</span></span>|<span data-ttu-id="41c18-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="41c18-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="41c18-116">Icon</span><span class="sxs-lookup"><span data-stu-id="41c18-116">Icon</span></span>](icon-element-mastershortcut_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="41c18-117">Icon_Type</span><span class="sxs-lookup"><span data-stu-id="41c18-117">Icon_Type</span></span>](icon_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="41c18-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="41c18-118">Attributes</span></span>

|<span data-ttu-id="41c18-119">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="41c18-119">**Attribute**</span></span>|<span data-ttu-id="41c18-120">**Typ**</span><span class="sxs-lookup"><span data-stu-id="41c18-120">**Type**</span></span>|<span data-ttu-id="41c18-121">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="41c18-121">**Required**</span></span>|<span data-ttu-id="41c18-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="41c18-122">**Description**</span></span>|<span data-ttu-id="41c18-123">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="41c18-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="41c18-124">AlignName</span><span class="sxs-lookup"><span data-stu-id="41c18-124">AlignName</span></span>  <br/> |<span data-ttu-id="41c18-125">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="41c18-125">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="41c18-126">Optional</span><span class="sxs-lookup"><span data-stu-id="41c18-126">optional</span></span>  <br/> ||<span data-ttu-id="41c18-127">Werte des Typs xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="41c18-127">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="41c18-128">IconSize</span><span class="sxs-lookup"><span data-stu-id="41c18-128">IconSize</span></span>  <br/> |<span data-ttu-id="41c18-129">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="41c18-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="41c18-130">Optional</span><span class="sxs-lookup"><span data-stu-id="41c18-130">optional</span></span>  <br/> ||<span data-ttu-id="41c18-131">Werte des Typs xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="41c18-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="41c18-132">ID</span><span class="sxs-lookup"><span data-stu-id="41c18-132">ID</span></span>  <br/> |<span data-ttu-id="41c18-133">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="41c18-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="41c18-134">erforderlich</span><span class="sxs-lookup"><span data-stu-id="41c18-134">required</span></span>  <br/> ||<span data-ttu-id="41c18-135">Werte des xsd:unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="41c18-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="41c18-136">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="41c18-136">IsCustomName</span></span>  <br/> |<span data-ttu-id="41c18-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="41c18-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="41c18-138">Optional</span><span class="sxs-lookup"><span data-stu-id="41c18-138">optional</span></span>  <br/> ||<span data-ttu-id="41c18-139">Werte des typs xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="41c18-139">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="41c18-140">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="41c18-140">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="41c18-141">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="41c18-141">xsd:boolean</span></span>  <br/> |<span data-ttu-id="41c18-142">Optional</span><span class="sxs-lookup"><span data-stu-id="41c18-142">optional</span></span>  <br/> ||<span data-ttu-id="41c18-143">Werte des typs xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="41c18-143">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="41c18-144">MasterType</span><span class="sxs-lookup"><span data-stu-id="41c18-144">MasterType</span></span>  <br/> |<span data-ttu-id="41c18-145">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="41c18-145">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="41c18-146">Optional</span><span class="sxs-lookup"><span data-stu-id="41c18-146">optional</span></span>  <br/> ||<span data-ttu-id="41c18-147">Werte des Typs xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="41c18-147">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="41c18-148">Name</span><span class="sxs-lookup"><span data-stu-id="41c18-148">Name</span></span>  <br/> |<span data-ttu-id="41c18-149">xsd:string</span><span class="sxs-lookup"><span data-stu-id="41c18-149">xsd:string</span></span>  <br/> |<span data-ttu-id="41c18-150">Optional</span><span class="sxs-lookup"><span data-stu-id="41c18-150">optional</span></span>  <br/> ||<span data-ttu-id="41c18-151">Werte des xsd:string-Typs.</span><span class="sxs-lookup"><span data-stu-id="41c18-151">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="41c18-152">NameU</span><span class="sxs-lookup"><span data-stu-id="41c18-152">NameU</span></span>  <br/> |<span data-ttu-id="41c18-153">xsd:string</span><span class="sxs-lookup"><span data-stu-id="41c18-153">xsd:string</span></span>  <br/> |<span data-ttu-id="41c18-154">Optional</span><span class="sxs-lookup"><span data-stu-id="41c18-154">optional</span></span>  <br/> ||<span data-ttu-id="41c18-155">Werte des xsd:string-Typs.</span><span class="sxs-lookup"><span data-stu-id="41c18-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="41c18-156">PatternFlags</span><span class="sxs-lookup"><span data-stu-id="41c18-156">PatternFlags</span></span>  <br/> |<span data-ttu-id="41c18-157">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="41c18-157">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="41c18-158">Optional</span><span class="sxs-lookup"><span data-stu-id="41c18-158">optional</span></span>  <br/> ||<span data-ttu-id="41c18-159">Werte des Typs xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="41c18-159">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="41c18-160">Eingabeaufforderung</span><span class="sxs-lookup"><span data-stu-id="41c18-160">Prompt</span></span>  <br/> |<span data-ttu-id="41c18-161">xsd:string</span><span class="sxs-lookup"><span data-stu-id="41c18-161">xsd:string</span></span>  <br/> |<span data-ttu-id="41c18-162">Optional</span><span class="sxs-lookup"><span data-stu-id="41c18-162">optional</span></span>  <br/> ||<span data-ttu-id="41c18-163">Werte des xsd:string-Typs.</span><span class="sxs-lookup"><span data-stu-id="41c18-163">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="41c18-164">ShortcutHelp</span><span class="sxs-lookup"><span data-stu-id="41c18-164">ShortcutHelp</span></span>  <br/> |<span data-ttu-id="41c18-165">xsd:string</span><span class="sxs-lookup"><span data-stu-id="41c18-165">xsd:string</span></span>  <br/> |<span data-ttu-id="41c18-166">Optional</span><span class="sxs-lookup"><span data-stu-id="41c18-166">optional</span></span>  <br/> ||<span data-ttu-id="41c18-167">Werte des xsd:string-Typs.</span><span class="sxs-lookup"><span data-stu-id="41c18-167">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="41c18-168">ShortcutURL</span><span class="sxs-lookup"><span data-stu-id="41c18-168">ShortcutURL</span></span>  <br/> |<span data-ttu-id="41c18-169">xsd:string</span><span class="sxs-lookup"><span data-stu-id="41c18-169">xsd:string</span></span>  <br/> |<span data-ttu-id="41c18-170">Optional</span><span class="sxs-lookup"><span data-stu-id="41c18-170">optional</span></span>  <br/> ||<span data-ttu-id="41c18-171">Werte des xsd:string-Typs.</span><span class="sxs-lookup"><span data-stu-id="41c18-171">Values of the xsd:string type.</span></span>  <br/> |
   

