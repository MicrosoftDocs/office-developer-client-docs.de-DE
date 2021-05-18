---
title: xlAsyncReturn
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 159bc9bf-8dd5-4cd2-8384-474c74a3f112
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 32d5075af34cda9753c5d082bd4ab00afab1ecff
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414109"
---
# <a name="xlasyncreturn"></a><span data-ttu-id="039bd-103">xlAsyncReturn</span><span class="sxs-lookup"><span data-stu-id="039bd-103">xlAsyncReturn</span></span>

<span data-ttu-id="039bd-104">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="039bd-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="039bd-105">Wird verwendet, um das Ergebnis einer asynchronen benutzerdefinierten Funktion (User-Defined Function, UDF) zurück zu geben.</span><span class="sxs-lookup"><span data-stu-id="039bd-105">Used to return the result of an asynchronous user-defined function (UDF).</span></span>
  
```cpp
Excel12(xlAsyncReturn, LPXLOPER12 pxRes, 2, LPXLOPER12 pxAsyncHandle, LPXLOPER12 pxFunctionResult);
```

## <a name="parameters"></a><span data-ttu-id="039bd-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="039bd-106">Parameters</span></span>

<span data-ttu-id="039bd-107">_pxAsyncHandle_ (**xltypeBigData**)</span><span class="sxs-lookup"><span data-stu-id="039bd-107">_pxAsyncHandle_ (**xltypeBigData**)</span></span>
  
<span data-ttu-id="039bd-108">Das asynchrone Handle der UDF, an die das Ergebnis zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="039bd-108">The asynchronous handle of the UDF to which the result is returned.</span></span>
  
<span data-ttu-id="039bd-109">_pxFunctionResult_</span><span class="sxs-lookup"><span data-stu-id="039bd-109">_pxFunctionResult_</span></span>
  
<span data-ttu-id="039bd-110">Der Rückgabewert der UDF.</span><span class="sxs-lookup"><span data-stu-id="039bd-110">The return value of the UDF.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="039bd-111">Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="039bd-111">Property value/Return value</span></span>

<span data-ttu-id="039bd-112">Wenn dies erfolgreich ist, wird **TRUE** (**xltypeBool**) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="039bd-112">If successful, returns **TRUE** (**xltypeBool**).</span></span> <span data-ttu-id="039bd-113">Wenn der Wert nicht erfolgreich ist, wird **FALSE zurückgegeben.**</span><span class="sxs-lookup"><span data-stu-id="039bd-113">If unsuccessful, returns **FALSE**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="039bd-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="039bd-114">Remarks</span></span>

<span data-ttu-id="039bd-115">**xlAsyncReturn** ist der einzige Rückruf, Excel nicht berechnungsfreie Threads während der Neuberechnung zulässt.</span><span class="sxs-lookup"><span data-stu-id="039bd-115">**xlAsyncReturn** is the only callback Excel allows on non-calculation threads during recalculation.</span></span> <span data-ttu-id="039bd-116">Der asynchrone Teil einer asynchronen UDF darf keine anderen Rückrufe als **xlAsyncReturn ausführen.**</span><span class="sxs-lookup"><span data-stu-id="039bd-116">The asynchronous portion of an asynchronous UDF must not perform any callbacks other than **xlAsyncReturn**.</span></span> <span data-ttu-id="039bd-117">Die XLL muss speicherplatz frei, der für den Rückgabewert reserviert ist.</span><span class="sxs-lookup"><span data-stu-id="039bd-117">The XLL must free memory allocated to hold the return value.</span></span>
  
<span data-ttu-id="039bd-118">Die _Parameter pxAsyncHandle_ und  _pxFunctionResult_ können auch vom Typ **xltypeMulti** sein, wenn sie zum Zurückgeben eines Arrays von Handles und entsprechenden Werten in einem einzelnen Rückruf verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="039bd-118">The _pxAsyncHandle_ and  _pxFunctionResult_ parameters can also be of type **xltypeMulti** when used to return an array of handles and corresponding values in a single callback.</span></span> <span data-ttu-id="039bd-119">Übergeben Sie bei Verwendung eines einzelnen Rückrufs eine LPXLOPER12, die auf XLOPER12-Strukturen verweist, die eindimensionale Arrays enthalten, die die asynchronen Ziehpunkte und Rückgabewerte enthalten.</span><span class="sxs-lookup"><span data-stu-id="039bd-119">When using a single callback, pass an LPXLOPER12 that points to XLOPER12 structures that contain one dimensional arrays that contain the asynchronous handles and return values.</span></span> <span data-ttu-id="039bd-120">Diese Arrays müssen sich in derselben Reihenfolge befinden, Excel einem asynchronen Handle mit dem entsprechenden Wert korrekt entspricht.</span><span class="sxs-lookup"><span data-stu-id="039bd-120">These arrays must be in the same order for Excel to correctly match an asynchronous handle with its corresponding value.</span></span> 
  
<span data-ttu-id="039bd-121">Das folgende Beispiel zeigt, wie Sie einen Batchaufruf mit **xlAsyncReturn erstellen können.**</span><span class="sxs-lookup"><span data-stu-id="039bd-121">The following example shows how you can make a batch call using **xlAsyncReturn**.</span></span>
  
```cpp
int batchSize = 10;
    LPXLOPER12 pHandles = new XLOPER12[batchSize];
    LPXLOPER12 pValues = new XLOPER12[batchSize];
    /*Add code to fill in LPXLOPER12 arrays (pHandles and pValues)
    with the XOPER12 structures that contain the asynchronous handles
    and values, in respective order*/
    //Create an XLOPER12 of type xltypeMulti, and fill the Handle array
    XLOPER12 handleArray;
    handleArray.xltype = xltypeMulti;
    handleArray.val.array.rows = 1;
    handleArray.val.array.columns = (COL)batchSize;
    handleArray.val.array.lparray = pHandles;
    
    //Create an XLOPER12 if type xltypeMulti, and fill the Values array
    XLOPER12 valueArray;
    valueArray.xltype = xltypeMulti;
    valueArray.val.array.rows = 1;
    valueArray.val.array.columns = (COL)batchSize;
    valueArray.val.array.lparray = pValues;
    //Make the callback with the return value
    int ret = Excel12(xlAsyncReturn, 0, 2, &amp;handleArray, &amp;valueArray);
    //Add code to free the allocated memory here (pHandles, pValues, valueArray, handleArray)
    return ret;

```

## <a name="see-also"></a><span data-ttu-id="039bd-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="039bd-122">See also</span></span>

- [<span data-ttu-id="039bd-123">Asynchrone benutzerdefinierte Funktionen</span><span class="sxs-lookup"><span data-stu-id="039bd-123">Asynchronous User-Defined Functions</span></span>](asynchronous-user-defined-functions.md)

