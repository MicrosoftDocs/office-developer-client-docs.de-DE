---
title: PidLidNonSendableBccTrackStatus (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidNonSendableBccTrackStatus
api_type:
- COM
ms.assetid: daad8735-a3da-4a0b-9329-6eb253c281fd
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e5c795f15046bcab40abc2396b36e14925d3869d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359948"
---
# <a name="pidlidnonsendablebcctrackstatus-canonical-property"></a>PidLidNonSendableBccTrackStatus (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält den Wert für jeden Teilnehmer, der in der **eigenschaft dispidNonSendableBCC** ([PidLidNonSendableBcc](pidlidnonsendablebcc-canonical-property.md)) aufgeführt ist.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidNonSendBccTrackStatus  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Common  <br/> |
|Lange ID (LID):  <br/> |0x00008545  <br/> |
|Datentyp:  <br/> |PT_MV_LONG  <br/> |
|Bereich:  <br/> |Allgemeines Messaging  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft ist nur erforderlich, wenn **die dispidNonSendableBCC-Eigenschaft** festgelegt ist. Die Anzahl der Werte in dieser Eigenschaft muss der Anzahl der Werte im **dispidNonSendableBCC entspricht.** Jeder Wert in dieser Eigenschaft entspricht dem Teilnehmer in der **dispidNonSendableBCC-Eigenschaft** am gleichen Index. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungs- und Antwortnachrichten an.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

