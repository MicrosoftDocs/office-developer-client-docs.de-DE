---
title: Nachrichtenempfangsmodell
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d85d269e-2251-4399-9159-a2f47a85e3d1
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 487598374f15300cc8b899a50d74b535b5a33c91
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415117"
---
# <a name="message-reception-model"></a>Nachrichtenempfangsmodell

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Der Transportanbieter steuert, ob der MAPI-Spooler eingehende E-Mails abruft oder ob ein Rückruf an den MAPI-Spooler beim Eintreffen neuer E-Mails durchführt wird. Der Transportanbieter legt das SP_LOGON_POLL fest, wenn er von [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) zum Anfordern der Abfrage zurückgibt. Andernfalls verwendet der Transportanbieter [IMAPISupport::SpoolerNotify,](imapisupport-spoolernotify.md) wenn eingehende E-Mails verfügbar sind. Nachdem sie gelernt haben, dass eingehende E-Mails verfügbar sind, öffnet der MAPI-Spooler eine neue Nachricht und fordert den Transportanbieter auf, die empfangenen Nachrichteneigenschaften in der Nachricht zu speichern. 
  
Dieser Vorgang funktioniert wie folgt:
  
1. Verfügbare Nachrichten werden entweder vom Transportanbieter angegeben, der **IMAPISupport::SpoolerNotify** aufruft, oder durch den MAPI-Spooler, der [IXPLogon::P oll aufruft.](ixplogon-poll.md)
    
2. Der MAPI-Spooler ruft [IXPLogon::StartMessage auf,](ixplogon-startmessage.md) um den Prozess zu initiieren. 
    
3. Der Transportanbieter platziert einen Referenzwert an dem Speicherort, auf den in **StartMessage verwiesen wird.** Mit diesen Referenzwerten können der Transportanbieter und der MAPI-Spooler nachverfolgen, welche Nachricht verarbeitet wird, wenn mehrere Nachrichten zu liefern sind.
    
4. Der Transportanbieter speichert die Nachrichtendaten in der übergebenen [IMessage : IMAPIProp-Instanz.](imessageimapiprop.md) 
    
5. Der Transportanbieter ruft die [IMAPIProp::SaveChanges-Methode](imapiprop-savechanges.md) für die **IMessage-Instanz** auf und gibt von **StartMessage zurück.**
    
6. Der MAPI-Spooler ruft [IXPLogon::TransportNotify](ixplogon-transportnotify.md) auf, wenn die Nachrichtenzustellung beendet werden muss. 
    
> [!NOTE]
> Wenn ein Transportanbieter eine große Anzahl von Nachrichten bereitstellen muss und der Transportanbieter **IMAPISupport::SpoolerNotify** anstelle von **IXPLogon::P oll** verwendet, sollte darauf achten, **dass SpoolerNotify** nicht zu häufig anruft, um anderen Transportanbietern keine CPU-Zeit zu entziehen. Der MAPI-Spooler verfügt über eine Logik, um dies zu verhindern, aber im Allgemeinen sollte das Intervall zwischen **SpoolerNotify-Aufrufen** länger sein als die Zeit, die ihr Transportanbieter benötigt, um eine Nachricht zu verarbeiten. > Wird eine eingehende Nachricht möglicherweise nicht sofort vom MAPI-Spooler verarbeiten. Der MAPI-Spooler kann den Transportanbieter bitten, andere Aufgaben auszuführen, bevor die eingehende Nachricht empfangen wird. 
  

