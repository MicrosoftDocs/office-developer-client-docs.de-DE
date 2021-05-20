---
title: BLUE-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251402
localization_priority: Normal
ms.assetid: da9fb933-4e2c-3e2a-1879-6e70db0cd830
description: Gibt die blaue Komponente einer Farbe zurück. Der Rückgabewert ist eine ganze Zahl im Bereich von 0 bis einschließlich 255. Bei einer ungültigen Eingabe wird 0 zurückgegeben.
ms.openlocfilehash: adefbe0f8c2df0ead0f3e50cd5d4945501972865
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439037"
---
# <a name="blue-function"></a>BLUE Function

Gibt die blaue Komponente einer Farbe zurück. Der Rückgabewert ist eine ganze Zahl im Bereich von 0 bis einschließlich 255. Bei einer ungültigen Eingabe wird 0 zurückgegeben.
  
## <a name="syntax"></a>Syntax

BLUE(** *Expression* ** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _expression_ <br/> |Erforderlich  <br/> |**String** <br/> |Ein Index einer Farbe aus der Farbtabelle des Dokuments, ein Ausdruck, der zu einer benutzerdefinierten Farbe (wie RGB oder HSL) aufgelöst wird, oder ein Bezug auf eine Zelle, die einen Farbindex oder ein Farbergebnis enthält.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

Ganze Zahl
  
## <a name="example-1"></a>Beispiel 1

BLUE(Sheet.4! FillForegnd)
  
Gibt die Blaukomponente der Vordergrundfüllfarbe von Sheet.4 zurück.
  
## <a name="example-2"></a>Beispiel 2

BLUE(13)
  
Gibt 128 zurück, wenn das Dokument die Standardfarbpalette von Visio verwendet, wobei Cyan die Farbe mit Index 13 ist.
  
## <a name="example-3"></a>Beispiel 3

BLUE(RGB(10, 20, 30))
  
Gibt 30 zurück.
  

