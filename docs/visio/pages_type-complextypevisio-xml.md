---
title: Pages_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 13508e59-e29a-ca70-676b-c5b23ca8e3d0
ms.openlocfilehash: 4615f365448b96981088352f9f2d6e98255e4101
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538942"
---
# <a name="pages_type-complextype-visio-xml"></a><span data-ttu-id="7a987-102">Pages_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="7a987-102">Pages_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="7a987-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="7a987-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7a987-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="7a987-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="7a987-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="7a987-105">**Schema file**</span></span> <br/> |<span data-ttu-id="7a987-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="7a987-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="7a987-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="7a987-107">**Extension base**</span></span> <br/> |<span data-ttu-id="7a987-108">Keine</span><span class="sxs-lookup"><span data-stu-id="7a987-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="7a987-109">Definition</span><span class="sxs-lookup"><span data-stu-id="7a987-109">Definition</span></span>

```XML
          <xs:complexType name="Pages_Type">
          
          <xs:sequence>
    <xs:element name="Page"  type="Page_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="7a987-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="7a987-110">Elements and attributes</span></span>

<span data-ttu-id="7a987-111">Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="7a987-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="7a987-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7a987-112">Child elements</span></span>

|<span data-ttu-id="7a987-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="7a987-113">**Element**</span></span>|<span data-ttu-id="7a987-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="7a987-114">**Type**</span></span>|<span data-ttu-id="7a987-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7a987-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="7a987-116">Page</span><span class="sxs-lookup"><span data-stu-id="7a987-116">Page</span></span>](page-element-pages_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7a987-117">Page_Type</span><span class="sxs-lookup"><span data-stu-id="7a987-117">Page_Type</span></span>](page_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="7a987-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="7a987-118">Attributes</span></span>

<span data-ttu-id="7a987-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="7a987-119">None.</span></span>
  

