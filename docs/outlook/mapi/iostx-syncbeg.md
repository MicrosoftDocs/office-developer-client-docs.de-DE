---
title: IOSTXSyncBeg
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IOSTX.SyncBeg
api_type:
- COM
ms.assetid: 4a935df3-98c4-2742-206e-4e16eda7b9bc
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: ae4497295328155780fc5208d1699169698e02d8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411939"
---
# <a name="iostxsyncbeg"></a>IOSTX::SyncBeg

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bereitet den lokalen Speicher für die Synchronisierung in einem bestimmten Zustand vor und ruft die erforderlichen Informationen zum Replizieren ab.
  
```cpp
HRESULT SyncBeg( 
    UINT uiSync, 
    LPVOID *ppv 
);
```

## <a name="parameters"></a>Parameter

 _uiSync_
  
>  [in] Der Zustand, in den der lokale Speicher einwahlt. Nachfolgend finden Sie eine Liste der Zustandsidentiferen: 
    
LR_SYNC_IDLE
  
> 
    
LR_SYNC
  
> 
    
LR_SYNC_UPLOAD_HIERARCHY
  
> 
    
LR_SYNC_UPLOAD_FOLDER
  
> 
    
LR_SYNC_CONTENTS
  
> 
    
LR_SYNC_UPLOAD_TABLE
  
> 
    
LR_SYNC_UPLOAD_MESSAGE
  
> 
    
LR_SYNC_UPLOAD_MESSAGE_READ
  
> 
    
LR_SYNC_UPLOAD_MESSAGE_DEL
  
> 
    
LR_SYNC_DOWNLOAD_HIERARCHY
  
> 
    
LR_SYNC_DOWNLOAD_TABLE
  
> 
    
 _ppv_
  
>  [in]/[out] Zeiger auf die Datenstruktur, die dem zu gebende Zustand entspricht. 
    
[DNHIER](dnhier.md)
  
> 
    
[DNTBL](dntbl.md)
  
> 
    
[DNTBL](dntbl.md)
  
> 
    
[SYNC](sync.md)
  
> 
    
[SYNCCONT](synccont.md)
  
> 
    
[UPDEL](updel.md)
  
> 
    
[UPDELE](updele.md)
  
> 
    
[UPFLD](upfld.md)
  
> 
    
[UPHIER](uphier.md)
  
> 
    
[UPMOV](upmov.md)
  
> 
    
[UPMSG](upmsg.md)
  
> 
    
[UPREAD](upread.md)
  
> 
    
[UPREADE](upreade.md)
  
> 
    
[UPTBL](uptbl.md)
  
> 
    
[UPTBLE](uptble.md)
  
> 
    
## <a name="remarks"></a>Hinweise

Der Client ruft **[IOSTX::SetSyncResult](iostx-setsyncresult.md)** auf, um das Ergebnis der Synchronisierung zu festlegen, und ruft **[dann IOSTX::SyncEnd](iostx-syncend.md)** auf, um den Status zu beenden. Der Client muss **[IOSTX::SyncEnd](iostx-syncend.md)** für jeden Aufruf von **IOSTX::SyncBeg** aufrufen, um zu ermitteln, ob der Status erfolgreich repliziert wurde. Nachdem dies ermittelt wurde, kann Outlook damit beginnen, den internen Zustand zu bereinigen. 
  
Die meisten dieser Strukturen enthalten [out]/[in]-Informationen, sodass Outlook Informationen an den Client und den Client an Outlook übergeben kann. Wenn der Client **IOSTX::SyncBeg** aufruft, ordnet Outlook die Datenstruktur für einen bestimmten Zustand zu und initialisiert sie mit Informationen für diesen Zustand. Dies sind die [out]-Informationen. In einem Zustand aktualisiert der Client die entsprechende Datenstruktur für den betreffenden Zustand. Dies sind die [in]-Informationen. 
  
## <a name="see-also"></a>Siehe auch



[IOSTX::GetLastError](iostx-getlasterror.md)
  
[IOSTX::InitSync](iostx-initsync.md)
  
[IOSTX::SetSyncResult](iostx-setsyncresult.md)
  
[IOSTX::SyncEnd](iostx-syncend.md)
  
[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)
  
[IOSTX::SyncHdrEnd](iostx-synchdrend.md)
  
[IOSTX : IUnknown](iostxiunknown.md)


[MAPI-Konstanten](mapi-constants.md)

