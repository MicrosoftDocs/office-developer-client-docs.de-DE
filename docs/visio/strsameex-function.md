---
title: STRSAMEEX-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251787
localization_priority: Normal
ms.assetid: 056b54ae-1475-9480-6ebc-5c34ef48e0f8
description: Bestimmt, ob zwei Zeichenfolgen identisch sind.
ms.openlocfilehash: ac5a74e08079f86c28b086b92302ebb01a4b0627
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413864"
---
# <a name="strsameex-function"></a>STRSAMEEX Function

Bestimmt, ob zwei Zeichenfolgen identisch sind.
  
## <a name="syntax"></a>Syntax

STRSAMEEX (" ** *string1* ** ", " ** *string2* ** ", ** *localeID* **, ** *flag* ** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _string1_ <br/> |Erforderlich  <br/> |**String** <br/> |Die erste zu vergleichende Zeichenfolge.  <br/> |
| _string2_ <br/> |Erforderlich  <br/> |**String** <br/> | Die zweite zu vergleichende Zeichenfolge.  <br/> |
| _localeID_ <br/> |Erforderlich  <br/> |**Numeric** <br/> |Der lokale ID-Code.  <br/> |
| _Flag_ <br/> |Erforderlich  <br/> |**Numeric** <br/> | Ein Bit, das den Typ des Vergleichs bestimmt.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

Boolesch
  
## <a name="remarks"></a>Bemerkungen

STRSAMEEX gibt TRUE zurück, wenn beide Eingabezeichenfolgen identisch sind. Ist dies nicht der Fall, wird FALSE zurückgegeben. Verwenden Sie diese Funktion, wenn Sie Multibyte-Zeichenfolgen vergleichen oder Vergleiche mit Groß- und Kleinschreibregeln für ein bestimmtes Gebietsschema durchführen möchten.
			

  
Sie können eine beliebige Kombination folgender Flags mit der STRGLEICHEX-Funktion verwenden.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|1  <br/> |Groß- und Kleinschreibung ignorieren.  <br/> |
|2  <br/> |Nicht-gesperrte Zeichen ignorieren.  <br/> |
|4   <br/> |Symbole ignorieren.  <br/> |
|4096  <br/> |Interpunktionszeichen wie Symbole behandeln.  <br/> |
|65536  <br/> |Nicht zwischen Hiragana- und Katakana-Zeichen unterscheiden.  <br/> |
|131072  <br/> |Nicht zwischen Einzel-Byte-Zeichen und dem gleichen Zeichen als Doppel-Byte-Zeichen unterscheiden.  <br/> |
   

