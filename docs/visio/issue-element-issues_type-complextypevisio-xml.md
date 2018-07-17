---
title: Problem-Element (Issues_Type ComplexType) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5c4d07bf-4edc-e241-7827-017f96c11957
description: Stellt ein einzelnes Überprüfungsproblem im Dokument.
ms.openlocfilehash: 904b42c969bdf97fcfa1e34bad97f73242b17cc2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797256"
---
# <a name="issue-element-issuestype-complextype-visio-xml"></a><span data-ttu-id="6e5aa-103">Problem-Element (Issues_Type ComplexType) ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="6e5aa-103">Issue element (Issues_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="6e5aa-104">Stellt ein einzelnes Überprüfungsproblem im Dokument.</span><span class="sxs-lookup"><span data-stu-id="6e5aa-104">Represents a single validation issue in the document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6e5aa-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="6e5aa-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6e5aa-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="6e5aa-106">**Element type**</span></span> <br/> |[<span data-ttu-id="6e5aa-107">Issue_Type</span><span class="sxs-lookup"><span data-stu-id="6e5aa-107">Issue_Type</span></span>](issue_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="6e5aa-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="6e5aa-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="6e5aa-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="6e5aa-109">**Schema file**</span></span> <br/> |<span data-ttu-id="6e5aa-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="6e5aa-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="6e5aa-111">**Dokumentbausteine**</span><span class="sxs-lookup"><span data-stu-id="6e5aa-111">**Document parts**</span></span> <br/> |<span data-ttu-id="6e5aa-112">Validation.Xml</span><span class="sxs-lookup"><span data-stu-id="6e5aa-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="6e5aa-113">Definition</span><span class="sxs-lookup"><span data-stu-id="6e5aa-113">Definition</span></span>

```XML
< xs:element name="Issue" type="Issue_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="6e5aa-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="6e5aa-114">Elements and attributes</span></span>

<span data-ttu-id="6e5aa-115">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="6e5aa-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="6e5aa-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6e5aa-116">Parent elements</span></span>

|<span data-ttu-id="6e5aa-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="6e5aa-117">**Element**</span></span>|<span data-ttu-id="6e5aa-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="6e5aa-118">**Type**</span></span>|<span data-ttu-id="6e5aa-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6e5aa-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="6e5aa-120">Probleme</span><span class="sxs-lookup"><span data-stu-id="6e5aa-120">Issues</span></span>](issues-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6e5aa-121">Issues_Type</span><span class="sxs-lookup"><span data-stu-id="6e5aa-121">Issues_Type</span></span>](issues_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="6e5aa-122">Enthält alle **Problem** Elemente für das Dokument.</span><span class="sxs-lookup"><span data-stu-id="6e5aa-122">Contains all the **Issue** elements for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="6e5aa-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6e5aa-123">Child elements</span></span>

|<span data-ttu-id="6e5aa-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="6e5aa-124">**Element**</span></span>|<span data-ttu-id="6e5aa-125">**Typ**</span><span class="sxs-lookup"><span data-stu-id="6e5aa-125">**Type**</span></span>|<span data-ttu-id="6e5aa-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6e5aa-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="6e5aa-127">IssueTarget</span><span class="sxs-lookup"><span data-stu-id="6e5aa-127">IssueTarget</span></span>](issuetarget-element-issue_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6e5aa-128">IssueTarget_Type</span><span class="sxs-lookup"><span data-stu-id="6e5aa-128">IssueTarget_Type</span></span>](issuetarget_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="6e5aa-129">Je nach das Ziel des übergeordneten gibt Überprüfungsproblem, entweder die Seite oder die Seite und die Form, der übergeordnete Überprüfungsproblem zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="6e5aa-129">Depending on the target of the parent validation issue, specifies either the page, or both the page and the shape, associated with the parent validation issue.</span></span>  <br/> |
|[<span data-ttu-id="6e5aa-130">RuleInfo</span><span class="sxs-lookup"><span data-stu-id="6e5aa-130">RuleInfo</span></span>](ruleinfo-element-issue_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6e5aa-131">RuleInfo_Type</span><span class="sxs-lookup"><span data-stu-id="6e5aa-131">RuleInfo_Type</span></span>](ruleinfo_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="6e5aa-132">Gibt Informationen zu der Überprüfungsregel, die für die übergeordnete Überprüfungsproblem relevant ist.</span><span class="sxs-lookup"><span data-stu-id="6e5aa-132">Specifies information about the validation rule that the parent validation issue pertains to.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="6e5aa-133">Attribute</span><span class="sxs-lookup"><span data-stu-id="6e5aa-133">Attributes</span></span>

|<span data-ttu-id="6e5aa-134">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="6e5aa-134">**Attribute**</span></span>|<span data-ttu-id="6e5aa-135">**Typ**</span><span class="sxs-lookup"><span data-stu-id="6e5aa-135">**Type**</span></span>|<span data-ttu-id="6e5aa-136">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="6e5aa-136">**Required**</span></span>|<span data-ttu-id="6e5aa-137">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6e5aa-137">**Description**</span></span>|<span data-ttu-id="6e5aa-138">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="6e5aa-138">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="6e5aa-139">ID</span><span class="sxs-lookup"><span data-stu-id="6e5aa-139">ID</span></span>  <br/> |<span data-ttu-id="6e5aa-140">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="6e5aa-140">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="6e5aa-141">erforderlich</span><span class="sxs-lookup"><span data-stu-id="6e5aa-141">required</span></span>  <br/> |<span data-ttu-id="6e5aa-142">Gibt den eindeutigen Bezeichner des überprüfungsproblems.</span><span class="sxs-lookup"><span data-stu-id="6e5aa-142">Specifies the unique identifier of the validation issue.</span></span>  <br/> |<span data-ttu-id="6e5aa-143">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="6e5aa-143">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="6e5aa-144">Ignoriert</span><span class="sxs-lookup"><span data-stu-id="6e5aa-144">Ignored</span></span>  <br/> |<span data-ttu-id="6e5aa-145">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="6e5aa-145">xsd:boolean</span></span>  <br/> |<span data-ttu-id="6e5aa-146">Optional</span><span class="sxs-lookup"><span data-stu-id="6e5aa-146">optional</span></span>  <br/> |<span data-ttu-id="6e5aa-147">Gibt Informationen zu der Überprüfungsregel, die für die übergeordnete Überprüfungsproblem relevant ist.</span><span class="sxs-lookup"><span data-stu-id="6e5aa-147">Specifies information about the validation rule that the parent validation issue pertains to.</span></span>  <br/> |<span data-ttu-id="6e5aa-148">Werte des Typs xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="6e5aa-148">Values of the xsd:boolean type.</span></span>  <br/> |
   
