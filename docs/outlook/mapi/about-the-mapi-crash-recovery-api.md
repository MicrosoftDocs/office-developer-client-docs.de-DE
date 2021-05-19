---
title: Informationen über die API zur MAPI-Wiederherstellung nach einem Absturz
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: bc1e1f55-1959-a4a9-a24d-f006af531c9a
description: 'Letzte �nderung: Montag, 25. Juni 2012'
ms.openlocfilehash: 1acca6d806c1734007ac7c5e41059d3a870dc5bb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420262"
---
# <a name="about-the-mapi-crash-recovery-api"></a>Informationen über die API zur MAPI-Wiederherstellung nach einem Absturz

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die MAPI Crash Recovery-API überprüft den Status des freigegebenen Arbeitsspeichers für persönliche Ordner (PST) oder Offlineordner (OST), um sicherzustellen, dass sich die Daten in einem konsistenten Zustand befinden. Wenn sie sich in einem konsistenten Zustand befindet, verschiebt die [MAPICrashRecovery-Funktion](mapicrashrecovery.md) die Daten aus den geöffneten PSTs oder OSTs auf den Datenträger und sperrt die PSTs oder OSTs und lässt keinen Lese- oder Schreibzugriff auf die Daten zu. Dadurch wird sichergestellt, dass die Daten in einem konsistenten Zustand bleiben, bis der Prozess beendet wird. Indem Sie sicherstellen, dass sich die PSTs oder OSTs in einem konsistenten Zustand befinden, bevor der Prozess beendet wird, können Sie verhindern, dass Microsoft Outlook 2013 und Microsoft Outlook 2010 die folgende Fehlermeldung anzeigen und Leistungsprobleme vermeiden. 
  
 **Eine Datendatei wurde bei der letzten Verwendung nicht ordnungsgemäß geschlossen und wird auf Probleme überprüft. Die Leistung kann während der Überprüfung beeinträchtigt werden.**
  
Diese API bietet Folgendes:
  
Konstanten:
  
- [MAPI-Konstanten](mapi-constants.md)
    
Funktionen:
  
- [MAPICrashRecovery](mapicrashrecovery.md)
    
## <a name="see-also"></a>Siehe auch



[Verwenden der API zur MAPI-Wiederherstellung nach einem Absturz](how-to-use-the-mapi-crash-recovery-api.md)

