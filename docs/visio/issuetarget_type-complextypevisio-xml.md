---
title: IssueTarget_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7a0dde1d-5748-63ce-b0da-87f545299b38
ms.openlocfilehash: 38c73e54ff75e94468cfb95258f1fde510d8019a
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542142"
---
# <a name="issuetarget_type-complextype-visio-xml"></a><span data-ttu-id="5359c-102">IssueTarget_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="5359c-102">IssueTarget_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="5359c-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="5359c-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5359c-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="5359c-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="5359c-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="5359c-105">**Schema file**</span></span> <br/> |<span data-ttu-id="5359c-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="5359c-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="5359c-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="5359c-107">**Extension base**</span></span> <br/> |<span data-ttu-id="5359c-108">Keine</span><span class="sxs-lookup"><span data-stu-id="5359c-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="5359c-109">Definition</span><span class="sxs-lookup"><span data-stu-id="5359c-109">Definition</span></span>

```XML
      <xs:complexType name="IssueTarget_Type">
    <xs:attribute name="PageID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="ShapeID"
  type="xsd:unsignedInt"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="5359c-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="5359c-110">Elements and attributes</span></span>

<span data-ttu-id="5359c-111">Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="5359c-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="5359c-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5359c-112">Child elements</span></span>

<span data-ttu-id="5359c-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="5359c-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5359c-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="5359c-114">Attributes</span></span>

|<span data-ttu-id="5359c-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="5359c-115">**Attribute**</span></span>|<span data-ttu-id="5359c-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="5359c-116">**Type**</span></span>|<span data-ttu-id="5359c-117">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="5359c-117">**Required**</span></span>|<span data-ttu-id="5359c-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5359c-118">**Description**</span></span>|<span data-ttu-id="5359c-119">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="5359c-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="5359c-120">PageID</span><span class="sxs-lookup"><span data-stu-id="5359c-120">PageID</span></span>  <br/> |<span data-ttu-id="5359c-121">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="5359c-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="5359c-122">erforderlich</span><span class="sxs-lookup"><span data-stu-id="5359c-122">required</span></span>  <br/> ||<span data-ttu-id="5359c-123">Werte des xsd:unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="5359c-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="5359c-124">ShapeID</span><span class="sxs-lookup"><span data-stu-id="5359c-124">ShapeID</span></span>  <br/> |<span data-ttu-id="5359c-125">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="5359c-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="5359c-126">erforderlich</span><span class="sxs-lookup"><span data-stu-id="5359c-126">required</span></span>  <br/> ||<span data-ttu-id="5359c-127">Werte des xsd:unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="5359c-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

