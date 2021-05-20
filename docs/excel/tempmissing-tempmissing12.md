---
title: TempMissing/TempMissing12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempMissing
- TempMissing12
keywords:
- tempmissing function [excel 2007],TempMissing12 function [Excel 2007]
localization_priority: Normal
ms.assetid: d9cb6afc-1fbb-45d6-88e5-84eba3af3c60
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 37c127b2252f18643b34dfc72fd9929885a68d01
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435957"
---
# <a name="tempmissingtempmissing12"></a>TempMissing/TempMissing12

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Frameworkbibliotheksfunktion, die eine temporäre **XLOPER** /  **XLOPER12 vom** Typ **xltypeMissing erstellt.**
  
```cs
LPXLOPER TempMissing(void);
LPXLOPER12 TempMissing12(void);
```

## <a name="parameters"></a>Parameter

Diese Funktion verwendet keine Parameter.
  
## <a name="return-value"></a>Rückgabewert

Gibt einen Zeiger auf **xltypeMissing** **XLOPER** /  **XLOPER12 zurück.**
  
## <a name="example"></a>Beispiel

In diesem Beispiel wird **TempMissing12** verwendet, um **xlcWorkspace** drei fehlende Argumente zu geben, gefolgt von **einem Boolean** **FALSE,** um die Anzeige von Arbeitsblatt-Bildlaufleisten zu unterdrücken. Die ersten drei Argumente entsprechen anderen Arbeitsbereichseinstellungen, die nicht betroffen sind. 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempMissingExample(void)
{
   XLOPER12 xBool;
   xBool.xltype = xltypeBool;
   xBool.val.xbool = 0;
   Excel12f(xlcWorkspace, 0, 4, TempMissing12(), TempMissing12(),
      TempMissing12(), (LPXLOPER12)&xBool);
   return 1;
}
```

## <a name="see-also"></a>Siehe auch



[Funktionen in der Framework-Klassenbibliothek](functions-in-the-framework-library.md)

