---
title: PidTagRecipientNumberForAdvice (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecipientNumberForAdvice
api_type:
- COM
ms.assetid: 636c1e75-3024-43ca-a7dd-1bb480dfbb5b
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 79ef85955f15e0ca829ac6f206dddc17031b0562
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420640"
---
# <a name="pidtagrecipientnumberforadvice-canonical-property"></a>PidTagRecipientNumberForAdvice (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Diese Eigenschaft enthält die Telefonnummer eines Nachrichtenempfängers, um sich über die physische Zustellung einer Nachricht zu informieren.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_RECIPIENT_NUMBER_FOR_ADVICE, PR_RECIPIENT_NUMBER_FOR_ADVICE_A, PR_RECIPIENT_NUMBER_FOR_ADVICE_W  <br/> |
|Kennung:  <br/> |0x0C14  <br/> |
|Datentyp:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Bereich:  <br/> |MAPI-Empfänger  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaften sollen in Verbindung mit der Zustellung an ein physisches Ziel und nicht in einem elektronischen Postfach verwendet werden, wenn nicht erwartet wird, dass der menschliche Empfänger bei der Zustellung vorhanden ist. Ein Beispiel ist die Telefonnummer auf einem Faxdeckblatt.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

