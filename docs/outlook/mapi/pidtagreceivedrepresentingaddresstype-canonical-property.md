---
title: PidTagReceivedRepresentingAddressType (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReceivedRepresentingAddressType
api_type:
- COM
ms.assetid: c342bb2a-157e-4748-bf21-0926f95e5312
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 9592057757b7bad0c2400f8b1c720ef0146bb9a7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359199"
---
# <a name="pidtagreceivedrepresentingaddresstype-canonical-property"></a>PidTagReceivedRepresentingAddressType (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält den Adresstyp für den Messagingbenutzer, der durch den Benutzer dargestellt wird, der die Nachricht tatsächlich empfängt.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_RCVD_REPRESENTING_ADDRTYPE, PR_RCVD_REPRESENTING_ADDRTYPE_A, PR_RCVD_REPRESENTING_ADDRTYPE_W  <br/> |
|Kennung:  <br/> |0x0077  <br/> |
|Datentyp:  <br/> |PT_UNICODE, PT_STRING8  <br/> |
|Bereich:  <br/> |Adresse  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaften sind Beispiele für die Adresseigenschaften für den Messagingbenutzer, der vom empfangenden Benutzer dargestellt wird. Sie muss vom eingehenden Transportanbieter festgelegt werden, der auch für die Autorisierung oder Überprüfung der Stellvertretung zuständig ist. Wenn kein Messagingbenutzer dargestellt wird, sollte diese Eigenschaft auf den Adresstyp festgelegt werden, der in der **PR_RECEIVED_BY_ADDRTYPE** ([PidTagReceivedByAddressType](pidtagreceivedbyaddresstype-canonical-property.md)) -Eigenschaft enthalten ist.
  
Eine Clientanwendung, die auf eine Nachricht antwortet, die im Auftrag eines anderen Clients empfangen wurde, sollte diese Eigenschaft aus der empfangenen Nachricht in die **PR_SENT_REPRESENTING_ADDRTYPE** ([PidTagSentRepresentingAddressType](pidtagsentrepresentingaddresstype-canonical-property.md)) -Eigenschaft für die Antwort kopieren.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf Exchange Server Protokollspezifikationen.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge an, die für E-Mail-Nachrichtenobjekte zulässig sind.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Verarbeitet die Reihenfolge und den Fluss für Datenübertragungen zwischen einem Client und einem Server.
    
[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> Konvertiert zwischen IETF RFC2445, RFC2446 und RFC2447 sowie Termin- und Besprechungsobjekten.
    
[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)
  
> Gibt Methoden zum Verbinden und Konfigurieren von Postfächern als Stellvertretung sowie Interaktionen mit Nachrichten- und Kalenderobjekten an, wenn sie im Auftrag eines anderen Benutzers agieren.
    
[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Codiert und decodiert Nachrichten- und Anlagenobjekte in eine effiziente Streamdarstellung.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[PidTagAddressType (kanonische Eigenschaft)](pidtagaddresstype-canonical-property.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

