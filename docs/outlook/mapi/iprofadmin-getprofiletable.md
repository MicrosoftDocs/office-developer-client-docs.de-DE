---
title: IProfAdminGetProfileTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.GetProfileTable
api_type:
- COM
ms.assetid: cebccd2d-8215-486e-9964-7fc42412cec6
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 2db7dba67e7b71df6921ecd97189255a0ef7823a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414645"
---
# <a name="iprofadmingetprofiletable"></a>IProfAdmin::GetProfileTable

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bietet Zugriff auf die Profiltabelle, eine Tabelle, die Informationen zu allen verfügbaren Profilen enthält.
  
```cpp
HRESULT GetProfileTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> [in] Immer NULL.
    
 _lppTable_
  
> [out] Ein Zeiger auf einen Zeiger auf die Profiltabelle.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Profiltabelle wurde erfolgreich abgerufen.
    
## <a name="remarks"></a>Hinweise

Die **IProfAdmin::GetProfileTable-Methode** bietet Zugriff auf die Profiltabelle, die für jedes verfügbare Profil eine Zeile enthält. Jede Zeile enthält nur zwei Spalten: den Anzeigenamen des Profils und ein Flag, das angibt, ob das Profil der Standard ist. 
  
Profile, die gelöscht wurden oder verwendet werden, aber zum Löschen markiert wurden, sind nicht in der Profiltabelle enthalten. Die Profiltabelle ist statisch. Nachfolgende Ergänzungen und Löschungen von Profilen werden nicht in der Tabelle widerspiegelt. 
  
Wenn keine Profile vorhanden sind, **gibt GetProfileTable** eine Tabelle mit null Zeilen zurück. 
  
Weitere Informationen zur Profiltabelle finden Sie unter [Profile Tables](profile-tables.md). 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnShowProfiles  <br/> |MFCMAPI verwendet die **IProfAdmin::GetProfileTable-Methode,** um die Profiltabelle in einem neuen Dialogfeld anzuzeigen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPITable : IUnknown](imapitableiunknown.md)
  
[MAPILogonEx](mapilogonex.md)
  
[IProfAdmin : IUnknown](iprofadminiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

