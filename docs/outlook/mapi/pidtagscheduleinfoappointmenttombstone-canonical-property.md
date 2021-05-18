---
title: PidTagScheduleInfoAppointmentTombstone (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoAppointmentTombstone
api_type:
- COM
ms.assetid: 6b82e2ee-992f-4cbe-bdcb-e7465e556640
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7a7134a037aa4845ae22ab18899d27f1e50d6b7e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321322"
---
# <a name="pidtagscheduleinfoappointmenttombstone-canonical-property"></a>PidTagScheduleInfoAppointmentTombstone (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine Liste der Datenblöcke, die besprechungen darstellen, die abgelehnt wurden.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_SCHDINFO_APPT_TOMBSTONE  <br/> |
|Kennung:  <br/> |0x686A  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Frei/Gebucht  <br/> |
   
## <a name="remarks"></a>Hinweise

Die Datenblöcke beginnen mit einer Kopfzeile von 32-Bit-Werten, die wie folgt definiert sind:
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|Bezeichner  <br/> |Dieses Feld muss der Wert 0xBEDEAFCD.  <br/> |
|HeaderSize  <br/> |Dieses Feld muss den Wert 0x00000014.  <br/> |
|Version  <br/> |Dieses Feld muss den Wert 3 haben.  <br/> |
|RecordsCount  <br/> |Die Anzahl der folgenden Datensätze.  <br/> |
|RecordsSize  <br/> |Dieses Feld muss den Wert 0x00000014.  <br/> |
   
Dem Header folgen **RecordsCount-Einträge** mit 32-Bit-Werten, die als definiert sind: 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|StartTime  <br/> |Die Startzeit des Besprechungsobjekts in Minuten seit Mitternacht, 1. Januar 1601, UTC.  <br/> |
|EndTime  <br/> |Die Endzeit des Besprechungsobjekts in Minuten seit Mitternacht, 1. Januar 1601, UTC.  <br/> |
|GlobalObjectIdSize  <br/> |Die Größe des Felds GlobalObjectId in Bytes.  <br/> |
|GlobalObjectId  <br/> |Der Wert der **LID_GLOBAL_OBJID** ([PidLidGlobalObjectId](pidlidglobalobjectid-canonical-property.md)) -Eigenschaft der Besprechung, die dieser Datensatz darstellt.  <br/> |
|UserName  <br/> |Die ersten beiden Bytes sind die Länge der PT_STRING8 zeichenfolge, die folgt.  <br/> |
   
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf Exchange Server Protokollspezifikationen.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungs- und Antwortnachrichten an.
    
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

