---
title: PidLidContactItemData (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidContactItemData
api_type:
- COM
ms.assetid: 411e8f81-c2b9-440a-9e9a-d6add5e4be63
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 031e5483539ce17c8b9b994690985c2349573e27
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319510"
---
# <a name="pidlidcontactitemdata-canonical-property"></a>PidLidContactItemData (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wird zum Anzeigen der Kontaktinformationen verwendet.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidContactItemData  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Address  <br/> |
|Lange ID (LID):  <br/> |0x00008007  <br/> |
|Datentyp:  <br/> |PT_MV_LONG  <br/> |
|Bereich:  <br/> |Kontakt  <br/> |
   
## <a name="remarks"></a>Hinweise

Wenn vorhanden, muss die Eigenschaft sechs Einträge enthalten, die jeweils einem sichtbaren Feld auf der Benutzeroberfläche der Anwendung entspricht.
  
|**Ein basierter Index in die mehrwertige Eigenschaft**|**Der Wert muss einer der folgenden Werte sein:**|**Beschreibung**|
|:-----|:-----|:-----|
|1  <br/> |0x00000001  <br/> |Die Anwendung sollte die Privatadresse des Kontakts anzeigen.  <br/> |
|1  <br/> |0x00000002 oder 0x00000000  <br/> |Die Anwendung sollte die Arbeit des Kontakts anzeigen.  <br/> |
|1  <br/> |0x00000003  <br/> |Die Anwendung sollte die andere Adresse des Kontakts anzeigen.  <br/> |
|2  <br/> |0x00008080  <br/> |Die Anwendung sollte Email1 anzeigen.  <br/> |
|2  <br/> |0x00008090  <br/> |Die Anwendung sollte Email2 anzeigen.  <br/> |
|2  <br/> |0x000080A0  <br/> |Die Anwendung sollte Email3 anzeigen.  <br/> |
|3,4,5,6  <br/> |PropertyID aller Telefoneigenschaften oder faxnummern, die in [[MS-OXOCNTC] angegeben sind.](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)  <br/> |Die Anwendung sollte die entsprechende Eigenschaft anzeigen.  <br/> |
   
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge an, die für Kontakte und persönliche Verteilerlisten zulässig sind.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

