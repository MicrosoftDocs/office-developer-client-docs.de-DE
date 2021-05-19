---
title: Issue_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d6768062-37aa-5658-f068-dae8d3a24717
ms.openlocfilehash: b351554fe7919cada99172f721f5dbe2fd8f243a
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542961"
---
# <a name="issue_type-complextype-visio-xml"></a><span data-ttu-id="4efba-102">Issue_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="4efba-102">Issue_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="4efba-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="4efba-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4efba-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="4efba-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="4efba-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="4efba-105">**Schema file**</span></span> <br/> |<span data-ttu-id="4efba-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="4efba-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="4efba-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="4efba-107">**Extension base**</span></span> <br/> |<span data-ttu-id="4efba-108">Keine</span><span class="sxs-lookup"><span data-stu-id="4efba-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4efba-109">Definition</span><span class="sxs-lookup"><span data-stu-id="4efba-109">Definition</span></span>

```XML
          <xs:complexType name="Issue_Type">
          
          <xs:sequence>
    <xs:element name="IssueTarget"  type="IssueTarget_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="RuleInfo"  type="RuleInfo_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="Ignored"
  type="xsd:boolean"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="4efba-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="4efba-110">Elements and attributes</span></span>

<span data-ttu-id="4efba-111">Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="4efba-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="4efba-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4efba-112">Child elements</span></span>

|<span data-ttu-id="4efba-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="4efba-113">**Element**</span></span>|<span data-ttu-id="4efba-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="4efba-114">**Type**</span></span>|<span data-ttu-id="4efba-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4efba-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4efba-116">IssueTarget</span><span class="sxs-lookup"><span data-stu-id="4efba-116">IssueTarget</span></span>](issuetarget-element-issue_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4efba-117">IssueTarget_Type</span><span class="sxs-lookup"><span data-stu-id="4efba-117">IssueTarget_Type</span></span>](issuetarget_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="4efba-118">RuleInfo</span><span class="sxs-lookup"><span data-stu-id="4efba-118">RuleInfo</span></span>](ruleinfo-element-issue_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4efba-119">RuleInfo_Type</span><span class="sxs-lookup"><span data-stu-id="4efba-119">RuleInfo_Type</span></span>](ruleinfo_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="4efba-120">Attribute</span><span class="sxs-lookup"><span data-stu-id="4efba-120">Attributes</span></span>

|<span data-ttu-id="4efba-121">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="4efba-121">**Attribute**</span></span>|<span data-ttu-id="4efba-122">**Typ**</span><span class="sxs-lookup"><span data-stu-id="4efba-122">**Type**</span></span>|<span data-ttu-id="4efba-123">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="4efba-123">**Required**</span></span>|<span data-ttu-id="4efba-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4efba-124">**Description**</span></span>|<span data-ttu-id="4efba-125">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="4efba-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="4efba-126">ID</span><span class="sxs-lookup"><span data-stu-id="4efba-126">ID</span></span>  <br/> |<span data-ttu-id="4efba-127">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="4efba-127">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="4efba-128">erforderlich</span><span class="sxs-lookup"><span data-stu-id="4efba-128">required</span></span>  <br/> ||<span data-ttu-id="4efba-129">Werte des xsd:unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="4efba-129">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="4efba-130">Ignoriert</span><span class="sxs-lookup"><span data-stu-id="4efba-130">Ignored</span></span>  <br/> |<span data-ttu-id="4efba-131">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="4efba-131">xsd:boolean</span></span>  <br/> |<span data-ttu-id="4efba-132">Optional</span><span class="sxs-lookup"><span data-stu-id="4efba-132">optional</span></span>  <br/> ||<span data-ttu-id="4efba-133">Werte des typs xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="4efba-133">Values of the xsd:boolean type.</span></span>  <br/> |
   

