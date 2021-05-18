---
title: Behandeln von Adressbuchbenachrichtigungen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0dc4bb48-c8a1-447f-9e38-1c234a358fca
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 122e50328272a4009e5a129233d449613817dfc8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413535"
---
# <a name="handing-address-book-notification"></a>Behandeln von Adressbuchbenachrichtigungen
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Adressbuchbenachrichtigungen ermöglichen es einem Client, von Ereignissen zu erfahren, die für jeden Adressbucheintrag oder für einen bestimmten Eintrag auftreten. Sie können sich für diese Benachrichtigungen entweder über das MAPI-Adressbuch registrieren, indem Sie [IAddrBook::Advise](iaddrbook-advise.md) aufrufen oder die Hierarchie- oder Inhaltstabelle eines Adressbuchcontainers über [IMAPITable::Advise aufrufen.](imapitable-advise.md) 
  
Geben Sie die Eintrags-ID eines Adressbuchcontainers, einer Verteilerliste oder eines Messagingbenutzers an, wenn Sie sich für Benachrichtigungen für einen bestimmten Eintrag registrieren, und NULL, wenn Sie sich für Benachrichtigungen im gesamten Adressbuch registrieren. Der Eintragsbezeichner muss einen Messagingbenutzer oder eine Verteilerliste in einem Adressbuchcontainer darstellen. **IAddrBook::Advise** untersucht diesen Eintragsbezeichner, um zu bestimmen, welcher Adressbuchanbieter für das entsprechende Objekt verantwortlich ist, und gibt den Aufruf an die [IABLogon::Advise-Methode](iablogon-advise.md) des entsprechenden Adressbuchanbieters weiter. 
  
Clients können sich für die folgenden Ereignistypen für Adressbucheinträge registrieren:
  
- Kritischer Fehler
    
- Alle Objektereignisse (erstellt, geändert, gelöscht, verschoben oder kopiert)
    
- Tabelle geändert
    
In der Regel erfolgt die Registrierung nur für Adressbuchcontainerinhalte und Hierarchietabellen. Es ist selten, dass Clients sich bei den Messagingbenutzer- und Verteilerlistenobjekten der unteren Ebene registrieren. Dies liegt daran, dass:
  
- Viele Adressbuchanbieter unterstützen keine Benachrichtigungen für ihre Messagingbenutzer und Verteilerlisten.
    
- Tabellenbenachrichtigungen sind ausreichend, um Änderungen zu verfolgen und sie benutzern zu melden.
    

