---
title: FtMulDw
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FtMulDw
api_type:
- COM
ms.assetid: e135ba67-97be-4ce0-a72e-93c49ed7d6e2
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 27ec919d720e1089d6e102f20485d936c9dc9808
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406346"
---
# <a name="ftmuldw"></a>FtMulDw

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Multipliziert eine nicht signierte ganzzahlige 64-Bit-Zahl mit einer nicht signierten 32-Bit-Ganzzahl.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und Dienstanbieter  <br/> |
   
```cpp
FILETIME FtMulDw(
  DWORD Multiplier,
  FILETIME Multiplicand
);
```

## <a name="parameters"></a>Parameter

 _Multiplikator_
  
> [in] Ein Doppelwort, das den nicht signierten 32-Bit-Ganzzahlmultiplikator enthält. 
    
 _Multiplikation_
  
> [in] Eine [FILETIME-Struktur,](filetime.md) die die nicht signierte ganzzahlige 64-Bit-Zahl enthält, die mit dem Wert im  _Multiplikatorparameter multipliziert werden_ soll. 
    
## <a name="return-value"></a>Rückgabewert

Die **FtMulDw-Funktion** gibt eine **FILETIME-Struktur** zurück, die das Produkt der beiden ganzen Zahlen enthält. Die beiden Eingabeparameter bleiben unverändert. 
  

