---
title: Schreiben eines automatisierten Clients
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b8f9ac1a-b377-4f83-8fb6-ed85ab9053d0
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: f9ce3452bbc2d3297cc67168835a9387235746a8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439765"
---
# <a name="writing-an-automated-client"></a>Schreiben eines automatisierten Clients

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Eine automatisierte Clientanwendung ist eine Anwendung, die unbeaufsichtigt ausgeführt wird und keine Benutzeroberfläche zeigt.
  
 Standardmäßig zeigen viele MAPI-Schnittstellenmethoden eine Benutzeroberfläche an. Alle diese Methoden verfügen über Flags, mit denen ein Client diese Anzeige entweder zulassen oder unterdrücken kann. Obwohl MAPI erwartet, dass Dienstanbieter diese Kennzeichen erfüllen, gibt es einige Anbieter, die diese Erwartungen nicht immer erfüllen. Ein legitimer Grund dafür, dass die Kennzeichen nicht berücksichtigt werden, ist die Abhängigkeit des Dienstanbieters von einem anderen Dienst, der keine Benutzeroberflächenunterdrückung zu lässt. Wenn Sie einen automatisierten Client entwickeln, achten Sie sorgfältig auf die von Ihnen verwendeten Dienstanbieter und deren Konfiguration. Gehen Sie nicht davon aus, dass alle Aufrufe zum Unterdrücken einer Benutzeroberfläche erfolgreich sind. 
  
Automatisierte Clients müssen über die erforderlichen Informationen für die ordnungsgemäße Konfiguration der einzelnen Nachrichtendienste im Profil verfügen. Es gibt zwei Möglichkeiten, Konfigurationsinformationen zur Anmeldezeit zur Verfügung zu stehen:
  
- Der Dienstanbieter kann Informationen aus dem Profil abrufen.
    
- Der Dienstanbieter kann den Benutzer zur Eingabe von Informationen aufforderen. 
    
Da die zweite Option für automatisierte Clients nicht verfügbar ist, müssen diese Clients die erste Option verwenden. Clients müssen ihre Profile sorgfältig konfigurieren, um sicherzustellen, dass diese Option immer funktioniert.
  
Automatisierte Clients legen immer das MAPI_NO_MAIL im [MAPILogonEx-Funktionsaufruf](mapilogonex.md) ein, um eine MAPI-Sitzung zu starten. 
  

