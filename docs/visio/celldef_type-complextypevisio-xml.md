---
title: CellDef_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 87ea346d-1786-dc87-073d-8e7459b7fef1
ms.openlocfilehash: 6471158df8c89e8d7b0202f9bdbce196e24b93b8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796600"
---
# <a name="celldeftype-complextype-visio-xml"></a><span data-ttu-id="88383-102">CellDef_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="88383-102">CellDef_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="88383-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="88383-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="88383-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="88383-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="88383-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="88383-105">**Schema file**</span></span> <br/> |<span data-ttu-id="88383-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="88383-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="88383-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="88383-107">**Extension base**</span></span> <br/> |<span data-ttu-id="88383-108">Keine</span><span class="sxs-lookup"><span data-stu-id="88383-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="88383-109">Definition</span><span class="sxs-lookup"><span data-stu-id="88383-109">Definition</span></span>

```XML
      <xs:complexType name="CellDef_Type">
    <xs:attribute name="N"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="T"
  type="xsd:token"
     use="required"
    />
    <xs:attribute name="F"
  type="xsd:string"
    />
    <xs:attribute name="IX"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="S"
  type="xsd:unsignedByte"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="88383-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="88383-110">Elements and attributes</span></span>

<span data-ttu-id="88383-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="88383-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="88383-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="88383-112">Child elements</span></span>

<span data-ttu-id="88383-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="88383-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="88383-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="88383-114">Attributes</span></span>

|<span data-ttu-id="88383-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="88383-115">**Attribute**</span></span>|<span data-ttu-id="88383-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="88383-116">**Type**</span></span>|<span data-ttu-id="88383-117">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="88383-117">**Required**</span></span>|<span data-ttu-id="88383-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="88383-118">**Description**</span></span>|<span data-ttu-id="88383-119">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="88383-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="88383-120">F</span><span class="sxs-lookup"><span data-stu-id="88383-120">F</span></span>  <br/> |<span data-ttu-id="88383-121">XSD: String</span><span class="sxs-lookup"><span data-stu-id="88383-121">xsd:string</span></span>  <br/> |<span data-ttu-id="88383-122">Optional</span><span class="sxs-lookup"><span data-stu-id="88383-122">optional</span></span>  <br/> ||<span data-ttu-id="88383-123">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="88383-123">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="88383-124">IX</span><span class="sxs-lookup"><span data-stu-id="88383-124">IX</span></span>  <br/> |<span data-ttu-id="88383-125">XSD:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="88383-125">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="88383-126">Optional</span><span class="sxs-lookup"><span data-stu-id="88383-126">optional</span></span>  <br/> ||<span data-ttu-id="88383-127">Werte des Typs Xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="88383-127">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="88383-128">N</span><span class="sxs-lookup"><span data-stu-id="88383-128">N</span></span>  <br/> |<span data-ttu-id="88383-129">XSD: String</span><span class="sxs-lookup"><span data-stu-id="88383-129">xsd:string</span></span>  <br/> |<span data-ttu-id="88383-130">erforderlich</span><span class="sxs-lookup"><span data-stu-id="88383-130">required</span></span>  <br/> ||<span data-ttu-id="88383-131">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="88383-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="88383-132">S</span><span class="sxs-lookup"><span data-stu-id="88383-132">S</span></span>  <br/> |<span data-ttu-id="88383-133">XSD:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="88383-133">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="88383-134">Optional</span><span class="sxs-lookup"><span data-stu-id="88383-134">optional</span></span>  <br/> ||<span data-ttu-id="88383-135">Werte des Typs Xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="88383-135">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="88383-136">T</span><span class="sxs-lookup"><span data-stu-id="88383-136">T</span></span>  <br/> |<span data-ttu-id="88383-137">XSD:Token</span><span class="sxs-lookup"><span data-stu-id="88383-137">xsd:token</span></span>  <br/> |<span data-ttu-id="88383-138">erforderlich</span><span class="sxs-lookup"><span data-stu-id="88383-138">required</span></span>  <br/> ||<span data-ttu-id="88383-139">Werte des Typs Xsd:token.</span><span class="sxs-lookup"><span data-stu-id="88383-139">Values of the xsd:token type.</span></span>  <br/> |
   
