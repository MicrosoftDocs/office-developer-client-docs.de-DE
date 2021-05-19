---
title: TempNum/TempNum12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempNum
- TempNum12
keywords:
- tempnum12-Funktion [excel 2007],TempNum-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: 5b74d618-db3a-4d84-bd17-4fee7ae3b51e
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: cabd44ab828a2cfe22253e9aaf12abf7b7709d69
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426632"
---
# <a name="tempnumtempnum12"></a>TempNum/TempNum12

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Framework library function that creates a temporary **XLOPER** /  **XLOPER12** containing a Microsoft Excel worksheet number (an IEEE 8-byte double). 
  
```cs
LPXLOPER TempNum(double d);
LPXLOPER12 TempNum12(double d);
```

## <a name="parameters"></a>Parameter

 _d_ (**double**)
  
Der beabsichtigte Wert. Beachten Sie, dass IEEE-Unternormalnummern derzeit nicht unterstützt werden und auf Null gerundet werden. Negative Unendlichkeit wird unterstützt.
  
## <a name="return-value"></a>Rückgabewert

Gibt einen numerischen **xltypeNum-Wert zurück,** der den übergebenen Wert oder Null enthält, wenn der übergebene Wert subnormal war. 
  
## <a name="example"></a>Beispiel

In diesem Beispiel wird die **TempNum12-Funktion** verwendet, um ein Argument an **xlfGetWorkspace zu übergeben.**
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempNumExample(void)
{
   XLOPER12 xRes;
   Excel12f(xlfGetWorkspace, &xRes, 1, TempNum12(44));
   Excel12f(xlFree, 0, 1, (LPXLOPER12)&xRes);
   return 1;
}
```

## <a name="see-also"></a>Siehe auch



[Funktionen in der Framework-Klassenbibliothek](functions-in-the-framework-library.md)

