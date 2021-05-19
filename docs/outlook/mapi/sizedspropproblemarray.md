---
title: SizedSPropProblemArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedSPropProblemArray
api_type:
- COM
ms.assetid: 2fc3febb-8c69-4315-a112-a28eee98013d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: b3818e5e1429c7e2b7d5f7533db733ba29e672c8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418113"
---
# <a name="sizedspropproblemarray"></a>SizedSPropProblemArray

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Erstellt eine benannte [SPropProblemArray-Struktur,](spropproblemarray.md) die eine angegebene Anzahl von [SPropProblem-Strukturen](spropproblem.md) enthält. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verwandte Struktur:  <br/> |**SPropProblemArray** <br/> |
   
```cpp
SizedSPropProblemArray(_cprob, _name)
```

## <a name="parameters"></a>Parameter

_ _cprob_
  
> Anzahl der **SPropProblem-Strukturen,** die in die neue Struktur eingeschlossen werden sollen. 
    
_ _name_
  
> Name für die neue Struktur.
    
## <a name="remarks"></a>Hinweise

Verwenden Sie **das SizeSPropProblemArray-Makro,** um ein Eigenschaftenproblemarray mit expliziten Grenzen zu erstellen. Führen Sie die folgende Gliederung aus, um die neue Struktur zu verwenden, die aus dem **Makro SizedSPropProblemArray** als Zeiger auf eine **SPropProblemArray-Struktur** resultiert: 
  
```cpp
lpPropProbArray = (LPSPropProblemArray) &SizedSPropProblemArray;
```

## <a name="see-also"></a>Siehe auch

- [SPropProblemArray](spropproblemarray.md)
- [SPropProblem](spropproblem.md)
- [Makros im Zusammenhang mit Strukturen](macros-related-to-structures.md)

