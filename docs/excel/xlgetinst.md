---
title: xlGetInst
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlGetInst
keywords:
- xlgetinst-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: 631a8f4e-ea7c-4743-9ee1-b2233fd7d98d
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: e113ddbf55e2b4651d578549802c44e2c6413a18
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428130"
---
# <a name="xlgetinst"></a><span data-ttu-id="30edc-104">xlGetInst</span><span class="sxs-lookup"><span data-stu-id="30edc-104">xlGetInst</span></span>

 <span data-ttu-id="30edc-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="30edc-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="30edc-106">Gibt das Instanzhandle der Instanz des Microsoft Excel, die derzeit eine DLL aufruft.</span><span class="sxs-lookup"><span data-stu-id="30edc-106">Returns the instance handle of the instance of Microsoft Excel that is currently calling a DLL.</span></span>
  
```cs
Excel4(xlGetInst, LPXLOPER pxRes, 0); /* returns low part only */
Excel12(xlGetInst, LPXLOPER12 pxRes, 0); /* returns full handle */
```

## <a name="parameters"></a><span data-ttu-id="30edc-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="30edc-107">Parameters</span></span>

<span data-ttu-id="30edc-108">Diese Funktion hat keine Argumente.</span><span class="sxs-lookup"><span data-stu-id="30edc-108">This function has no arguments.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="30edc-109">Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="30edc-109">Property value/Return value</span></span>

<span data-ttu-id="30edc-110">Das Instanzhandle (**xltypeInt**) wird im **Val.w-Feld** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="30edc-110">The instance handle (**xltypeInt**) will be in the **val.w** field.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="30edc-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="30edc-111">Remarks</span></span>

<span data-ttu-id="30edc-112">Diese Funktion kann verwendet werden, um zwischen mehreren ausgeführten Instanzen von Excel, die die DLL aufrufen, zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="30edc-112">This function can be used to distinguish between multiple running instances of Excel that are calling the DLL.</span></span>
  
<span data-ttu-id="30edc-113">Wenn Sie diese Funktion mithilfe von [Excel4](excel4-excel12.md) oder [Excel4v](excel4v-excel12v.md)aufrufen, ist die zurückgegebene XLOPER-Ganzzahlvariable eine signierte 16-Bit-Short-Int. Dies kann nur die niedrigen 16 Bit des 32-Bit-Windows enthalten.</span><span class="sxs-lookup"><span data-stu-id="30edc-113">When you are calling this function using [Excel4](excel4-excel12.md) or [Excel4v](excel4v-excel12v.md), the returned XLOPER integer variable is a signed 16-bit short int. This is only capable of containing the low 16 bits of the 32-bit Windows handle.</span></span> <span data-ttu-id="30edc-114">Ab Excel 2007 ist die ganzzahlige Variable des **XLOPER12** ein signiertes 32-Bit-Int und enthält daher das gesamte Handle, ohne dass alle geöffneten Fenster durch iteriert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="30edc-114">Starting in Excel 2007, the integer variable of the **XLOPER12** is a signed 32-bit int and therefore contains the entire handle, removing the need to iterate all open windows.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="30edc-115">Wenn die **xlGetInst-Funktion** mit der 64-Bit-Version von Microsoft Excel verwendet wird, kann die Funktion fehlschlagen.</span><span class="sxs-lookup"><span data-stu-id="30edc-115">If the **xlGetInst** function is used with the 64-bit version of Microsoft Excel, then the function will fail.</span></span> <span data-ttu-id="30edc-116">Dies liegt daran, dass der **xltypeInt-Werttyp** nicht breit genug ist, um den 64-Bit-Long-Handle zu halten, der von Excel in diesem Fall zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="30edc-116">This is because the **xltypeInt** value type is not wide enough to hold the 64-bit long handle returned by Excel in this case.</span></span> <span data-ttu-id="30edc-117">Zu diesem Zweck wurde Excel 2010 eine neue Funktion namens [xlGetInstPtr](xlgetinstptr.md)eingeführt, die sowohl mit der 32-Bit- als auch der 64-Bit-Version von Excel.</span><span class="sxs-lookup"><span data-stu-id="30edc-117">For this purpose, Excel 2010 introduced a new function named [xlGetInstPtr](xlgetinstptr.md), which runs correctly with both the 32-bit and 64-bit versions of Excel.</span></span> 
  
## <a name="example"></a><span data-ttu-id="30edc-118">Beispiel</span><span class="sxs-lookup"><span data-stu-id="30edc-118">Example</span></span>

<span data-ttu-id="30edc-119">Im folgenden Beispiel wird die Instanz der letzten Kopie von Excel, die sie aufgerufen hat, mit der aktuellen Kopie von Excel, die sie aufgerufen hat, verglichen.</span><span class="sxs-lookup"><span data-stu-id="30edc-119">The following example compares the instance of the last copy of Excel that called it to the current copy of Excel that called it.</span></span> <span data-ttu-id="30edc-120">Wenn sie identisch sind, wird 1 zurückgegeben. Andern falls nicht, wird 0 zurückgegeben. Wenn die Funktion fehlschlägt, gibt sie -1 zurück.</span><span class="sxs-lookup"><span data-stu-id="30edc-120">If they are the same, it returns 1; if not, it returns 0; if the function fails, it returns -1.</span></span>
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlGetInstExample(void)
{
    XLOPER12 xRes;
    static HANDLE hOld = 0;
    short iRet;
    if (Excel12(xlGetInst, &xRes, 0) != xlretSuccess)
        iRet = -1;
    else
    {
    HANDLE hNew;
    hNew = (HANDLE)xRes.val.w;
    if (hNew != hOld)
            iRet = 0;
    else
            iRet = 1;
    hOld = hNew;
    }
    return iRet;
}
```

## <a name="see-also"></a><span data-ttu-id="30edc-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="30edc-121">See also</span></span>



[<span data-ttu-id="30edc-122">xlGetHwnd</span><span class="sxs-lookup"><span data-stu-id="30edc-122">xlGetHwnd</span></span>](xlgethwnd.md)
  
[<span data-ttu-id="30edc-123">xlGetInstPtr</span><span class="sxs-lookup"><span data-stu-id="30edc-123">xlGetInstPtr</span></span>](xlgetinstptr.md)


[<span data-ttu-id="30edc-124">C-API-Funktionen, die nur aus einer DLL oder XLL aufgerufen werden können</span><span class="sxs-lookup"><span data-stu-id="30edc-124">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

