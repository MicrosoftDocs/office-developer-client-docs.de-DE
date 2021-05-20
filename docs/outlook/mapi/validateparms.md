---
title: ValidateParms
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ValidateParms
api_type:
- COM
ms.assetid: 3ede1a35-4acc-4b8f-a1bd-027f35798a37
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f2669f703827924493387c4beac0b64b25672860
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436804"
---
# <a name="validateparms"></a>ValidateParms

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ruft eine interne Funktion auf, um die Parameter zu überprüfen, die Clientanwendungen an Dienstanbieter übergeben haben. 
  
|||
|:-----|:-----|
|Headerdatei:  <br/> |Mapival.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Dienstanbieter  <br/> |
   
```cpp
HRESULT ValidateParms(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a>Parameter

 _eMethod_
  
> [in] Gibt die zu überprüfende Methode per Enumeration an. 
    
 _First_
  
> [in] Zeiger auf das erste Argument auf dem Stapel.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Alle Parameter sind gültig. 
    
MAPI_E_CALL_FAILED 
  
> Mindestens einer der Parameter ist ungültig.
    
## <a name="remarks"></a>Hinweise

Parameter, die zwischen MAPI und Dienstanbietern übergeben werden, werden als richtig angenommen und werden nur mit dem [CheckParms-Makro](checkparms.md) einer Debugüberprüfung unterzogen. Anbieter sollten alle von Clientanwendungen übergebenen Parameter überprüfen, Clients sollten jedoch davon ausgehen, dass MAPI- und Anbieterparameter korrekt sind. Verwenden Sie das **HR_FAILED,** um Rückgabewerte zu testen. 
  
 **ValidateParms** wird unterschiedlich aufgerufen, je nachdem, ob der aufrufende Code C oder C++ ist. C++ übergibt jeden Methodenaufruf einen impliziten Parameter, der in C explizit wird und die Adresse des Objekts ist.  Der erste  _Parameter, eMethod_, ist ein Aufzählerator, der aus der zu überprüfenden Schnittstelle und Methode besteht, und gibt an, welche Parameter auf dem Stapel zu finden sind. Der zweite Parameter ist für C und C++ unterschiedlich. In C++ heißt er  _First_, und er ist der erste Parameter für die zu überprüfende Methode. Der zweite Parameter für die Sprache C,  _ppThis_, ist die Adresse des ersten Parameters für die Methode, die immer ein Objektzeiger ist. In beiden Fällen gibt der zweite Parameter die Adresse des Anfangs der Parameterliste der Methode an, und basierend auf  _eMethod_ wird der Stapel nach unten bewegt und die Parameter überprüft. 
  
Anbieter, die allgemeine Schnittstellen wie **IMAPITable** und **IMAPIProp** implementieren, sollten parameter immer mit der **ValidateParms-Funktion** überprüfen, um die Konsistenz für alle Anbieter sicherzustellen. Zusätzliche Parameterüberprüfungsfunktionen wurden definiert, damit einige komplexe Parametertypen stattdessen entsprechend verwendet werden können. Die folgenden Funktionen finden Sie in den Referenzthemen: 
  
- [FBadColumnSet](fbadcolumnset.md)
    
- [FBadEntryList](fbadentrylist.md)
    
- [FBadProp](fbadprop.md)
    
- [FBadProp](fbadprop.md)
    
- [FBadRestriction](fbadrestriction.md)
    
- [FBadRestriction](fbadrestriction.md)
    
- [FBadRglpszW](fbadrglpszw.md)
    
- [FBadRow](fbadrow.md)
    
- [FBadRowSet](fbadrowset.md)
    
- [FBadSortOrderSet](fbadsortorderset.md)
    
Geerbte Methoden verwenden dieselbe Parameterüberprüfung wie die Schnittstelle, von der sie erben. Beispielsweise sollte die Parameterüberprüfung für **IMessage** und **IMAPIProp** identisch sein. 
  
## <a name="see-also"></a>Siehe auch



[UlValidateParms](ulvalidateparms.md)

