---
title: IOSTXSetSyncResult
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IOSTX.SetSyncResult
api_type:
- COM
ms.assetid: 7f083ee0-bf36-0059-1589-66e454fe0098
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 78ccf72f17ec350d77f2d22d0e6d2fa7c3d97543
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432870"
---
# <a name="iostxsetsyncresult"></a>IOSTX::SetSyncResult

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Legt das Ergebnis der Synchronisierung fest.
  
```cpp
HRESULT SetSyncResult( 
    HRESULT hrSync 
);
```

## <a name="parameters"></a>Parameter

 _hrSync_
  
>  [in] Das Ergebnis der Synchronisierung. 
    
## <a name="remarks"></a>Hinweise

Rufen **Sie IOSTX::SetSyncResult auf,** bevor **Sie IOSTX::SyncEnd** aufrufen, um den lokalen Speicher über das Ergebnis der Synchronisierung zu informieren. 
  
## <a name="see-also"></a>Siehe auch



[IOSTX::GetLastError](iostx-getlasterror.md)
  
[IOSTX::InitSync](iostx-initsync.md)
  
[IOSTX::SyncBeg](iostx-syncbeg.md)
  
[IOSTX::SyncEnd](iostx-syncend.md)
  
[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)
  
[IOSTX::SyncHdrEnd](iostx-synchdrend.md)


[MAPI-Konstanten](mapi-constants.md)

