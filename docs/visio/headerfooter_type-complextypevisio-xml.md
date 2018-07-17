---
title: HeaderFooter_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f5fcf3d9-c11a-ed5e-0bf5-e706259ef30b
ms.openlocfilehash: 9c567542061ec419de9c4347209059b0486bdf88
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797124"
---
# <a name="headerfootertype-complextype-visio-xml"></a><span data-ttu-id="d3d84-102">HeaderFooter_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="d3d84-102">HeaderFooter_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="d3d84-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="d3d84-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d3d84-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="d3d84-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="d3d84-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="d3d84-105">**Schema file**</span></span> <br/> |<span data-ttu-id="d3d84-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="d3d84-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="d3d84-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="d3d84-107">**Extension base**</span></span> <br/> |<span data-ttu-id="d3d84-108">Keine</span><span class="sxs-lookup"><span data-stu-id="d3d84-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d3d84-109">Definition</span><span class="sxs-lookup"><span data-stu-id="d3d84-109">Definition</span></span>

```XML
          <xs:complexType name="HeaderFooter_Type">
          
          <xs:all>
    <xs:element name="HeaderMargin"  type="HeaderMargin_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="FooterMargin"  type="FooterMargin_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="HeaderLeft"  type="HeaderLeft_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="HeaderCenter"  type="HeaderCenter_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="HeaderRight"  type="HeaderRight_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="FooterLeft"  type="FooterLeft_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="FooterCenter"  type="FooterCenter_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="FooterRight"  type="FooterRight_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="HeaderFooterFont"  type="HeaderFooterFont_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:all>
    <xs:attribute name="HeaderFooterColor"
  type="xsd:string"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="d3d84-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="d3d84-110">Elements and attributes</span></span>

<span data-ttu-id="d3d84-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="d3d84-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="d3d84-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d3d84-112">Child elements</span></span>

|<span data-ttu-id="d3d84-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="d3d84-113">**Element**</span></span>|<span data-ttu-id="d3d84-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="d3d84-114">**Type**</span></span>|<span data-ttu-id="d3d84-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d3d84-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d3d84-116">FooterCenter</span><span class="sxs-lookup"><span data-stu-id="d3d84-116">FooterCenter</span></span>](footercenter-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d3d84-117">FooterCenter_Type</span><span class="sxs-lookup"><span data-stu-id="d3d84-117">FooterCenter_Type</span></span>](footercenter_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="d3d84-118">FooterLeft</span><span class="sxs-lookup"><span data-stu-id="d3d84-118">FooterLeft</span></span>](footerleft-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d3d84-119">FooterLeft_Type</span><span class="sxs-lookup"><span data-stu-id="d3d84-119">FooterLeft_Type</span></span>](footerleft_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="d3d84-120">FooterMargin</span><span class="sxs-lookup"><span data-stu-id="d3d84-120">FooterMargin</span></span>](footermargin-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d3d84-121">FooterMargin_Type</span><span class="sxs-lookup"><span data-stu-id="d3d84-121">FooterMargin_Type</span></span>](footermargin_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="d3d84-122">FooterRight</span><span class="sxs-lookup"><span data-stu-id="d3d84-122">FooterRight</span></span>](footerright-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d3d84-123">FooterRight_Type</span><span class="sxs-lookup"><span data-stu-id="d3d84-123">FooterRight_Type</span></span>](footerright_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="d3d84-124">HeaderCenter</span><span class="sxs-lookup"><span data-stu-id="d3d84-124">HeaderCenter</span></span>](headercenter-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d3d84-125">HeaderCenter_Type</span><span class="sxs-lookup"><span data-stu-id="d3d84-125">HeaderCenter_Type</span></span>](headercenter_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="d3d84-126">HeaderFooterFont</span><span class="sxs-lookup"><span data-stu-id="d3d84-126">HeaderFooterFont</span></span>](headerfooterfont-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d3d84-127">HeaderFooterFont_Type</span><span class="sxs-lookup"><span data-stu-id="d3d84-127">HeaderFooterFont_Type</span></span>](headerfooterfont_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="d3d84-128">HeaderLeft</span><span class="sxs-lookup"><span data-stu-id="d3d84-128">HeaderLeft</span></span>](headerleft-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d3d84-129">HeaderLeft_Type</span><span class="sxs-lookup"><span data-stu-id="d3d84-129">HeaderLeft_Type</span></span>](headerleft_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="d3d84-130">HeaderMargin</span><span class="sxs-lookup"><span data-stu-id="d3d84-130">HeaderMargin</span></span>](headermargin-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d3d84-131">HeaderMargin_Type</span><span class="sxs-lookup"><span data-stu-id="d3d84-131">HeaderMargin_Type</span></span>](headermargin_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="d3d84-132">HeaderRight</span><span class="sxs-lookup"><span data-stu-id="d3d84-132">HeaderRight</span></span>](headerright-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d3d84-133">HeaderRight_Type</span><span class="sxs-lookup"><span data-stu-id="d3d84-133">HeaderRight_Type</span></span>](headerright_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="d3d84-134">Attribute</span><span class="sxs-lookup"><span data-stu-id="d3d84-134">Attributes</span></span>

|<span data-ttu-id="d3d84-135">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="d3d84-135">**Attribute**</span></span>|<span data-ttu-id="d3d84-136">**Typ**</span><span class="sxs-lookup"><span data-stu-id="d3d84-136">**Type**</span></span>|<span data-ttu-id="d3d84-137">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="d3d84-137">**Required**</span></span>|<span data-ttu-id="d3d84-138">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d3d84-138">**Description**</span></span>|<span data-ttu-id="d3d84-139">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="d3d84-139">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="d3d84-140">HeaderFooterColor</span><span class="sxs-lookup"><span data-stu-id="d3d84-140">HeaderFooterColor</span></span>  <br/> |<span data-ttu-id="d3d84-141">XSD: String</span><span class="sxs-lookup"><span data-stu-id="d3d84-141">xsd:string</span></span>  <br/> |<span data-ttu-id="d3d84-142">Optional</span><span class="sxs-lookup"><span data-stu-id="d3d84-142">optional</span></span>  <br/> ||<span data-ttu-id="d3d84-143">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="d3d84-143">Values of the xsd:string type.</span></span>  <br/> |
   
