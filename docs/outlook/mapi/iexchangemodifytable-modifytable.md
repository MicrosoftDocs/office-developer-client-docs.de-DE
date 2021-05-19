---
title: IExchangeModifyTableModifyTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IExchangeModifyTable.ModifyTable
api_type:
- COM
ms.assetid: b9a745cc-260d-4a1c-896e-6a038ab3cfb9
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 46bb9b2cc1a4d54807d6929b4e1439b58fb3a531
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418176"
---
# <a name="iexchangemodifytablemodifytable"></a>IExchangeModifyTable::ModifyTable

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Aktualisiert ein MAPI-Tabellenobjekt.
  
```cpp
HRESULT ModifyTable( 
  ULONG ulFlags, 
  LPROWLIST lpMods 
); 

```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> [in] Verwenden Sie einen der folgenden Werte: 
    
0 (Null)
  
> Verwenden Sie den Wert des **ulRowFlags-Mitglieds** der [ROWENTRY-Struktur.](rowentry.md) 
    
ACLTABLE_FREEBUSY
  
> Legt neue Rechte fest.
    
frightsFreeBusyDetailed
  
> Wenn ACLTABLE_FREEBUSY übergeben wird, wird eine detaillierte Anzeige der neuen Frei/Gebucht-Rechte angezeigt.
    
frightsFreeBusySimple
  
> Wenn ACLTABLE_FREEBUSY übergeben wird, wird eine einfache Anzeige neuer Frei/Gebucht-Rechte angezeigt.
    
ROWLIST_REPLACE
  
> Ersetzen Sie alle Zeilen in der Tabelle.
    
 _lpMods_
  
> [in] Zeigt auf eine [ROWLIST-Struktur,](rowlist.md) die die Eigenschaften für das Tabellenobjekt enthält. 
    
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|RulesDlg.cpp  <br/> |CRulesDlg::OnModifySelectedItem  <br/> |MFCMAPI verwendet die **IExchangeModifyTable::ModifyTable-Methode,** um eine geänderte Regel zurück in das Regelverzeichnis zu schreiben.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)
  
[ROWENTRY](rowentry.md)
  
[ROWLIST](rowlist.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

