---
title: IPSTX2SetSpoolSuspendState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTX2.SetSpoolSuspendState
api_type:
- COM
ms.assetid: 396db029-1d4a-203d-2256-3353d03c6767
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: e988114e8e71ad1f80d20ab0d5a30c37425f5952
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407515"
---
# <a name="ipstx2setspoolsuspendstate"></a>IPSTX2::SetSpoolSuspendState

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Legt den angehaltenen Status für den Spooler fest.
  
```cpp
void SetSpoolSuspendState( 
    ULONG ulState 
);
```

## <a name="parameters"></a>Parameter

 _ulState_
  
> [in] Der Zustand, auf den der Spooler festgelegt werden soll. Dies muss einer der folgenden Werte sein:
    
 **SS_ACTIVE**
  
> 
    
 **SS_SUSPENDED**
  
> 
    
## <a name="see-also"></a>Siehe auch



[MAPI-Konstanten](mapi-constants.md)

