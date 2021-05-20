---
title: IDistList IMAPIContainer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IDistList
api_type:
- COM
ms.assetid: bd8e1ddb-3027-428b-8964-81614f80282d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 463d81a6692b6071cada0ad22e7343020563e41c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431547"
---
# <a name="idistlist--imapicontainer"></a>IDistList : IMAPIContainer

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bietet Zugriff auf Verteilerlisten in veränderbaren Adressbuchcontainern. **IDistList** kann Verteilerlisten zusätzlich zur Namensauflösung erstellen, kopieren und löschen. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verf�gbar gemacht von:  <br/> |Verteilerlistenobjekte  <br/> |
|Implementiert von:  <br/> |Adressbuchanbieter  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IDistList  <br/> |
|Zeigertyp:  <br/> |LPDISTLIST  <br/> |
|Transaktionsmodell:  <br/> |Transacted  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

Diese Schnittstelle verfügt nicht über eindeutige Methoden.
  
|**Erforderliche Eigenschaften**|**Access**|
|:-----|:-----|
|**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))  <br/> |Lesen/Schreiben  <br/> |
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |Lesen/Schreiben  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
|**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
   
## <a name="remarks"></a>Hinweise

Die **IDistList-Schnittstelle** erbt von [IMAPIContainer](imapicontainerimapiprop.md) und enthält dieselben Methoden wie Adressbuchcontainer. Da die Methoden der **IDistList-Schnittstelle** mit denen der [IABContainer-Schnittstelle](iabcontainerimapicontainer.md) identisch sind, werden sie hier nicht dupliziert. 
  
Eine Verteilerliste oder ein Objekt, das **IDistList** implementiert, ist eine Sammlung von Messagingbenutzerobjekten oder einzelnen Empfängern. Eine Verteilerliste kann aus allen Messagingbenutzerobjekten oder einem Messagingbenutzer und einigen Verteilerlisten bestehen. 
  
In der Regel gibt es zwei Arten von Verteilerlisten:
  
- Verteilerlisten, die vom zugrunde liegenden Messagingsystem erweitert werden. Dieser Listentyp hat eine Adresse, **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)), und wird genauso behandelt wie ein einzelner Empfänger. 
    
- Verteilerlisten, die in einem lokalen Container vorhanden sind und von der Clientanwendung erweitert werden.
    
Optionale Eigenschaften der Verteilerliste umfassen Folgendes:
  
- **PR_LAST_MODIFICATION_TIME** ([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))
    
- **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) 
    
- **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) 
    
Beachten **Sie, PR_ADDRTYPE** erforderlich ist, **aber PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) nicht. Das liegt daran, dass eine Verteilerliste ohne E-Mail-Adresse weiterhin Nachrichten empfangen kann, die Mitgliederliste muss jedoch erweitert werden. Wenn die **PR_ADDRTYPE** auf MAPIPDL festgelegt ist, führt MAPI die Erweiterung aus. Wenn **PR_ADDRTYPE** ein anderer Wert als MAPIPDL ist, führt der Transportanbieter die Erweiterung aus. 
  
Weitere Informationen zur Verwendung der **IDistList-Methoden** finden Sie in den Referenzeinträgen für die parallelen Methoden von **IABContainer**.
  
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

