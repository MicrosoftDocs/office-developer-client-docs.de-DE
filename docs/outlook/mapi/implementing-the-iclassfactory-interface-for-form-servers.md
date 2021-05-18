---
title: Implementieren der IClassFactory-Schnittstelle für Formularserver
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 22402261-c0fc-49bd-a222-e31989d6ff30
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 12d854b72632653d9e1081c9e726c0fe7087bc27
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310031"
---
# <a name="implementing-the-iclassfactory-interface-for-form-servers"></a>Implementieren der IClassFactory-Schnittstelle für Formularserver

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
[IClassFactory](https://msdn.microsoft.com/library/ms694364%28VS.85%29.aspx) ist die OLE-Schnittstelle, die Clientanwendungen zum Erstellen neuer Formularobjekte der Nachrichtenklasse Des Formularservers verwenden. In der folgenden Tabelle sind die **erforderlichen IClassFactory-Methoden** aufgeführt. 
  
|**Methode**|**Beschreibung**|
|:-----|:-----|
|[CreateInstance](https://msdn.microsoft.com/library/ms682215%28v=VS.85%29.aspx) <br/> |Erstellt ein neues Formularobjekt.  <br/> |
|[LockServer](https://msdn.microsoft.com/library/ms682332%28v=VS.85%29.aspx) <br/> |Sperrt den Formularserver im Arbeitsspeicher, sodass beim Erstellen mehrerer Formularobjekte ein Startaufwand vermieden werden kann.  <br/> |
   
Alle erforderlichen Informationen zum Implementieren dieser Methoden finden Sie im Abschnitt COM und ActiveX Object Services im Windows SDK.
  
## <a name="see-also"></a>Siehe auch



[Schreiben von Formularservercode](writing-form-server-code.md)

