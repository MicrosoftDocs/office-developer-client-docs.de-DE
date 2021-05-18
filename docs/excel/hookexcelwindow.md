---
title: HookExcelWindow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- HookExcelWindow
keywords:
- hookexcelwindow-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: 13f0ae5e-9951-4e89-a245-7cf68c6f6724
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 4103bf3a95388d20efeb74fcd736aeb5520d0845
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413507"
---
# <a name="hookexcelwindow"></a><span data-ttu-id="317da-104">HookExcelWindow</span><span class="sxs-lookup"><span data-stu-id="317da-104">HookExcelWindow</span></span>

 <span data-ttu-id="317da-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="317da-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="317da-106">Installiert **ExcelCursorProc** so, dass es vor dem Microsoft Excel **WndProc aufgerufen wird.**</span><span class="sxs-lookup"><span data-stu-id="317da-106">Installs **ExcelCursorProc** so that it is called before the Microsoft Excel main **WndProc**.</span></span>
  
```cs
extern void FAR PASCAL HookExcelWindow(HANDLE hWndExcel);
```

## <a name="parameters"></a><span data-ttu-id="317da-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="317da-107">Parameters</span></span>

 <span data-ttu-id="317da-108">_hWndExcel_ (**HANDLE**)</span><span class="sxs-lookup"><span data-stu-id="317da-108">_hWndExcel_ (**HANDLE**)</span></span>
  
<span data-ttu-id="317da-109">Das Excel-Windows-Handle.</span><span class="sxs-lookup"><span data-stu-id="317da-109">The Excel main Windows handle.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="317da-110">Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="317da-110">Property value/Return value</span></span>

<span data-ttu-id="317da-111">Die Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="317da-111">The function does not return a value.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="317da-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="317da-112">Remarks</span></span>

<span data-ttu-id="317da-113">Die Funktion ruft die Adresse des Excel **WndProc** über die Verwendung von **GetWindowLong() ab.**</span><span class="sxs-lookup"><span data-stu-id="317da-113">The function obtains the address of the Excel **WndProc** through the use of **GetWindowLong()**.</span></span> <span data-ttu-id="317da-114">Er speichert diesen Wert in einer globalen Datei, die zum Aufrufen des **Standard-WndProc** und zum Wiederherstellen verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="317da-114">It stores this value in a global that can be used to call the default **WndProc** and also to restore it.</span></span> <span data-ttu-id="317da-115">Schließlich wird diese Adresse durch die Adresse von **ExcelCursorProc** mithilfe von **SetWindowLong() ersetzt.**</span><span class="sxs-lookup"><span data-stu-id="317da-115">Finally, it replaces this address with the address of **ExcelCursorProc** using **SetWindowLong()**.</span></span>
  
### <a name="example"></a><span data-ttu-id="317da-116">Beispiel</span><span class="sxs-lookup"><span data-stu-id="317da-116">Example</span></span>

<span data-ttu-id="317da-117">Den  `\SAMPLES\GENERIC\GENERIC.C` Quellcode für diese Funktion finden Sie unter.</span><span class="sxs-lookup"><span data-stu-id="317da-117">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="317da-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="317da-118">See also</span></span>



[<span data-ttu-id="317da-119">Funktionen in der generische DLL</span><span class="sxs-lookup"><span data-stu-id="317da-119">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

