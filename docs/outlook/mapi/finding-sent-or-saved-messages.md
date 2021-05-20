---
title: Suchen nach gesendeten oder gespeicherten Nachrichten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6b6714a5-7f36-4a72-9a2a-0d7fdf0e21b7
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 86373fae2753df66d4456cc0fc00f8b289977650
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437420"
---
# <a name="finding-sent-or-saved-messages"></a>Suchen nach gesendeten oder gespeicherten Nachrichten

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
 **So suchen Sie alle ausgehenden Nachrichten, die Sie gespeichert oder gesendet haben**
  
1. Rufen [Sie IMsgStore::CompareEntryIDs](imsgstore-compareentryids.md) auf, um den Ordner mit den gesendeten Nachrichten mit dem Ordner zu vergleichen, der ihre eingehenden Nachrichten enthält. 
    
2. Legen Sie den  _lpEntryID1-Parameter_ **auf PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)) und  _den lpEntryID2-Parameter_ auf **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md))
    
Beachten Sie, dass diese Strategie nicht funktioniert, wenn Sie Nachrichten löschen, nachdem sie gesendet wurden oder eine der gesendeten Nachrichten in einen anderen Ordner verschoben haben. 
  
Wenn Sie bei der Untersuchung einer eingehenden Nachricht feststellen, dass die Eigenschaften fehlen, die normalerweise von einem Transportanbieter festgelegt werden, können Sie davon ausgehen, dass die Nachricht nie von einem Transportanbieter verarbeitet wurde. Zu diesen Eigenschaften zählen:
  
- **PR_RECEIVED_BY** Eigenschaften 
    
- **PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))
    
- **PR_TRANSPORT_MESSAGE_HEADERS** ([PidTagTransportMessageHeaders](pidtagtransportmessageheaders-canonical-property.md))
    
- **PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md))
    
- **PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md))
    
- **PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md))
    

