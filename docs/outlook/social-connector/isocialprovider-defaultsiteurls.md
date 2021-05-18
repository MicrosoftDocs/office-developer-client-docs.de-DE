---
title: ISocialProviderDefaultSiteUrls
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 322ea2e9-d6c9-48f9-a927-7162346d16a4
description: Gibt ein Array von Zeichenfolgen zurück, die Website-URLs für den anbieter Outlook Social Connector (OSC) angeben.
ms.openlocfilehash: 34d779d5eb42b81a14c5236685104e9ef4fe36f2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413773"
---
# <a name="isocialproviderdefaultsiteurls"></a>ISocialProvider::DefaultSiteUrls

Gibt ein Array von Zeichenfolgen zurück, die Website-URLs für den anbieter Outlook Social Connector (OSC) angeben.
  
```cpp
[propget] HRESULT _stdcall DefaultSiteUrls([out, retval] SAFEARRAY(BSTR)* siteUrls);
```

## <a name="property-value"></a>Eigenschaftswert

Ein Zeiger auf eine Struktur, die ein Array von Zeichenfolgen angibt, die Website-URLs für den OSC-Anbieter darstellen.
  
## <a name="remarks"></a>Hinweise

Ein Anbieter kann mehrere Website-URLs unterstützen. Das OSC legt die [ISocialSession::SiteUrl-Eigenschaft](isocialsession-siteurl.md) fest, um den Anbieter über die ausgewählte Website-URL zu informieren. 
  
Das OSC verwendet das erste Element des Arrays als Standardwebsite-URL. Ein Anbieter kann zusätzliche Elemente im Website-URL-Array zurückgeben, die vom OSC jedoch nicht verwendet werden. 
  
## <a name="see-also"></a>Siehe auch

- [ISocialProvider : IUnknown](isocialprovideriunknown.md)

