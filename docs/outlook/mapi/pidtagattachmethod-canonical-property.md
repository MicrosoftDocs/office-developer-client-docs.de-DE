---
title: PidTagAttachMethod (kanonische Eigenschaft)
manager: soliver
ms.date: 9/7/2016
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachMethod
api_type:
- HeaderDef
ms.assetid: 32089213-ef7b-4152-84ab-b44e9911332b
description: 'Letzte Änderung: 07. September 2016'
ms.openlocfilehash: b84549ab31c939b4e6115795916ebd3520a96dbd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327258"
---
# <a name="pidtagattachmethod-canonical-property"></a>PidTagAttachMethod (kanonische Eigenschaft)

 
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine MAPI-definierte Konstante, die den Zugriff auf den Inhalt einer Anlage darstellt. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_ATTACH_METHOD  <br/> |
|Kennung:  <br/> |0x3705  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Nachrichtenanlage  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft kann genau einen der folgenden Werte haben:
  
NO_ATTACHMENT 
  
> Die Anlage wurde gerade erstellt. 
    
ATTACH_BY_VALUE 
  
> Die **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) -Eigenschaft enthält die Anlagendaten. 
    
ATTACH_BY_REFERENCE 
  
> Die **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) oder **PR_ATTACH_LONG_PATHNAME** ([PidTagAttachLongPathname](pidtagattachlongpathname-canonical-property.md)) -Eigenschaft enthält einen vollqualifizierten Pfad, der die Anlage für Empfänger mit Zugriff auf einen gemeinsamen Dateiserver identifiziert. 
    
ATTACH_BY_REF_RESOLVE 
  
> Die **PR_ATTACH_PATHNAME-** **oder PR_ATTACH_LONG_PATHNAME-Eigenschaft** enthält einen vollqualifizierten Pfad, der die Anlage identifiziert. 
    
ATTACH_BY_REF_ONLY 
  
> Die **PR_ATTACH_PATHNAME-** **oder PR_ATTACH_LONG_PATHNAME-Eigenschaft** enthält einen vollqualifizierten Pfad, der die Anlage identifiziert. 
    
ATTACH_EMBEDDED_MSG 
  
> Die **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) -Eigenschaft enthält ein eingebettetes Objekt, das die **IMessage-Schnittstelle** unterstützt. 
    
ATTACH_OLE 
  
> Die Anlage ist ein eingebettetes OLE-Objekt.
    
ATTACH_BY_WEBREFERENCE 
  
> Der Anlageninhalt befindet sich nicht in der Nachricht. 
    
Beim Erstellen verfügen alle Anlagenobjekte über einen **PR_ATTACH_METHOD** Wert von **NO_ATTACHMENT**. 
  
Clientanwendungen und Dienstanbieter müssen nur die Anlagemethode unterstützen, die durch den Wert ATTACH_BY_VALUE **wird.** Die anderen Anlagenmethoden sind optional. Der Nachrichtenspeicher erzwingt keine Konsistenz  zwischen dem Wert PR_ATTACH_METHOD und den Werten der anderen Anlageneigenschaften. 
  
Namen der universellen Benennungskonvention (Universal Naming Convention, UNC) werden für vollqualifizierte Pfade empfohlen, die mit ATTACH_BY_REFERENCE **und** **ATTACH_BY_REF_ONLY.** Bei **ATTACH_BY_REF_RESOLVE** ist ein absoluter Pfad schneller, da der MAPI-Spooler die Anlage in **ATTACH_BY_VALUE.** 
  
Wenn **ATTACH_BY_REFERENCE** festgelegt ist, **PR_ATTACH_DATA_BIN** leer sein. Ein ausgehendes Gateway kann eine **ATTACH_BY_REFERENCE** anlage in eine ATTACH_BY_VALUE anlage  verwandeln, indem die Anlagendaten in die PR_ATTACH_DATA_BIN **werden.** 
  
Wenn **ATTACH_BY_REF_RESOLVE** festgelegt ist, **muss PR_ATTACH_DATA_BIN** leer sein. Wenn die Nachricht, die die **ATTACH_BY_REF_RESOLVE** enthält, gesendet wird, kopiert der MAPI-Spooler die Anlagendaten in eine **ATTACH_BY_VALUE** Anlage. Bei diesem Auflösungsprozess werden die Anlagendaten in **PR_ATTACH_DATA_BIN.** 
  
Wenn **ATTACH_BY_REF_ONLY** festgelegt ist, **PR_ATTACH_DATA_BIN** leer sein, und das Messagingsystem löst den Anlagenverweis nie auf. Verwenden Sie diesen Wert, wenn Sie den Link senden möchten, jedoch nicht die Daten. 
  
Wenn sich das OLE-Objekt im OLE 2.0-IStorage-Format befindet, ist der Zugriff auf die **Daten** über PR_ATTACH_DATA_OBJ.  Wenn sich das OLE-Objekt im OLE 1.0-OLESTREAM-Format befindet, kann über PR_ATTACH_DATA_BIN **als** IStream auf die **Daten zugegriffen werden.**  Der Typ der #A0 kann durch den Wert PR_ATTACH_TAG **(** [PidTagAttachTag](pidtagattachtag-canonical-property.md)) bestimmt werden. 
  
Weitere Informationen zu OLE-Schnittstellen und -Formaten finden Sie unter  *OLE Programmer's Reference*  . 
  
## <a name="remarks"></a>Hinweise

Wenn die **PR_ATTACH_METHOD** **ATTACH_BY_WEBREFERENCE** wird, befindet sich der Anlageninhalt nicht in der Nachricht. Stattdessen enthält die **PR_ATTACH_LONG_FILENAME-Eigenschaft** eine absolute URL zum Anlageninhalt, der online gespeichert wird. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Behandelt Nachrichten- und Anlagenobjekte.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[PidTagStoreSupportMask (kanonische Eigenschaft)](pidtagstoresupportmask-canonical-property.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

