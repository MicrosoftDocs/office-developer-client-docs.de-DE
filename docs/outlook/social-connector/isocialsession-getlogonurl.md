---
title: ISocialSessionGetLogonUrl
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d61bab07-acb3-433b-8783-c3fe110a5582
description: Ruft eine Zeichenfolge ab, die eine URL darstellt, die zum Präsentieren eines browserbasierten Formulars für den Benutzer während der Webauthentifizierung verwendet wird.
ms.openlocfilehash: 83867282922ea136b9673609cc2ba2f1a206f6ab
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427913"
---
# <a name="isocialsessiongetlogonurl"></a>ISocialSession::GetLogonUrl

Ruft eine Zeichenfolge ab, die eine URL darstellt, die zum Präsentieren eines browserbasierten Formulars für den Benutzer während der Webauthentifizierung verwendet wird.
  
```cpp
HRESULT _stdcall GetLogonUrl([out, retval] BSTR* url);
```

## <a name="parameters"></a>Parameter

_url_
  
> [out] Eine Zeichenfolge, die eine URL für das formular enthält, das in der Webauthentifizierung verwendet wird.
    
## <a name="remarks"></a>Hinweise

Nachdem das Formular dem Benutzer angezeigt wurde, wird die [ISocialSession::LogonWeb-Methode](isocialsession-logonweb.md) mit einer leeren Zeichenfolge für den  _connectIn-Parameter_ aufgerufen. 
  
## <a name="see-also"></a>Siehe auch

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

