---
title: ISocialProviderSocialNetworkName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 96f32db2-d654-4e72-88d1-ef955e3ff42b
description: Gibt eine Zeichenfolge zurück, die den Namen des sozialen Netzwerks darstellt.
ms.openlocfilehash: 5a6240fa6e609eec8498456fe56c83a761fadab0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406878"
---
# <a name="isocialprovidersocialnetworkname"></a>ISocialProvider::SocialNetworkName

Gibt eine Zeichenfolge zurück, die den Namen des sozialen Netzwerks darstellt. 
  
```cpp
[propget] HRESULT _stdcall SocialNetworkName([out, retval] BSTR* networkName);
```

## <a name="property-value"></a>Eigenschaftswert

Eine Zeichenfolge, die den Namen des sozialen Netzwerks enthält.
  
## <a name="remarks"></a>Hinweise

Outlook Anbieter von Social Connector (OSC) sollten den Namen des sozialen Netzwerks lokalisieren.
  
## <a name="see-also"></a>Siehe auch

- [ISocialProvider : IUnknown](isocialprovideriunknown.md)

