---
title: Aktualisieren von MAPI-Eigenschaften
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: faafde3d-3989-4182-91f1-a0cf0f1b5388
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 6c2c733b87b85971fad8060040e713b41b0f5616
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407522"
---
# <a name="updating-mapi-properties"></a>Aktualisieren von MAPI-Eigenschaften

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Clients und Dienstanbieter können einen Eigenschaftswert aktualisieren, indem sie:
  
- Die [IMAPIProp::SetProps-Methode](imapiprop-setprops.md) eines Objekts, um den Wert einer oder mehreren Eigenschaften eines Objekts zu aktualisieren. 
    
- Die [HrSetOneProp-Funktion,](hrsetoneprop.md) um immer nur eine Eigenschaft zu aktualisieren. Verwenden **Sie HrSetOneProp nur,** wenn das Zielobjekt lokal ist. Diese Funktion kann bei Verwendung mit Remoteobjekten zu Leistungsbeeinträchtigungen führen. 
    
Das folgende Verfahren veranschaulicht, wie **Sie SetProps** verwenden, um die Nachrichtenklasse oder PR_MESSAGE_CLASS_A ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) -Eigenschaft einer Nachricht zu aktualisieren. 
  
### <a name="to-update-the-message-class-of-a-message"></a>So aktualisieren Sie die Nachrichtenklasse einer Nachricht 
  
1. Ordnen Sie [eine SPropValue-Struktur](spropvalue.md) für die Nachrichtenklasse zu, und legen Sie ihre Member entsprechend. 
    
  ```cpp
    SPropValue spvMsgClass;
    spvMsgClass.ulPropTag = PR_MESSAGE_CLASS_A;
    spvMsgClass.Value.lpszA = "IPM.NewClass";
    
  ```

2. Rufen Sie die **IMAPIProp::SetProps-Methode** der Nachricht auf, um die neue Nachrichtenklasse zu festlegen. 
    
  ```cpp
    hRes = lpMessage->SetProps(1, (LPSPropValue) &spvMsgClass, NULL);
  ```

## <a name="see-also"></a>Siehe auch

- [Übersicht über die MAPI-Eigenschaft](mapi-property-overview.md)

