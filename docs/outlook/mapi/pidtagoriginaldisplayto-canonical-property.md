---
title: PidTagOriginalDisplayTo (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalDisplayTo
api_type:
- COM
ms.assetid: 8c1cf14c-0339-4ced-8f68-4bfaa1e4d3e9
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 5a2f60051e5cb0717926a5c3e2f878a49919b04c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342701"
---
# <a name="pidtagoriginaldisplayto-canonical-property"></a>PidTagOriginalDisplayTo (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält die Anzeigenamen der primären Empfänger (An) der ursprünglichen Nachricht.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_ORIGINAL_DISPLAY_TO, PR_ORIGINAL_DISPLAY_TO_A, PR_ORIGINAL_DISPLAY_TO_W  <br/> |
|Kennung:  <br/> |0x0074  <br/> |
|Datentyp:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Bereich:  <br/> |Allgemeines Messaging  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaften enthalten eine DURCH Semikolons getrennte ASCII-Liste. Sie wird von MAPI eingerichtet und direkt aus **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)) kopiert, wenn ein Zustellungs- oder Nichtablagebericht oder ein Lese- oder Ungelesenbericht generiert wird. Diese Eigenschaft kann für andere Nachrichten vorhanden sein, wie durch ihre Nachrichtenklassen definiert.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf Exchange Server Protokollspezifikationen.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge an, die für E-Mail-Nachrichtenobjekte zulässig sind.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

