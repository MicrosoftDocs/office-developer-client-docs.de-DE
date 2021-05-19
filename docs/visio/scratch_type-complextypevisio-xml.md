---
title: Scratch_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1e3dd8c8-e84c-61ff-bfff-57d97545e441
ms.openlocfilehash: 434565cafe7d4345f3da7727760b21bfc186ee96
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539054"
---
# <a name="scratch_type-complextype-visio-xml"></a><span data-ttu-id="a1692-102">Scratch_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="a1692-102">Scratch_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="a1692-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="a1692-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a1692-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="a1692-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="a1692-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="a1692-105">**Schema file**</span></span> <br/> |<span data-ttu-id="a1692-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="a1692-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="a1692-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="a1692-107">**Extension base**</span></span> <br/> |<span data-ttu-id="a1692-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="a1692-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a1692-109">Definition</span><span class="sxs-lookup"><span data-stu-id="a1692-109">Definition</span></span>

```XML
          <xs:complexType name="Scratch_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Row"  type="ScratchRow_Type"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="a1692-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="a1692-110">Elements and attributes</span></span>

<span data-ttu-id="a1692-111">Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="a1692-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="a1692-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a1692-112">Child elements</span></span>

|<span data-ttu-id="a1692-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="a1692-113">**Element**</span></span>|<span data-ttu-id="a1692-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="a1692-114">**Type**</span></span>|<span data-ttu-id="a1692-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a1692-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a1692-116">Row</span><span class="sxs-lookup"><span data-stu-id="a1692-116">Row</span></span>](row-element-scratch-sectionvisio-xml.md) <br/> |[<span data-ttu-id="a1692-117">ScratchRow_Type</span><span class="sxs-lookup"><span data-stu-id="a1692-117">ScratchRow_Type</span></span>](scratchrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="a1692-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="a1692-118">Attributes</span></span>

<span data-ttu-id="a1692-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="a1692-119">None.</span></span>
  

