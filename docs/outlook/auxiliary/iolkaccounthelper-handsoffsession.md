---
title: IOlkAccountHelperHandsOffSession
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9f71fdef-5df5-0892-b64c-293a2f22f5c3
description: Gibt das MAPI-Sitzungsobjekt frei, das von IOlkAccountHelper::GetMapiSession zurückgegeben wurde.
ms.openlocfilehash: c481cee1ecb8c2bd3997cdee8ae86c9c3b5a712e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418631"
---
# <a name="iolkaccounthelperhandsoffsession"></a>IOlkAccountHelper::HandsOffSession

Gibt das MAPI-Sitzungsobjekt frei, das von - [IOlkAccountHelper::GetMapiSession zurückgegeben wurde.](iolkaccounthelper-getmapisession.md)
  
## <a name="quick-info"></a>QuickInfo

Siehe [IOlkAccountHelper](iolkaccounthelper.md).
  
```cpp
HRESULT IOlkAccountHelper::HandsOffSession( );
```

## <a name="return-values"></a>Rückgabewerte

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |Wenn Ihre Implementierung von **IOlkAccountHelper** eine eigene MAPI-Sitzung erstellt, die in **IOlkAccountHelper::GetMapiSession** zurückgegeben wird, müssen Sie die Sitzung hier veröffentlichen und S_OK.  <br/> |
|E_NOTIMPL  <br/> |Wenn Ihre Implementierung von **IOlkAccountHelper** keine eigene MAPI-Sitzung erstellt hat, müssen Sie nur eine E_NOTIMPL. In diesem Fall ist dies der einzige unterstützte Rückgabewert.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Konstanten (Account Management API)](constants-account-management-api.md)  
- [IOlkAccountHelper::GetMapiSession](iolkaccounthelper-getmapisession.md)

