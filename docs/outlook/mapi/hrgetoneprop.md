---
title: HrGetOneProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- HrGetOneProp
api_type:
- HeaderDef
ms.assetid: 8d0a381a-e714-4663-9a57-b0e1cdbd6ba7
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e5adc7d0c317d8b803645d78227777998d7d241f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416055"
---
# <a name="hrgetoneprop"></a>HrGetOneProp

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ruft den Wert einer einzelnen Eigenschaft von einer Eigenschaftenschnittstelle ab, d. h. einer Schnittstelle, die von [IMAPIProp abgeleitet ist.](imapipropiunknown.md) 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und Dienstanbieter  <br/> |
   
```cpp
HrGetOneProp(
  LPMAPIPROP pmp,
  ULONG ulPropTag,
  LPSPropValue FAR * ppprop
);
```

## <a name="parameters"></a>Parameter

 _pmp_
  
> [in] Zeiger auf die [IMAPIProp-Schnittstelle,](imapipropiunknown.md) von der der Eigenschaftswert abgerufen werden soll. 
    
 _ulPropTag_
  
> [in] Eigenschaftstag der abzurufende Eigenschaft. 
    
 _ppprop_
  
> [out] Zeiger auf einen Zeiger auf die [zurückgegebene SPropValue-Struktur,](spropvalue.md) die den abgerufenen Eigenschaftswert definiert. 
    
## <a name="return-value"></a>Rückgabewert

MAPI_E_NOT_FOUND 
  
> Die angeforderte Eigenschaft ist nicht über die angegebene Schnittstelle verfügbar.
    
## <a name="remarks"></a>Hinweise

Im Gegensatz zur [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) gibt die **HrGetOneProp-Funktion** nie eine Warnung zurück. Da nur eine Eigenschaft abgerufen wird, ist sie einfach erfolgreich oder schlägt fehl. Zum Abrufen mehrerer Eigenschaften ist **GetProps** schneller. 
  
Sie können eine einzelne Eigenschaft mit der [HrSetOneProp-Funktion](hrsetoneprop.md) festlegen oder ändern. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |GetMAPIObjectType  <br/> |MFCMAPI verwendet die **HrGetOneProp-Methode,** um den Typ eines Objekts abzurufen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

