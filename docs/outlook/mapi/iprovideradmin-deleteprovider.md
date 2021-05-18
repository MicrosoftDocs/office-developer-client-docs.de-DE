---
title: IProviderAdminDeleteProvider
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProviderAdmin.DeleteProvider
api_type:
- COM
ms.assetid: 0065b50f-95f6-4af1-81c2-a73e5111eecf
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 28dbbb98c9810bb688b9ecdd730ef6c4ada5f60b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404862"
---
# <a name="iprovideradmindeleteprovider"></a>IProviderAdmin::DeleteProvider

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Löscht einen Dienstanbieter aus dem Nachrichtendienst.
  
```cpp
HRESULT DeleteProvider(
  LPMAPIUID lpUID
);
```

## <a name="parameters"></a>Parameter

 _lpUID_
  
> [in, out] Ein Zeiger auf die [MAPIUID-Struktur,](mapiuid.md) die den eindeutigen Bezeichner enthält, der den zu löschenden Anbieter darstellt. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Anbieter wurde erfolgreich aus dem Nachrichtendienst gelöscht.
    
MAPI_E_NOT_FOUND 
  
> Die **MAPIUID,** auf die der  _lpUID-Parameter_ verweist, wurde nicht erkannt. 
    
## <a name="remarks"></a>Hinweise

Die **IProviderAdmin::D eleteProvider-Methode** löscht einen Dienstanbieter aus dem Nachrichtendienst. **DeleteProvider** bestimmt den zu löschenden Dienstanbieter, indem die **MAPIUID-Struktur,** auf die  _von lpUID_ verwiesen wird, mit dem Satz von Bezeichnern, die von den aktiven Dienstanbietern registriert wurden, übereinstimmen. 
  
Die meisten Nachrichtendienste lassen das Löschen von Anbietern während der Verwendung des Profils nicht zu. Wenn der zu löschende Anbieter verwendet wird, markiert **DeleteProvider** ihn zum Löschen, anstatt ihn sofort zu entfernen, und gibt S_OK. Wenn der Anbieter nicht mehr verwendet wird, wird er gelöscht. 
  
 **DeleteProvider** ruft die Einstiegspunktfunktion des Nachrichtendiensts auf, bevor der Anbieter aus dem Dienst entfernt wird. Der  _ulContext-Parameter_ ist auf MSG_SERVICE_PROVIDER_DELETE. Die Einstiegspunktfunktion des Nachrichtendiensts führt die folgenden Aufgaben aus: 
  
- Löscht den Dienstanbieter.
    
- Löscht den Profilabschnitt des Dienstanbieters.
    
Die Einstiegspunktfunktion des Nachrichtendiensts wird nicht erneut aufgerufen, nachdem der Anbieter gelöscht wurde.
  
## <a name="see-also"></a>Siehe auch



[MAPIUID](mapiuid.md)
  
[MSGSERVICEENTRY](msgserviceentry.md)
  
[IProviderAdmin : IUnknown](iprovideradminiunknown.md)

