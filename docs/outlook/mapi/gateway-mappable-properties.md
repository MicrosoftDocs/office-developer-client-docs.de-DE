---
title: Zum Gateway zuzuordnende Eigenschaften
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3a51ee7e-d030-4f04-915b-ff8bd351207d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 6f1a399cac2adbae66dabf9383540bb089424d17
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430476"
---
# <a name="gateway-mappable-properties"></a>Zum Gateway zuzuordnende Eigenschaften

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gateway-mappable-Eigenschaften sind Eigenschaften, die eine Übersetzung erfordern, wenn sie von einer Messagingdomäne in eine andere gesendet werden. Die Gateway-Mappable-Eigenschaften von MAPI ermöglichen es Nachrichten, Informationen zu enthalten, für die ein Gateway erforderlich ist, um sicherzustellen, dass das Zielnachrichtensystem es ordnungsgemäß verwendet. Obwohl Gatewayentwickler diese Übersetzungsfunktion nicht bereitstellen müssen, sollten sie Gateway-mappable-Eigenschaften als Möglichkeit zur Verbesserung der Behandlung von Nachrichteninhalten betrachten.
  
MAPI gibt fünf Typen von Gateway-mappable-Eigenschaften an:
  
- Distinguished Name (DN)
    
- Anzeigename
    
- E-Mail-Typ
    
- Eintrags-ID
    
- Suchtaste
    
Dies ist der Satz von Adressierungseigenschaften, die Empfängern, Absendern, Berichtsempfängern und delegierten Absendern und Empfängern zugeordnet sind. Damit Der Client diese Eigenschaften so definieren kann, dass sie von einem Gateway speziell behandelt werden, gibt MAPI eine Benennungskonvention mit benannten Eigenschaften und Eigenschaftensätzen an. Es sind fünf Eigenschaftensätze vorhanden, die benannte Eigenschaften enthalten, die Adressierungseigenschaften, die eine Zuordnung erfordern. Für jeden Typ von mappable-Eigenschaft ist eine Eigenschaft festgelegt. Die Eigenschaftensätze, die diese benannten Adressierungseigenschaften enthalten, sind wie folgt.
  
|**Eigenschaftensatz**|**Beschreibung**|
|:-----|:-----|
|PS_ROUTING_DISPLAY_NAME  <br/> |Enthält Zeichenfolgeneigenschaften, die als Anzeigenamen verwendet werden.  <br/> |
|PS_ROUTING_EMAIL_ADDRESSES  <br/> |Enthält Zeichenfolgeneigenschaften, die als E-Mail-Adressen verwendet werden.  <br/> |
|PS_ROUTING_ADDRTYPE  <br/> |Enthält Zeichenfolgeneigenschaften, die als E-Mail-Adresstypen verwendet werden.  <br/> |
|PS_ROUTING_ENTRYID  <br/> |Enthält binäre Eigenschaften, die als langfristige Eintragsbezeichner verwendet werden.  <br/> |
|PS_ROUTING_SEARCH_KEY  <br/> |Enthält binäre Eigenschaften, die als Suchschlüssel verwendet werden.  <br/> |
   

