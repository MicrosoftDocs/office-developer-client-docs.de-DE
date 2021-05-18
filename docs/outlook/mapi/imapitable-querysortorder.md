---
title: IMAPITableQuerySortOrder
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.QuerySortOrder
api_type:
- COM
ms.assetid: 7b4ca523-0703-417c-8586-c4324c200020
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 61991972fdf8674a9ffd2b790e26c7fa669df357
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407550"
---
# <a name="imapitablequerysortorder"></a>IMAPITable::QuerySortOrder

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ruft die aktuelle Sortierreihenfolge für eine Tabelle ab.
  
```cpp
HRESULT QuerySortOrder(
LPSSortOrderSet FAR * lppSortCriteria
);
```

## <a name="parameters"></a>Parameter

 _lppSortCriteria_
  
> [out] Zeiger auf einen Zeiger auf die [SSortOrderSet-Struktur](ssortorderset.md) mit der aktuellen Sortierreihenfolge. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die aktuelle Sortierreihenfolge wurde erfolgreich zurückgegeben.
    
MAPI_E_BUSY 
  
> Ein weiterer Vorgang wird ausgeführt, der verhindert, dass der Sortierreihenfolgenabrufvorgang gestartet wird. Der ausgeführte Vorgang sollte entweder abgeschlossen oder beendet werden.
    
## <a name="remarks"></a>Hinweise

Die **IMAPITable::QuerySortOrder-Methode** ruft die aktuelle Sortierreihenfolge für eine Tabelle ab. Sortierreihenfolgen werden mit einer [SSortOrderSet-Struktur](ssortorderset.md) beschrieben. 
  
- Das **cSorts-Element** der **SSortOrderSet-Struktur** kann auf Null festgelegt werden, wenn: 
    
- Die Tabelle ist unsortiert.
    
- Es gibt keine Informationen zur Sortierung der Tabelle.
    
- Die **SSortOrderSet-Struktur** ist nicht geeignet, um die Sortierreihenfolge zu beschreiben. 
    
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Wenn sie ihre [IMAPITable::SortTable-Methode](imapitable-sorttable.md) mit einer **SSortOrderSet-Struktur** aufruft, die keine Spalten im Sortierschlüssel enthält, entfernen Sie die aktuelle Sortierreihenfolge, und wenden Sie die Standardreihenfolge an, falls eine solche besteht. Bei nachfolgenden Aufrufen von **QuerySortOrder** können Sie auswählen, ob null oder mehr Spalten für den Sortierschlüssel zurückgegeben werden sollen. Sie können mehr Spalten als in der aktuellen Ansicht zurückgeben.
  
Weitere Informationen zum Sortieren finden Sie unter [Sorting and Categorization](sorting-and-categorization.md).
  
## <a name="see-also"></a>Siehe auch



[IMAPITable::SortTable](imapitable-sorttable.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SSortOrderSet](ssortorderset.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

