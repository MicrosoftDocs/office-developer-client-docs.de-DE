---
title: SOrRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SOrRestriction
api_type:
- COM
ms.assetid: 6fee29ce-9a34-4e0c-bb71-03120c3f1117
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 9b4ca4628f356142eb5303c064e3916474810fda
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437931"
---
# <a name="sorrestriction"></a>SOrRestriction

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beschreibt eine **OR-Einschränkung,** die zum Anwenden eines logischen **OR-Vorgangs** auf eine Einschränkung verwendet wird. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SOrRestriction
{
  ULONG cRes;
  LPSRestriction lpRes;
} SOrRestriction;

```

## <a name="members"></a>Elemente

 **cRes**
  
> Anzahl der Strukturen im Array, auf die das **lpRes-Element** verweist. 
    
 **lpRes**
  
> Zeiger auf die [SRestriction-Struktur,](srestriction.md) die die Einschränkung beschreibt, die mithilfe des logischen OR-Vorgangs **verbunden werden** soll. 
    
## <a name="remarks"></a>Hinweise

Weitere Informationen zur **SOrRestriction-Struktur** finden Sie unter [Informationen zu Einschränkungen](about-restrictions.md). 
  
## <a name="see-also"></a>Siehe auch



[SRestriction](srestriction.md)


[MAPI-Strukturen](mapi-structures.md)

