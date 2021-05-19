---
title: IAddrBookGetPAB
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.GetPAB
api_type:
- COM
ms.assetid: 9830e09c-700f-469b-a54d-4e4e0583aa84
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 6c565c088fd4ef7d5df141bf770c560f79535998
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419898"
---
# <a name="iaddrbookgetpab"></a>IAddrBook::GetPAB

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt den Eintragsbezeichner des Containers zurück, der als persönliches Adressbuch (PAB) festgelegt ist.
  
```cpp
HRESULT GetPAB(
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a>Parameter

 _lpcbEntryID_
  
> [out] Ein Zeiger auf die Byteanzahl in der Eintrags-ID, auf die der  _lppEntryID-Parameter_ verweist. 
    
 _lppEntryID_
  
> [out] Ein Zeiger auf einen Zeiger auf den Eintragsbezeichner des PAB. Der  _lppEntryID-Parameter_ enthält Null, wenn kein Container als PAB festgelegt wurde. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Eintragsbezeichner des PAB wurde erfolgreich zurückgegeben.
    
## <a name="remarks"></a>Hinweise

Clients rufen die **GetPAB-Methode** auf, um die Eintrags-ID des Containers abzurufen, der als PAB festgelegt ist. Wenn kein PAB im Profil eingerichtet wurde, wählt MAPI als PAB den ersten Container in der Adressbuchhierarchie aus, der Änderungen zulässt. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnOpenPAB  <br/> |MFCMAPI verwendet die **GetPAB-Methode,** um die ID für das persönliche Adressbuch des Benutzers zu erhalten.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[PidTagContainerFlags (kanonische Eigenschaft)](pidtagcontainerflags-canonical-property.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

