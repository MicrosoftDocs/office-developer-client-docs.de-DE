---
title: PidTagAttachFilename (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachFilename
api_type:
- HeaderDef
ms.assetid: cbf34dd6-7733-47f6-9c41-9d82656ca9dc
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f5dcf90e8224f1bf2e96042a7344109293cc2c3f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319222"
---
# <a name="pidtagattachfilename-canonical-property"></a>PidTagAttachFilename (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält den Basisdateinamen und die Erweiterung einer Anlage, mit Ausnahme des Pfads.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_ATTACH_FILENAME, PR_ATTACH_FILENAME_A, PR_ATTACH_FILENAME_W  <br/> |
|Kennung:  <br/> |0x3704  <br/> |
|Datentyp:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Bereich:  <br/> |Nachrichtenanlage  <br/> |
   
## <a name="remarks"></a>Hinweise

Es wird empfohlen, dass Anlagenobjekte diese Eigenschaften verfügbar machen, die sich auf die **ATTACH_BY_VALUE-,** **ATTACH_BY_REFERENCE-,** **ATTACH_BY_REF_RESOLVE-** und **ATTACH_BY_REF_ONLY-Werte** der **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md))-Eigenschaft bezieht. **PR_ATTACH_FILENAME** und zugeordnete Eigenschaften sind erforderlich, wenn einer dieser Werte verwendet wird. 
  
Diese Eigenschaften können als vorgeschlagener Dateiname zum Speichern der Anlage und zum Eingeben der Dateinamenerweiterung verwendet werden, wenn die **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) -Eigenschaft nicht bereitgestellt wird. 
  
Der Dateiname ist auf acht Zeichen plus eine Drei-Zeichen-Erweiterung beschränkt. Legen Sie für eine Plattform, die lange Dateinamen unterstützt, sowohl diese Eigenschaft als auch die **PR_ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)) -Eigenschaft fest. 
  
MAPI kann nur mit Dateinamen und anderen Zeichenfolgen verwendet werden, die im Zeichensatz American National Standards Institute (ANSI) übergeben werden. Clientanwendungen, die Dateinamen in einem OEM-Zeichensatz (Original Equipment Manufacturer) verwenden, müssen sie vor dem Aufrufen von MAPI in ANSI konvertieren. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Behandelt Nachrichten- und Anlagenobjekte.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Konvertiert von Internetstandard-E-Mail-Konventionen in Nachrichtenobjekte.
    
[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)
  
> Gibt die Eigenschaften von mit Rechten verwalteten codierten Nachrichten an.
    
[[MS-OXOSMIME]](https://msdn.microsoft.com/library/bb17d126-d211-462c-8cd3-454ed33c8746%28Office.15%29.aspx)
  
> Gibt signierte und verschlüsselte S/MIME-Nachrichteneigenschaften an.
    
[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Codiert und decodiert Nachrichten- und Anlagenobjekte in eine effiziente Streamdarstellung.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

