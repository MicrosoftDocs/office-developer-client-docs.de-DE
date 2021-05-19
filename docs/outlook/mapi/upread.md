---
title: UPREAD
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 568f2336-cb4d-3f2c-a304-d29cdb0bcbcc
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 7338edc13227e303ec5fa47da4a5d9ee611c6749
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419884"
---
# <a name="upread"></a>UPREAD

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Informationen zum Hochladen des Lesestatus von Elementen während des [Status des Upload-Lesestatus](upload-read-status-state.md).
  
## <a name="quick-info"></a>QuickInfo

```cpp
struct UPREAD 
{ 
    PUPREADE pupre; 
    UINT cEnt; 
};
```

## <a name="members"></a>Elemente

 _pupre_
  
>  [out] Vektor von **[UPREADE-Einträgen.](upreade.md)** 
    
 _cEnt_
  
>  [out] Anzahl **der UPREADE-Einträge.** 
    
## <a name="see-also"></a>Siehe auch



[Informationen über die Replikations-API](about-the-replication-api.md)
  
[Informationen über den Replikationszustandsautomaten](about-the-replication-state-machine.md)
  
[MAPI-Konstanten](mapi-constants.md)
  
[UPREADE](upreade.md)

