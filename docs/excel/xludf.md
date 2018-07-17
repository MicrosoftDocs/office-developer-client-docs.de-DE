---
title: xlUDF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlUDF
keywords:
- XlUDF-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: b608b356-ca5c-47bb-9de8-9b7e2b3924dd
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 8f45f800ca50d2a46792e7cf5e00ac25bd099e8c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790623"
---
# <a name="xludf"></a><span data-ttu-id="c7d9f-104">xlUDF</span><span class="sxs-lookup"><span data-stu-id="c7d9f-104">xlUDF</span></span>

<span data-ttu-id="c7d9f-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="c7d9f-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="c7d9f-106">Ruft eine benutzerdefinierte Funktion (UDF).</span><span class="sxs-lookup"><span data-stu-id="c7d9f-106">Calls a user-defined function (UDF).</span></span> <span data-ttu-id="c7d9f-107">Diese Funktion ermöglicht eine DLL zu Visual Basic für Applikationen (VBA) von benutzerdefinierten Funktionen, XLM-Makros-Sprache-Funktionen und registrierten in anderen add-ins enthaltenen Funktionen aufrufen.</span><span class="sxs-lookup"><span data-stu-id="c7d9f-107">This function allows a DLL to call Visual Basic for Applications (VBA) user-defined functions, XLM macro language functions, and registered functions contained in other add-ins.</span></span>
  
```cs
Excel12(xlUDF, LPXLOPER12 pxRes, int iCount, LPXLOPER12 pxFnRef,
LPXLOPER12 pxArg1, ...);
```

## <a name="parameters"></a><span data-ttu-id="c7d9f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c7d9f-108">Parameters</span></span>

<span data-ttu-id="c7d9f-109">_pxFnRef_ (**XltypeRef**, **XltypeSRef**, **XltypeStr** oder **XltypeNum**)</span><span class="sxs-lookup"><span data-stu-id="c7d9f-109">_pxFnRef_ (**xltypeRef**, **xltypeSRef**, **xltypeStr** or **xltypeNum**)</span></span>
  
<span data-ttu-id="c7d9f-110">Der Verweis von der Funktion, die Sie anrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="c7d9f-110">The reference of the function you want to call.</span></span> <span data-ttu-id="c7d9f-111">Dies kann ein Makro Blatt Zellbezug aufweisen, der registrierten Name der Funktion als String oder die Register-ID der Funktion sein.</span><span class="sxs-lookup"><span data-stu-id="c7d9f-111">This can be a macro sheet cell reference, the registered name of the function as a string, or the register ID of the function.</span></span> <span data-ttu-id="c7d9f-112">Für XLL-add-in-Funktionen mit **XlfRegister** , oder **Registrieren Sie** mit der bereitgestellten Argument _PxFunctionText_ registriert kann die ID mit **XlfEvaluate** zum Nachschlagen von den Namen abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="c7d9f-112">For XLL add-in functions registered using **xlfRegister** or **REGISTER** with the argument  _pxFunctionText_ supplied, the ID can be obtained by using **xlfEvaluate** to look up the name.</span></span> 
  
<span data-ttu-id="c7d9f-113">_pxArg1..._</span><span class="sxs-lookup"><span data-stu-id="c7d9f-113">_pxArg1, ..._</span></span>
  
<span data-ttu-id="c7d9f-114">NULL oder mehr Argumente an die benutzerdefinierte Funktion.</span><span class="sxs-lookup"><span data-stu-id="c7d9f-114">Zero or more arguments to the user-defined function.</span></span> <span data-ttu-id="c7d9f-115">Wenn Sie diese Funktion in Versionen vor Excel 2007 aufrufen, die maximale Anzahl von zusätzlichen Argumenten, die übergeben werden kann, ist 29, 30 einschließlich _PxFnRef_.</span><span class="sxs-lookup"><span data-stu-id="c7d9f-115">When you are calling this function in versions earlier than Excel 2007, the maximum number of additional arguments that can be passed is 29, which is 30 including  _pxFnRef_.</span></span> <span data-ttu-id="c7d9f-116">Ab Excel 2007 dieser Grenze ausgelöst wird in 254, 255 einschließlich _PxFnRef_.</span><span class="sxs-lookup"><span data-stu-id="c7d9f-116">Starting in Excel 2007, this limit is raised to 254, which is 255 including  _pxFnRef_.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="c7d9f-117">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="c7d9f-117">Return value</span></span>

<span data-ttu-id="c7d9f-118">Gibt den Wert der benutzerdefinierten Funktion zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c7d9f-118">Returns whatever value the user-defined function returned.</span></span>
  
## <a name="example"></a><span data-ttu-id="c7d9f-119">Beispiel</span><span class="sxs-lookup"><span data-stu-id="c7d9f-119">Example</span></span>

<span data-ttu-id="c7d9f-120">Das folgende Beispiel führt die **Kategorie** auf Blatt Macro1 in Mappe1. XLS.</span><span class="sxs-lookup"><span data-stu-id="c7d9f-120">The following example runs **TestMacro** on sheet Macro1 in BOOK1.XLS.</span></span> <span data-ttu-id="c7d9f-121">Stellen Sie sicher, dass das Makro in einem Blatt Makro1 ist.</span><span class="sxs-lookup"><span data-stu-id="c7d9f-121">Make sure that the macro is on a sheet named Macro1.</span></span> 
  
`\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlUDFExample(void)
{       
   XLOPER12 xMacroName, xMacroRef, xRes;
   xMacroName.xltype = xltypeStr;
   xMacroName.val.str = L"\044[BOOK1.XLSX]Macro1!TestMacro";
   Excel12(xlfEvaluate, &xMacroRef, 1, (LPXLOPER12)&xMacroName);
   Excel12(xlUDF, &xRes, 1, (LPXLOPER12)&xMacroRef);
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="c7d9f-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c7d9f-122">See also</span></span>

- [<span data-ttu-id="c7d9f-123">C C-API-Funktionen, die nur aus einer DLL oder XLL aufgerufen werden k�nnen</span><span class="sxs-lookup"><span data-stu-id="c7d9f-123">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
