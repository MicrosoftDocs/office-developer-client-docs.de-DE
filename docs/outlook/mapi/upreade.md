---
title: UPREADE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d146ee74-0c3a-5fdd-b1aa-af6498550801
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 1df2c665f8e9d7a0bd6d47ec59b2adf706bead75
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434144"
---
# <a name="upreade"></a>UPREADE

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Erweiterte Informationen zum Hochladen des Lesestatus eines Elements während des [Status des Upload-Lesestatus](upload-read-status-state.md).
  
## <a name="quick-info"></a>QuickInfo

```cpp
struct UPREADE 
{ 
    ULONG ulFlags; 
    SKEY skey; 
};
```

## <a name="members"></a>Elemente

_ulFlags_
  
>  [out]/[in] Flags, um das entsprechende Verhalten während des Uploads zu bestimmen. 
    
  - UPR_ASSOC
    
    - [out] Element ist ausgeblendet.
    
  - UPR_READ
    
    - [out] Der Lesestatus des Elements wurde geändert.
    
  - UPR_OK
    
    - [in] Hochladen war erfolgreich. Der Client legt dies nach dem Hochladen von Informationen auf den Server fest.
    
  - UPR_COMMIT
    
    - [in] Hochladen den Lesestatus des Elements jetzt anstatt bis zum [](upload-table-state.md) Ende des Status der Uploadtabelle zu warten, um mehrere Elemente zu verarbeiten. 
    
_skey_
  
> [out] Quellschlüssel des Elements.
    
## <a name="see-also"></a>Siehe auch

- [Informationen über die Replikations-API](about-the-replication-api.md)
- [Informationen über den Replikationszustandsautomaten](about-the-replication-state-machine.md)
- [MAPI-Konstanten](mapi-constants.md)
- [UPREAD](upread.md)

