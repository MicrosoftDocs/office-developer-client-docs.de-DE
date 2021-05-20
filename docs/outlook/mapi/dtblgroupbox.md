---
title: DTBLGROUPBOX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLGROUPBOX
api_type:
- COM
ms.assetid: 5e444b62-d6b6-4cfc-8601-d34aa004c1e6
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 324cfe9d7c412b3bb0e3150b8eec51aaeb6a0e93
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438393"
---
# <a name="dtblgroupbox"></a>DTBLGROUPBOX

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beschreibt ein Gruppenfeldsteuerelement, das in einem Dialogfeld verwendet wird, das aus einer Anzeigetabelle erstellt wird.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verwandtes Makro:  <br/> |[SizedDtblGroupBox](sizeddtblgroupbox.md) <br/> |
   
```cpp
typedef struct _DTBLGROUPBOX
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
} DTBLGROUPBOX, FAR *LPDTBLGROUPBOX;

```

## <a name="members"></a>Elemente

 **ulbLpszLabel**
  
> Position im Arbeitsspeicher der Zeichenzeichenfolge, die das Gruppenfeld begleitet. Wenn sie angezeigt wird, wird die Beschriftung oben links im Feld angezeigt.
    
 **ulFlags**
  
> Bitmaske von Flags, die verwendet werden, um das Format der Bezeichnung zu bestimmen, auf das das **ulbLpszLabel-Element** verweist. Das folgende Flag kann festgelegt werden: 
    
MAPI_UNICODE 
  
> Die Bezeichnung ist im Unicode-Format. Wenn das MAPI_UNICODE nicht festgelegt ist, befindet sich die Bezeichnung im ANSI-Format.
    
## <a name="remarks"></a>Hinweise

Eine **DTBLGROUPBOX-Struktur** beschreibt ein Gruppenfeldsteuerelement, das zum visuellen Zuordnen anderer Steuerelemente im Dialogfeld verwendet wird. Die Hervorhebungstechnik umfasst das Um umgeben der anderen Steuerelemente durch ein Feld. 
  
Eine Übersicht über Anzeigetabellen finden Sie unter [Display Tables](display-tables.md). Informationen zum Implementieren einer Anzeigetabelle finden Sie unter [Implementieren einer Anzeigetabelle](display-table-implementation.md).
  
## <a name="see-also"></a>Siehe auch



[DTCTL](dtctl.md)


[MAPI-Strukturen](mapi-structures.md)

