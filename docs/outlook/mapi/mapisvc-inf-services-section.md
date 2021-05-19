---
title: MapiSvc.inf [Services] Section
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 99f8e623-3138-4def-9778-5580326111a5
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: e5bf5242ef673976ebda928d6ce4862e3e7dd072
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434781"
---
# <a name="mapisvcinf-services-section"></a>MapiSvc.inf [Services] Section

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Im **Abschnitt [Dienste]** werden die Nachrichtendienste aufgeführt, die auf einem Computer installiert sind. Einträge in diesem Abschnitt verwenden das folgende Format: 
  
 **[Services]**
  
 _Name des Message-Service-Abschnitts_  =   _Name des Nachrichtendiensts_
  
Der Name des Nachrichtendienstabschnitts ist eine vom Nachrichtendienst definierte Zeichenfolge, die diesen Eintrag mit einem entsprechenden Abschnitt für den Dienst an anderer Stelle in mapisvc.inf verknüpft. Der Name des Nachrichtendiensts ist der Name des installierten Diensts. Im folgenden Abschnitt werden drei Nachrichtendienste gezeigt: das Standard-Adressbuch, mein eigener Dienst und der Nachrichtendienst Store Dienst. Diese Dienste sind nur zur Veranschaulichung fiktional. Jeder Nachrichtendienst implementer würde den entsprechenden Eintrag für seinen Nachrichtendienst in diesem Abschnitt ersetzen.
  
```cpp
[Services]
AB=Default Address Book
MsgService=My Own Service
MS=Message Store Service

```

Jeder Eintrag in diesem Abschnitt verfügt über einen entsprechenden eigenen Abschnitt, in dem Informationen für den Nachrichtendienst gespeichert werden. Der entsprechende Abschnitt für das Standard-Adressbuch heißt beispielsweise [AB].
  

