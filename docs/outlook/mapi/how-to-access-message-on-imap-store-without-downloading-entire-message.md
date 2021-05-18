---
title: Zugreifen auf eine Nachricht in einem IMAP-Speicher, ohne die gesamte Nachricht herunterzuladen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 2a93ab3e-798f-5741-d5e0-bba8c6b437c7
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 194131148cc36dfff791b4cfae01862e8bbef5cb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299076"
---
# <a name="access-a-message-on-an-imap-store-without-downloading-the-entire-message"></a>Zugreifen auf eine Nachricht in einem IMAP-Speicher, ohne die gesamte Nachricht herunterzuladen

**Gilt für**: Outlook 2013 | Outlook 2016 
  
In diesem Thema wird ein Codebeispiel in C++ gezeigt, das einen Nachrichtenspeicher für die **[IProxyStoreObject-Schnittstelle](iproxystoreobject.md)** abfragt und den zurückgegebenen Zeiger und die **[IProxyStoreObject::UnwrapNoRef-Funktion](iproxystoreobject-unwrapnoref.md)** verwendet, um einen Zeiger auf ein imAP-Speicherobjekt abzurufen, das entpackt wurde. Die Verwendung dieses nicht ausgepackten Speichers ermöglicht den Zugriff auf eine Nachricht im aktuellen Status, ohne einen Download der gesamten Nachricht aufrufen zu müssen. 
  
Da **UnwrapNoRef** die Referenzanzahl für diesen neuen Zeiger nicht auf das nicht mehr ausgepackte Speicherobjekt erhöht, müssen Sie nach dem erfolgreichen Aufruf von **UnwrapNoRef** [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) aufrufen, um die Referenzanzahl zu verwalten. 
  
```cpp
HRESULT HrUnWrapMDB(LPMDB lpMDBIn, LPMDB* lppMDBOut) 
{ 
    HRESULT hRes = S_OK; 
    IProxyStoreObject* lpProxyObj = NULL; 
    LPMDB lpUnwrappedMDB = NULL; 
    hRes = lpMDBIn->QueryInterface(IID_IProxyStoreObject,(void**)&lpProxyObj); 
    if (SUCCEEDED(hRes) && lpProxyObj) 
    { 
        hRes = lpProxyObj->UnwrapNoRef((LPVOID*)&lpUnwrappedMDB); 
        if (SUCCEEDED(hRes) && lpUnwrappedMDB) 
        { 
            // UnwrapNoRef doesn't addref, so do it here 
            lpUnwrappedMDB->AddRef(); 
            (*lppMDBOut) = lpUnwrappedMDB; 
        } 
    } 
    if (lpProxyObj) lpProxyObj->Release(); 
    return hRes; 
}
```


