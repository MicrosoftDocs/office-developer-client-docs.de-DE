---
title: Rel-Element (Page_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d61b1b97-c360-4d9d-217f-e6f45f760e42
description: Gibt eine Beziehung zu einem Teil mit der entsprechenden Seiten-XML an.
ms.openlocfilehash: 19224a7057786677cdb371df887e69e8457649c6
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542779"
---
# <a name="rel-element-page_type-complextype-visio-xml"></a>Rel-Element (Page_Type complexType) (Visio XML)

Gibt eine Beziehung zu einem Teil mit der entsprechenden Seiten-XML an.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[Rel_Type](rel_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentteile** <br/> |pages.xml, masters.xml, recordsets.xml, Seite#.xml, Master#.xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="Rel" type="Rel_Type" minOccurs="1" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Page](page-element-pages_type-complextypevisio-xml.md) <br/> |[Page_Type](page_type-complextypevisio-xml.md) <br/> |Gibt eine Instanz von Seiten-XML an, die in der Zeichnung gespeichert ist.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|r:id  <br/> |xsd:string  <br/> Weitere Informationen finden Sie in der "Anmerkungen".  <br/> |erforderlich  <br/> |Gibt eine Beziehung zu einem Teil an.  <br/> |"rId#"  <br/> Weitere Informationen finden Sie in der "Anmerkungen".  <br/> |
   
## <a name="remarks"></a>Hinweise

Der Wert des **r:id-Attributs** muss ein **ST_RelationshipID** sein. Der **ST_RelationshipID** ist eine Zeichenfolge im Format "rId#", wobei das letzte Zeichen eine Zahl sein muss. Die Zahl muss zwischen allen gleichgeordneten Elementen des **Rel-Elements eindeutig** sein. 
  
Weitere Informationen zum ST_RelationshipID finden Sie in der [SPEZIFIKATION ISO/IEC 29500 Part 1](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).
  

