---
title: TempErr/TempErr12
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempErr
- TempErr12
keywords:
- "\"tempr\"-Funktion [excel 2007],TempErr12-Funktion [Excel 2007]"
localization_priority: Normal
ms.assetid: cf8c26b2-ca2b-4dda-a02d-0ccbeac19106
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 68a0addc36ecf1b4491ab1e4f5b10f359bbc59c3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410609"
---
# <a name="temperrtemperr12"></a>TempErr/TempErr12

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Framework library function that creates a temporary **XLOPER** /  **XLOPER12** containing a Microsoft Excel worksheet error. 
  
```cs
LPXLOPER TempErr(WORD err);
LPXLOPER12 TempErr12(BOOL err);
```

## <a name="parameters"></a>Parameter

 _err_
  
Der gewünschte Fehlercode oder sein literales numerisches Äquivalent, wie in der folgenden Tabelle dargestellt.
  
|**Error**|**Fehlercode, der in XLCALL definiert ist. H**|**Dezimaläquivalent**|
|:-----|:-----|:-----|
|#NULL  <br/> |**xlerrNull** <br/> |0  <br/> |
|#DIV/0!  <br/> |**xlerrDiv0** <br/> |7   <br/> |
|#VALUE!  <br/> |**xlerrValue** <br/> |15   <br/> |
|#REF!  <br/> |**xlerrRef** <br/> |23  <br/> |
|#NAME?  <br/> |**xlerrName** <br/> |29  <br/> |
|#NUM!  <br/> |**xlerrNum** <br/> |36  <br/> |
|#N/A  <br/> |**xlerrNA** <br/> |42  <br/> |
   
## <a name="return-value"></a>Rückgabewert

Gibt einen **xltypeBool zurück,** der den übergebenen Fehlercode enthält. 
  
## <a name="example"></a>Beispiel

In diesem Beispiel wird die **TempErr12-Funktion** verwendet, um eine #VALUE! Fehler zu Excel. 
  
> [!NOTE]
> Die Framework-Bibliotheksfunktion **TempErr12** weist Speicher aus einem internen Puffer zu, der normalerweise beim Aufgerufen der Framework-Funktion **Excel12f** frei wird. Wenn diese Beispielfunktion wiederholt aufgerufen wird, ohne **dass Excel12f** aufgerufen wird, tritt ein Speicherverlust auf. 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
LPXLOPER WINAPI TempErrExample(void)
{
    return TempErr12(xlerrValue);
}
```

## <a name="see-also"></a>Siehe auch



[Funktionen in der Framework-Klassenbibliothek](functions-in-the-framework-library.md)

