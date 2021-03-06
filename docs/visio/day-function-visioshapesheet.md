---
title: DAY-Funktion (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251415
localization_priority: Normal
ms.assetid: 3b0842ae-6893-2d7b-6cb2-8905198fae30
description: Gibt eine ganze Zahl von 1 bis 31 zurück, die den Tag in Datetime oder Ausdruck darstellt. Die DAY-Funktion verwendet den gregorianischen Kalender.
ms.openlocfilehash: 49c29d5dc25bf11599f89a20cb2bc2367bd74187
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360296"
---
# <a name="day-function-visioshapesheet"></a>DAY-Funktion (VisioShapeSheet)

Gibt eine ganze Zahl von 1 bis 31 zurück, die den Tag in _datetime oder_ Ausdruck _darstellt._ Die DAY-Funktion verwendet den gregorianischen Kalender.
  
## <a name="syntax"></a>Syntax

DAY(" ** *datetime* ** "| ** *Ausdruck* ** [, ** *lcid* ** ]) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _datetime_ <br/> |Erforderlich  <br/> |**String** <br/> |Beliebige Zeichenfolge, die allgemein als Datums- und Zeitangabe erkannt wird, oder ein Bezug auf eine Zelle mit einer Datums- und Zeitangabe.  <br/> |
| _expression_ <br/> |Erforderlich  <br/> |**String** <br/> |Beliebiger Ausdruck, der eine Datums- und Zeitangabe liefert.  <br/> |
| _lcid_ <br/> |Optional.  <br/> |**Number** <br/> |Gibt den lokalen Bezeichner an, der bei der Auswertung eines nicht lokalen Werts für datetime verwendet werden soll. Der lokale Bezeichner ist eine Zahl, die in den Systemkopfdateien beschrieben wird.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

Ganze Zahl
  
## <a name="remarks"></a>Bemerkungen

Jede Zeitkomponente in  _datetime_ oder  _ausdruck_ wird verworfen. 
  
Es findet kein Auf- oder Abrunden statt. Wenn  _datetime_ fehlt oder nicht in ein gültiges Ergebnis konvertiert werden kann, gibt die Funktion einen Fehler zurück. 
  
Die DAY-Funktion akzeptiert auch  einen einzelnen Zahlenwert für ausdruck, wobei der ganzzahlige Teil des Ergebnisses die Anzahl der Tage seit dem 30. Dezember 1899 darstellt. 
  
## <a name="example-1"></a>Beispiel 1

DAY("30. Mai 1997 15:45:24")
  
Gibt 30 zurück.
  
## <a name="example-2"></a>Beispiel 2

DAY(DATUMSWERT("30. Mai 1997")+7 t.)
  
Gibt 6 zurück.
  
## <a name="example-3"></a>Beispiel 3

DAY(35580.6337)
  
Gibt 30 zurück.
  

