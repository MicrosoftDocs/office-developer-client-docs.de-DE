---
title: FuncSum
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- FuncSum
keywords:
- funcsum-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: 934192ef-8a89-4dbb-bd37-01e92ba24256
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 14db5812165812161cf7031f75338a981251dfd2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406941"
---
# <a name="funcsum"></a><span data-ttu-id="df1ba-104">FuncSum</span><span class="sxs-lookup"><span data-stu-id="df1ba-104">FuncSum</span></span>

 <span data-ttu-id="df1ba-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="df1ba-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="df1ba-106">Beispiel für eine benutzerdefinierte Arbeitsblattfunktion, die 1 bis 29 Argumente benötigt und deren Summe berechnet.</span><span class="sxs-lookup"><span data-stu-id="df1ba-106">Example user-defined worksheet function that takes 1 to 29 arguments and computes their sum.</span></span> <span data-ttu-id="df1ba-107">Jedes Argument kann eine einzelne Zahl, ein Bereich oder ein Array sein.</span><span class="sxs-lookup"><span data-stu-id="df1ba-107">Each argument can be a single number, a range, or an array.</span></span> <span data-ttu-id="df1ba-108">Wenn GENERIC.xll geladen wird, registriert es diese Funktion, sodass sie aus dem Arbeitsblatt aufgerufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="df1ba-108">When GENERIC.xll is loaded, it registers this function so that it can be called from the worksheet.</span></span> 
  
```cs
LPXLOPER12 WINAPI FuncSum(LPXLOPER12 px1, LPXLOPER12 px2, LPXLOPER12 px3,LPXLOPER12 px4, LPXLOPER12 px5, LPXLOPER12 px6, LPXLOPER12 px7,LPXLOPER12 px8, LPXLOPER12 px9, LPXLOPER12 px10, LPXLOPER12 px11,LPXLOPER12 px12, LPXLOPER12 px13, LPXLOPER12 px14, LPXLOPER12 px15,LPXLOPER12 px16, LPXLOPER12 px17, LPXLOPER12 px18, LPXLOPER12 px19,LPXLOPER12 px20, LPXLOPER12 px21, LPXLOPER12 px22, LPXLOPER12 px23,LPXLOPER12 px24, LPXLOPER12 px25, LPXLOPER12 px26, LPXLOPER12 px27,LPXLOPER12 px28, LPXLOPER12 px29);
```

## <a name="parameters"></a><span data-ttu-id="df1ba-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="df1ba-109">Parameters</span></span>

 <span data-ttu-id="df1ba-110">_px1-px29_ (**LPXLOPER12**)</span><span class="sxs-lookup"><span data-stu-id="df1ba-110">_px1-px29_ (**LPXLOPER12**)</span></span>
  
<span data-ttu-id="df1ba-111">Zeiger auf **XLOPER12-Argumente.**</span><span class="sxs-lookup"><span data-stu-id="df1ba-111">Pointers to **XLOPER12** arguments.</span></span> <span data-ttu-id="df1ba-112">Die Funktion akzeptiert jede Art von Eingabetyp, ist jedoch nur für den Betrieb mit Zahlen, Literalarrays von Zahlen und Bereichen codiert, die nur Zahlen oder leere Zellen enthalten.</span><span class="sxs-lookup"><span data-stu-id="df1ba-112">The function accepts any kind of input type but is coded only to operate on numbers, literal arrays of numbers, and ranges containing only numbers or blank cells.</span></span> <span data-ttu-id="df1ba-113">Wenn weniger als 29 Argumente angegeben werden, werden die verbleibenden Argumente als **xltypeMissing angegeben.**</span><span class="sxs-lookup"><span data-stu-id="df1ba-113">If fewer than 29 arguments are supplied, the remaining arguments are supplied as **xltypeMissing**.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="df1ba-114">Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="df1ba-114">Property value/Return value</span></span>

<span data-ttu-id="df1ba-115">(**LPXLOPER12 xltypeNum** oder **xltypeErr**)</span><span class="sxs-lookup"><span data-stu-id="df1ba-115">(**LPXLOPER12 xltypeNum** or **xltypeErr**)</span></span>
  
<span data-ttu-id="df1ba-116">Die Summe der Argumente oder #VALUE!</span><span class="sxs-lookup"><span data-stu-id="df1ba-116">The sum of the arguments or #VALUE!</span></span> <span data-ttu-id="df1ba-117">wenn in der angegebenen Argumentliste oder in einer Zelle in einem Bereich oder Element in einem Array nicht numerische Zahlen vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="df1ba-117">if there are non-numerics in the supplied argument list or in a cell in a range or element in an array.</span></span>
  
### <a name="example"></a><span data-ttu-id="df1ba-118">Beispiel</span><span class="sxs-lookup"><span data-stu-id="df1ba-118">Example</span></span>

<span data-ttu-id="df1ba-119">Den  `\SAMPLES\GENERIC\GENERIC.C` Quellcode für diese Funktion finden Sie unter.</span><span class="sxs-lookup"><span data-stu-id="df1ba-119">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="df1ba-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="df1ba-120">See also</span></span>



[<span data-ttu-id="df1ba-121">Funktionen in der generische DLL</span><span class="sxs-lookup"><span data-stu-id="df1ba-121">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

