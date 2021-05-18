---
title: ISocialSessionLogon
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8b3c9a23-6378-4054-ad1c-193fc15c473c
description: Meldet sich mit dem angegebenen Benutzernamen und Kennwort am Standort des sozialen Netzwerks an.
ms.openlocfilehash: 7915097e456d6fafa713901f8074e6531bfaa001
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361040"
---
# <a name="isocialsessionlogon"></a>ISocialSession::Logon

Meldet sich mit dem angegebenen Benutzernamen und Kennwort am Standort des sozialen Netzwerks an.
  
```cpp
HRESULT _stdcall Logon([in] BSTR username, [in] BSTR password);
```

## <a name="parameters"></a>Parameter

_benutzername_
  
> [in] Eine Zeichenfolge, die den benutzernamen enthält, der sich anmelden soll.
    
_password_
  
> [in] Eine Zeichenfolge, die das kennwort für die Anmeldung enthält.
    
## <a name="see-also"></a>Siehe auch

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

