---
title: BOOKMARK
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.BOOKMARK
api_type:
- COM
ms.assetid: 678bdc52-3404-48b2-9154-64ce2a941555
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 069cb41ceac70a2eaaa08440e43745605890f071
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418134"
---
# <a name="bookmark"></a>BOOKMARK

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Definiert Lesezeichendaten zum Speichern einer Position in einer Tabelle. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verwandte Methoden:  <br/> |[IMAPITable::CreateBookmark](imapitable-createbookmark.md)[IMAPITable::FreeBookmark](imapitable-freebookmark.md) <br/> |
   
```cpp
typedef ULONG_PTR BOOKMARK;
```

## <a name="remarks"></a>Hinweise

MAPI definiert drei Lesezeichen, die wie folgt aufgeführt sind:
  
BOOKMARK_BEGINNING 
  
> Erinnert sich an die Anfangsposition der Tabelle. 
    
BOOKMARK_CURRENT 
  
> Erinnert sich an die aktuelle Position der Tabelle.
    
BOOKMARK_END 
  
> Erinnert sich an die Endposition der Tabelle.
    
Clients können andere Lesezeichen zum Merken anderer Tabellenpositionen erstellen. Lesezeichen sind nur gültig, wenn die Tabelle geöffnet ist. Clients müssen alle Lesezeichen frei, die sie erstellt haben, bevor sie die zugeordnete Tabelle schließen. 
  
## <a name="see-also"></a>Siehe auch



[IMAPITable::CreateBookmark](imapitable-createbookmark.md)
  
[IMAPITable::FindRow](imapitable-findrow.md)
  
[IMAPITable::FreeBookmark](imapitable-freebookmark.md)
  
[IMAPITable::SeekRow](imapitable-seekrow.md)


[MAPI-Datentypen](mapi-data-types.md)

