---
title: UPTBLE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f7fcb385-186d-d5fe-7104-fe0af09d5768
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: d0b440f01aad7078ed76cd37d36c5ad506215438
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413840"
---
# <a name="uptble"></a>UPTBLE

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Erweiterte Informationen zum Hochladen des Inhalts eines Ordners während des [Status der Uploadtabelle](upload-table-state.md).
  
## <a name="quick-info"></a>QuickInfo

```cpp
struct UPTBLE 
{ 
    UINTiEntMod; 
    UINTcEntMod; 
    UINTiEntRead; 
    UINTcEntRead; 
    UINTiEntDel; 
    UINTcEntDel; 
};
```

## <a name="members"></a>Elemente

 _iEntMod_
  
>  [out] Index, um das Hochladen der  _cEntMod-Anzahl neuer_ oder geänderter Elemente nachzuverfolgen. 
    
 _cEntMod_
  
>  [out] Anzahl der neuen oder geänderten Elemente im Ordner. 
    
 _iEntRead_
  
>  [out] Index zum Nachverfolgen des Hochladens der Anzahl _der cEntRead-Leseelemente._ 
    
 _cEntRead_
  
>  [out] Anzahl der Leseelemente im Ordner. 
    
 _iEntDel_
  
>  [out] Index zum Nachverfolgen des Hochladens der Anzahl _gelöschter cEntDel-Elemente._ 
    
 _cEntDel_
  
>  [out] Die Anzahl der gelöschten Elemente im Ordner. 
    
## <a name="see-also"></a>Siehe auch

- [Informationen über die Replikations-API](about-the-replication-api.md) 
- [Informationen über den Replikationszustandsautomaten](about-the-replication-state-machine.md)
- [UPTBL](uptbl.md)

