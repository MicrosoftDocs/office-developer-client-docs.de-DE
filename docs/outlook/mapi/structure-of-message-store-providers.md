---
title: Struktur eines Nachrichtenspeicheranbieters
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 064b2fc1-e690-43e6-95d3-a61438115de5
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: eda62a4cd31e0de695d52391a6717e7a0f5ea581
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426422"
---
# <a name="structure-of-message-store-providers"></a>Struktur eines Nachrichtenspeicheranbieters
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ein Nachrichtenspeicheranbieter, wenn er im Arbeitsspeicher ausgeführt wird, ist eine [IMSProvider : IUnknown-Schnittstelle.](imsprovideriunknown.md) Über **die IMSProvider-Schnittstelle** können sich Clientanwendungen und der MAPI-Spooler beim nachrichtenspeicher anmelden und abmelden. Die Schnittstellen, die Clientanwendungen und der MAPI-Spooler für den Zugriff auf Ordner und Nachrichten im Nachrichtenspeicher verwenden, sind [IMSLogon-](imslogoniunknown.md) und [IMsgStore-Schnittstellen.](imsgstoreimapiprop.md) Diese Schnittstellen werden in der Regel erstellt, wenn der Nachrichtenspeicher zum ersten Mal angemeldet ist, obwohl sie auch vom [MSProviderInit-Einstiegspunkt](msproviderinit.md) der Nachrichtenspeicher-DLL erstellt werden können. 
  
Da die **IMSLogon-** und **IMsgStore-Schnittstellen** einige Methoden gemeinsam verwenden, ist es möglicherweise einfacher, ein Klassenobjekt zu erstellen, das von beiden Schnittstellen erbt. Sie können diese Schnittstellen auch in separaten Objekten implementieren und Hilfsfunktionen intern in Ihre DLL schreiben, die die gemeinsam genutzten Methoden implementieren, die dann von den Methoden in den **ImSLogon-** und **IMsgStore-Schnittstellen** aufgerufen werden können. 
  
Die folgende Abbildung zeigt eine übersichtsorientierte Gliederung der Objekthierarchie innerhalb eines ausgeführten Nachrichtenspeichers.
  
**Objekthierarchie des Nachrichtenspeichers**
  
![Objekthierarchie des Nachrichtenspeichers](media/storeobj.gif "Nachrichtenspeicherobjekthierarchie")
  
## <a name="see-also"></a>Siehe auch

- [Entwickeln eines MAPI-Nachrichtenspeicheranbieters](developing-a-mapi-message-store-provider.md)

