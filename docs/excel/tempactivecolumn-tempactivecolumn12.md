---
title: TempActiveColumn/TempActiveColumn12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempActiveColumn
- TempActiveColumn12
keywords:
- tempactivecolumn12-Funktion [excel 2007],TempActiveColumn-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: 4b1f34c4-e7fa-4a0b-8fc5-c9d465ebb70c
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: d1399a407e3e269b78c7afbde8ff32c126b4b1bc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417875"
---
# <a name="tempactivecolumntempactivecolumn12"></a><span data-ttu-id="b5ab7-104">TempActiveColumn/TempActiveColumn12</span><span class="sxs-lookup"><span data-stu-id="b5ab7-104">TempActiveColumn/TempActiveColumn12</span></span>

 <span data-ttu-id="b5ab7-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="b5ab7-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="b5ab7-106">Frameworkbibliotheksfunktionen, die eine temporäre **XLOPER** /  **XLOPER12** erstellen, die einen externen Verweis auf eine gesamte Spalte im aktiven Blatt enthält.</span><span class="sxs-lookup"><span data-stu-id="b5ab7-106">Framework library functions that create a temporary **XLOPER**/ **XLOPER12** containing an external reference to an entire column on the active sheet.</span></span> 
  
```cs
LPXLOPER TempActiveColumn(BYTE col);
LPXLOPER12 TempActiveColumn12(COL col);
```

## <a name="parameters"></a><span data-ttu-id="b5ab7-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="b5ab7-107">Parameters</span></span>

 <span data-ttu-id="b5ab7-108">_col_ (**BYTE**)</span><span class="sxs-lookup"><span data-stu-id="b5ab7-108">_col_ (**BYTE**)</span></span>
  
<span data-ttu-id="b5ab7-109">Die Spalte, auf die verwiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="b5ab7-109">The column to be referenced.</span></span> <span data-ttu-id="b5ab7-110">Dies ist nullbasierte, sodass Spalte A als 0 übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="b5ab7-110">This is zero-based so that column A is passed as 0.</span></span> <span data-ttu-id="b5ab7-111">In Microsoft Office Excel 2003 und früheren Versionen und ab Excel 2007, in dem eine Arbeitsmappe im Kompatibilitätsmodus ausgeführt wird, ist der Maximalwert 255 = 2^8 - 1 und der Höchstwert, der von einer GANZZAHL von BYTE verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="b5ab7-111">In Microsoft Office Excel 2003 and earlier versions, and starting in Excel 2007 running a workbook in compatibility mode, the maximum value is 255 = 2^8 - 1 and is the maximum value that can be taken by a BYTE integer.</span></span> <span data-ttu-id="b5ab7-112">Ab Excel 2007, in dem eine Arbeitsmappe ausgeführt wird, ist der maximale Wert 16.383 = 2^14 - 1.</span><span class="sxs-lookup"><span data-stu-id="b5ab7-112">Starting in Excel 2007 running a workbook, the maximum value is 16,383 = 2^14 - 1.</span></span> <span data-ttu-id="b5ab7-113">COL ist in XLCALL.H als 32-Bit-ganzzahlige 32-Bit-Zahl definiert.</span><span class="sxs-lookup"><span data-stu-id="b5ab7-113">COL is defined as a 32-bit signed integer in XLCALL.H.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="b5ab7-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b5ab7-114">Return value</span></span>

<span data-ttu-id="b5ab7-115">Gibt einen **externen xltypeRef-Verweis** auf die übergebene Spalte zurück.</span><span class="sxs-lookup"><span data-stu-id="b5ab7-115">Returns an **xltypeRef** external reference to the column passed in.</span></span> 
  
## <a name="example"></a><span data-ttu-id="b5ab7-116">Beispiel</span><span class="sxs-lookup"><span data-stu-id="b5ab7-116">Example</span></span>

<span data-ttu-id="b5ab7-117">Im folgenden Beispiel wird **TempActiveColumn12 verwendet,** um die gesamte Spalte B auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="b5ab7-117">The following example uses **TempActiveColumn12** to select the entire column B.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempActiveColumnExample(void)
{
    Excel12f(xlcSelect, 0, 1, TempActiveColumn12(1));
    return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="b5ab7-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b5ab7-118">See also</span></span>



[<span data-ttu-id="b5ab7-119">Funktionen in der Framework-Klassenbibliothek</span><span class="sxs-lookup"><span data-stu-id="b5ab7-119">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

