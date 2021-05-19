---
title: SizedDtblComboBox
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedDtblComboBox
api_type:
- COM
ms.assetid: 1e5ea9f2-1029-4584-845a-890d3e956036
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 8861c8f86eaab6defb270b673e0ee200446aedb3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416265"
---
# <a name="sizeddtblcombobox"></a>SizedDtblComboBox
 
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Erstellt eine benannte Struktur, die eine [DTBLCOMBOBOX-Struktur](dtblcombobox.md) zum Beschreiben eines Kombinationsfeldsteuerelements und die maximale Anzahl von Zeichen enthält, die in das zugeordnete Bearbeitungssteuerelement eingegeben werden können. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verwandte Struktur:  <br/> |**DTBLCOMBOBOX** <br/> |
   
```cpp
SizedDtblComboBox (n, u)
```

## <a name="parameters"></a>Parameter

_n_
  
> Die Anzahl der Zeichen, die im Bearbeitungssteuerelement des Kombinationsfelds eingegeben werden können. 
    
_u_
  
> Name für die neue Struktur.
    
## <a name="remarks"></a>Hinweise

Mit **dem Makro SizedDtblComboBox** können Sie ein Kombinationsfeld definieren, wenn die Länge der aktivierten Zeichenzeichenfolge bekannt ist. Die neue Struktur wird mit den folgenden Mitgliedern erstellt: 
  
```cpp
DTBLCOMBOBOX dtblcombobox;
TCHAR lpszCharsAllowed[n];

```

Führen Sie die folgende Gliederung aus, um einen Zeiger auf die resultierende Struktur des **SizedDtblComboBox-Makros** als **DTBLCOMBOBOX-Strukturzeiger** zu verwenden: 
  
```cpp
lpDtblComboBox = (LPDTBLCOMBOBOX) &SizedDtblComboBox;

```

## <a name="see-also"></a>Siehe auch

- [DTBLCOMBOBOX](dtblcombobox.md)
- [Makros im Zusammenhang mit Strukturen](macros-related-to-structures.md)

