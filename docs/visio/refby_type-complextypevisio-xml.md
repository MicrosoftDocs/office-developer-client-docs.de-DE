---
title: RefBy_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e2990281-6410-5a35-2b28-3a8b33246c73
ms.openlocfilehash: 7970ae735f4933f05e71f1758912d3ecd382bf89
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538277"
---
# <a name="refby_type-complextype-visio-xml"></a><span data-ttu-id="290f9-102">RefBy_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="290f9-102">RefBy_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="290f9-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="290f9-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="290f9-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="290f9-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="290f9-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="290f9-105">**Schema file**</span></span> <br/> |<span data-ttu-id="290f9-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="290f9-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="290f9-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="290f9-107">**Extension base**</span></span> <br/> |<span data-ttu-id="290f9-108">Keine</span><span class="sxs-lookup"><span data-stu-id="290f9-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="290f9-109">Definition</span><span class="sxs-lookup"><span data-stu-id="290f9-109">Definition</span></span>

```XML
      <xs:complexType name="RefBy_Type">
    <xs:attribute name="T"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="290f9-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="290f9-110">Elements and attributes</span></span>

<span data-ttu-id="290f9-111">Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="290f9-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="290f9-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="290f9-112">Child elements</span></span>

<span data-ttu-id="290f9-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="290f9-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="290f9-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="290f9-114">Attributes</span></span>

|<span data-ttu-id="290f9-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="290f9-115">**Attribute**</span></span>|<span data-ttu-id="290f9-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="290f9-116">**Type**</span></span>|<span data-ttu-id="290f9-117">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="290f9-117">**Required**</span></span>|<span data-ttu-id="290f9-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="290f9-118">**Description**</span></span>|<span data-ttu-id="290f9-119">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="290f9-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="290f9-120">ID</span><span class="sxs-lookup"><span data-stu-id="290f9-120">ID</span></span>  <br/> |<span data-ttu-id="290f9-121">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="290f9-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="290f9-122">erforderlich</span><span class="sxs-lookup"><span data-stu-id="290f9-122">required</span></span>  <br/> ||<span data-ttu-id="290f9-123">Werte des xsd:unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="290f9-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="290f9-124">T</span><span class="sxs-lookup"><span data-stu-id="290f9-124">T</span></span>  <br/> |<span data-ttu-id="290f9-125">xsd:string</span><span class="sxs-lookup"><span data-stu-id="290f9-125">xsd:string</span></span>  <br/> |<span data-ttu-id="290f9-126">erforderlich</span><span class="sxs-lookup"><span data-stu-id="290f9-126">required</span></span>  <br/> ||<span data-ttu-id="290f9-127">Werte des xsd:string-Typs.</span><span class="sxs-lookup"><span data-stu-id="290f9-127">Values of the xsd:string type.</span></span>  <br/> |
   

