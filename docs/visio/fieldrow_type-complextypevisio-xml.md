---
title: FieldRow_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3474d268-4435-cb4d-9c66-a30924635e20
ms.openlocfilehash: c0b3dab3cf173db65f0408a2142309d1679f5104
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796975"
---
# <a name="fieldrowtype-complextype-visio-xml"></a><span data-ttu-id="1eff7-102">FieldRow_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="1eff7-102">FieldRow_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="1eff7-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="1eff7-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1eff7-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="1eff7-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="1eff7-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="1eff7-105">**Schema file**</span></span> <br/> |<span data-ttu-id="1eff7-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="1eff7-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="1eff7-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="1eff7-107">**Extension base**</span></span> <br/> |<span data-ttu-id="1eff7-108">IndexedRow_Type</span><span class="sxs-lookup"><span data-stu-id="1eff7-108">IndexedRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1eff7-109">Definition</span><span class="sxs-lookup"><span data-stu-id="1eff7-109">Definition</span></span>

```XML
          <xs:complexType name="FieldRow_Type">
          
          <xs:complexContent>
          <xs:extension base="IndexedRow_Type">
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

## <a name="elements-and-attributes"></a><span data-ttu-id="1eff7-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="1eff7-110">Elements and attributes</span></span>

<span data-ttu-id="1eff7-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="1eff7-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="1eff7-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1eff7-112">Child elements</span></span>

|<span data-ttu-id="1eff7-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="1eff7-113">**Element**</span></span>|<span data-ttu-id="1eff7-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="1eff7-114">**Type**</span></span>|<span data-ttu-id="1eff7-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1eff7-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1eff7-116">Cell</span><span class="sxs-lookup"><span data-stu-id="1eff7-116">Cell</span></span>](cell-element-field-sectionvisio-xml.md) <br/> |[<span data-ttu-id="1eff7-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="1eff7-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="1eff7-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="1eff7-118">Attributes</span></span>

<span data-ttu-id="1eff7-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="1eff7-119">None.</span></span>
  
