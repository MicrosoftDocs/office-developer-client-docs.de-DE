---
title: Erforderliche Funktionalität für Transportanbieter
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a0d9a3e0-a500-4d72-8859-ecfd1604fc5b
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 7f9768d47cf740bdf50b439ee3af4b0d2a191602
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404442"
---
# <a name="required-functionality-for-transport-providers"></a>Erforderliche Funktionalität für Transportanbieter

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Jeder MAPI-Transportanbieter muss:
  
- Befolgen Sie die allgemeinen Richtlinien für die Arbeit mit MAPI und anderen Dienstanbietern. Weitere Informationen finden Sie unter [MAPI Application Development](mapi-application-development.md) und [MAPI Service Providers](mapi-service-providers.md).
    
- Die INITIALISIERUNGsfunktion des Transportanbieters DLL für MAPI verfügbar zu machen. [](xpproviderinit.md) 
    
- Expose to MAPI its implementation of the [IXPProvider : IUnknown](ixpprovideriunknown.md) and [IXPLogon : IUnknown](ixplogoniunknown.md) interfaces. 
    
- Machen Sie MAPI und Clientanwendungen die Implementierung der [IMAPIStatus : IMAPIProp-Schnittstelle](imapistatusimapiprop.md) verfügbar. Weitere Informationen zum Implementieren von **IMAPIStatus** finden Sie unter [Status Object Implementation](status-object-implementation.md). 
    
- Implementieren Sie ein Eigenschaftenblattdialogfeld für die Konfiguration. Weitere Informationen zum Implementieren von Eigenschaftenblättern finden Sie unter [Property Sheet Implementation](property-sheet-implementation.md).
    

