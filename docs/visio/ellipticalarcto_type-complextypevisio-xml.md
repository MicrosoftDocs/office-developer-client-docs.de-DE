---
title: EllipticalArcTo_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: dc10f727-5243-2fdb-4042-3dfdfcd8504c
ms.openlocfilehash: 98ff424d0037a9b86749480779d89370c4962caa
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539898"
---
# <a name="ellipticalarcto_type-complextype-visio-xml"></a><span data-ttu-id="cca81-102">EllipticalArcTo_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="cca81-102">EllipticalArcTo_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="cca81-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="cca81-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cca81-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="cca81-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="cca81-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="cca81-105">**Schema file**</span></span> <br/> |<span data-ttu-id="cca81-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="cca81-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="cca81-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="cca81-107">**Extension base**</span></span> <br/> |<span data-ttu-id="cca81-108">GeometryRow_Type</span><span class="sxs-lookup"><span data-stu-id="cca81-108">GeometryRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="cca81-109">Definition</span><span class="sxs-lookup"><span data-stu-id="cca81-109">Definition</span></span>

```XML
          <xs:complexType name="EllipticalArcTo_Type">
          
          <xs:complexContent>
          <xs:extension base="GeometryRow_Type">
          <xs:sequence>
    <xs:element name="Cell"  type="Cell_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="cca81-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="cca81-110">Elements and attributes</span></span>

<span data-ttu-id="cca81-111">Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="cca81-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="cca81-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="cca81-112">Child elements</span></span>

|<span data-ttu-id="cca81-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="cca81-113">**Element**</span></span>|<span data-ttu-id="cca81-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="cca81-114">**Type**</span></span>|<span data-ttu-id="cca81-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="cca81-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="cca81-116">Cell</span><span class="sxs-lookup"><span data-stu-id="cca81-116">Cell</span></span>](cell-element-ellipticalarcto-rowvisio-xml.md) <br/> |[<span data-ttu-id="cca81-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="cca81-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="cca81-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="cca81-118">Attributes</span></span>

<span data-ttu-id="cca81-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="cca81-119">None.</span></span>
  

