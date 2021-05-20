---
title: Verbinden -Element (Connects_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6e1ad47b-ee28-6b9a-f2f9-642e09ca28d4
description: Repräsentiert eine Verbindung zwischen zwei Shapes in einer Zeichnung, wie z. B. eine Linie und ein Feld in einem Organigramm.
ms.openlocfilehash: 3450a07e042fc633b9cd4952d9b3ad6b8190ed1e
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541995"
---
# <a name="connect-element-connects_type-complextype-visio-xml"></a>Verbinden -Element (Connects_Type complexType) (Visio XML)

Repräsentiert eine Verbindung zwischen zwei Shapes in einer Zeichnung, wie z. B. eine Linie und ein Feld in einem Organigramm.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[Connect_Type](connect_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentteile** <br/> |page#.xml, master#.xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="Connect" type="Connect_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Connects](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[Connects_Type](connects_type-complextypevisio-xml.md) <br/> |Enthält ein **Verbinden-Element** für jede Verbindung zwischen zwei Formen in einer Zeichnung.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|FromCell  <br/> |xsd:string  <br/> |Optional  <br/> |Die Zelle, aus der eine Verbindung stammt.  <br/> |Werte des xsd:string-Typs.  <br/> |
|FromPart  <br/> |xsd:int  <br/> |Optional  <br/> |Der Teil eines Shapes, von dem eine Verbindung stammt.  <br/> |Werte des xsd:int-Typs.  <br/> |
|FromSheet  <br/> |xsd:unsignedInt  <br/> |erforderlich  <br/> |Die ID des Shapes, von dem eine Verbindung oder Verbindungen stammen.  <br/> |Werte des xsd:unsignedInt-Typs.  <br/> |
|ToCell  <br/> |xsd:string  <br/> |Optional  <br/> |Die Zelle, mit der eine Verbindung hergestellt wird.  <br/> |Werte des xsd:string-Typs.  <br/> |
|ToPart  <br/> |xsd:int  <br/> |Optional  <br/> |Der Teil eines Shapes, mit dem eine Verbindung hergestellt wird.  <br/> |Werte des xsd:Int-Typs.  <br/> |
|ToSheet  <br/> |xsd:unsignedInt  <br/> |erforderlich  <br/> |Die ID des Shapes, mit dem eine oder mehrere Verbindungen hergestellt werden.  <br/> |Werte des xsd:unsignedInt-Typs.  <br/> |
   

