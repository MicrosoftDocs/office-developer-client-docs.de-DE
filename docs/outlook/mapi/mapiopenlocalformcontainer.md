---
title: MAPIOpenLocalFormContainer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MAPIOpenLocalFormContainer
api_type:
- COM
ms.assetid: 1c53170f-03a6-4a05-913e-de8eeadea692
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ace31079c51aac169f6091af0cb363e7f05f0d14
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427738"
---
# <a name="mapiopenlocalformcontainer"></a>MAPIOpenLocalFormContainer

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt einen Schnittstellenzeiger zur lokalen Formularbibliothek zurück. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiform.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen  <br/> |
   
```cpp
MAPIOpenLocalFormContainer(
  LPMAPIFORMCONTAINER FAR * ppfcnt
);
```

## <a name="parameters"></a>Parameter

 _ppfcnt_
  
> [out] Zeiger auf einen Zeiger auf die lokale Formularbibliotheksschnittstelle.
    
## <a name="return-value"></a>Return value

Keine.
  
## <a name="remarks"></a>Hinweise

Die Schnittstelle, an die ein Zeiger zurückgegeben wird, kann von Installationsprogrammen von Drittanbietern verwendet werden, um anwendungsspezifische Formulare in der Bibliothek zu installieren, ohne dass sich das Programm zuerst bei MAPI anmelden muss. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnMAPIOpenLocalFormContainer  <br/> |MFCMAPI verwendet die **MAPIOpenLocalFormContainer-Methode,** um den lokalen Formularcontainer zum Rendern in einem neuen Fenster zu öffnen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

