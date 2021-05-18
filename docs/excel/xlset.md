---
title: xlSet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlSet
keywords:
- xlset-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: 121e6212-0692-4430-97be-4792b53719bf
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 0912c1d40882933778d0df927ceb9de773063444
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404603"
---
# <a name="xlset"></a><span data-ttu-id="17299-104">xlSet</span><span class="sxs-lookup"><span data-stu-id="17299-104">xlSet</span></span>

<span data-ttu-id="17299-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="17299-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="17299-106">Legt konstante Werte sehr schnell in Zellen oder Bereiche.</span><span class="sxs-lookup"><span data-stu-id="17299-106">Puts constant values into cells or ranges very quickly.</span></span> <span data-ttu-id="17299-107">Weitere Informationen finden Sie unter "xlSet and Workbooks with Array Formulas" [unter Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span><span class="sxs-lookup"><span data-stu-id="17299-107">For more information, see "xlSet and Workbooks with Array Formulas" in [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span>
  
```cs
Excel12(xlSet, LPXLOPER12 pxRes, 2, LPXLOPER12 pxReference, LPXLOPER pxValue);
```

## <a name="parameters"></a><span data-ttu-id="17299-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="17299-108">Parameters</span></span>

<span data-ttu-id="17299-109">_pxReference_ (**xltypeRef** oder **xltypeSRef**)</span><span class="sxs-lookup"><span data-stu-id="17299-109">_pxReference_ (**xltypeRef** or **xltypeSRef**)</span></span>
  
<span data-ttu-id="17299-110">Ein rechteckiger Verweis, der die Zielzelle oder -zellen beschreibt.</span><span class="sxs-lookup"><span data-stu-id="17299-110">A rectangular reference describing the target cell or cells.</span></span> <span data-ttu-id="17299-111">Der Verweis muss benachbarte Zellen beschreiben, sodass in **einem xltypeRef** `val.mref.lpmref->count` auf 1 festgelegt werden muss.</span><span class="sxs-lookup"><span data-stu-id="17299-111">The reference must describe adjacent cells, so that in an **xltypeRef** `val.mref.lpmref->count` must be set to 1.</span></span> 
  
<span data-ttu-id="17299-112">_pxValue_</span><span class="sxs-lookup"><span data-stu-id="17299-112">_pxValue_</span></span>
  
<span data-ttu-id="17299-113">Der Wert oder die Werte, die in die Zelle oder Zellen platziert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="17299-113">The value or values to be placed into the cell or cells.</span></span> <span data-ttu-id="17299-114">Weitere Informationen finden Sie im Abschnitt "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="17299-114">For more information, see the "Remarks" section.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="17299-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="17299-115">Remarks</span></span>

### <a name="pxvalue-argument"></a><span data-ttu-id="17299-116">pxValue-Argument</span><span class="sxs-lookup"><span data-stu-id="17299-116">pxValue argument</span></span>

<span data-ttu-id="17299-117">_pxValue_ kann entweder ein Wert oder ein Array sein.</span><span class="sxs-lookup"><span data-stu-id="17299-117">_pxValue_ can either be a value or an array.</span></span> <span data-ttu-id="17299-118">Wenn es sich um einen Wert handelt, wird der gesamte Zielbereich mit diesem Wert gefüllt.</span><span class="sxs-lookup"><span data-stu-id="17299-118">If it is a value, the entire destination range is filled with that value.</span></span> <span data-ttu-id="17299-119">Wenn es sich um ein Array (**xltypeMulti)** handelt, werden die Elemente des Arrays an die entsprechenden Speicherorte im Rechteck eingesenert.</span><span class="sxs-lookup"><span data-stu-id="17299-119">If it is an array (**xltypeMulti**), the elements of the array are put into the corresponding locations in the rectangle.</span></span>
  
<span data-ttu-id="17299-120">Wenn Sie ein horizontales Array für das zweite Argument verwenden, wird es nach unten dupliziert, um das gesamte Rechteck zu füllen.</span><span class="sxs-lookup"><span data-stu-id="17299-120">If you use a horizontal array for the second argument, it is duplicated down to fill the entire rectangle.</span></span> <span data-ttu-id="17299-121">Wenn Sie ein vertikales Array verwenden, wird es nach rechts dupliziert, um das gesamte Rechteck zu füllen.</span><span class="sxs-lookup"><span data-stu-id="17299-121">If you use a vertical array, it is duplicated right to fill the entire rectangle.</span></span> <span data-ttu-id="17299-122">Wenn Sie ein rechteckiges Array verwenden und es zu klein für den rechteckigen Bereich ist, in den Sie es setzen möchten, wird dieser Bereich mit **#N/A-s gepolstert.**</span><span class="sxs-lookup"><span data-stu-id="17299-122">If you use a rectangular array, and it is too small for the rectangular range you want to put it in, that range is padded with **#N/A** s.</span></span>
  
<span data-ttu-id="17299-123">Wenn der Zielbereich kleiner als das Quellarray ist, werden die Werte bis zu den Grenzen des Zielbereichs kopiert, und die zusätzlichen Daten werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="17299-123">If the target range is smaller than the source array, the values are copied in up to the limits of the target range and the extra data are ignored.</span></span>
  
<span data-ttu-id="17299-124">Verwenden Sie ein **xltypeNil-Arrayelement** im Quellarray, um ein Element des Zielrechtecks zu löschen.</span><span class="sxs-lookup"><span data-stu-id="17299-124">To clear an element of the destination rectangle, use an **xltypeNil** type array element in the source array.</span></span> <span data-ttu-id="17299-125">Um das gesamte Zielrechteck zu löschen, lassen Sie das zweite Argument aus.</span><span class="sxs-lookup"><span data-stu-id="17299-125">To clear the entire destination rectangle, omit the second argument.</span></span> 
  
### <a name="restrictions"></a><span data-ttu-id="17299-126">Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="17299-126">Restrictions</span></span>

<span data-ttu-id="17299-127">**xlSet** kann nicht rückgängig gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="17299-127">**xlSet** cannot be undone.</span></span> <span data-ttu-id="17299-128">Darüber hinaus werden alle Zuvor verfügbaren Rückgängig-Informationen vernichtet.</span><span class="sxs-lookup"><span data-stu-id="17299-128">In addition, it destroys any undo information that may have been available before.</span></span> 
  
<span data-ttu-id="17299-129">**xlSet** kann nur Konstanten, nicht Formeln, in Zellen setzen.</span><span class="sxs-lookup"><span data-stu-id="17299-129">**xlSet** can put only constants, not formulas, into cells.</span></span> 
  
<span data-ttu-id="17299-130">**xlSet** verhält sich wie eine Befehlsentsprechungsfunktion der Klasse 3. Das heißt, sie ist nur innerhalb einer DLL verfügbar, wenn die DLL über ein  Objekt, ein Makro, ein Menü, eine Symbolleiste, eine Tastenkombination oder die Schaltfläche Ausführen im Dialogfeld **Makro** aufgerufen wird (zugriff auf die Registerkarte Ansicht auf dem Menüband ab Excel 2007 und das Menü **Extras** in früheren Versionen). </span><span class="sxs-lookup"><span data-stu-id="17299-130">**xlSet** behaves as a Class 3 command-equivalent function; that is, it is available only inside a DLL when the DLL is called from an object, macro, menu, toolbar, shortcut key, or the **Run** button in the **Macro** dialog box (accessed from **View** tab on the ribbon starting in Excel 2007, and the **Tools** menu in earlier versions).</span></span> 
  
## <a name="example"></a><span data-ttu-id="17299-131">Beispiel</span><span class="sxs-lookup"><span data-stu-id="17299-131">Example</span></span>

<span data-ttu-id="17299-132">Das folgende Beispiel füllt B205:B206 mit dem Wert aus, der von einem Makro übergeben wurde.</span><span class="sxs-lookup"><span data-stu-id="17299-132">The following example fills B205:B206 with the value that was passed in from a macro.</span></span> <span data-ttu-id="17299-133">Dieses Befehlsfunktionsbeispiel erfordert ein Argument und funktioniert nur, wenn es von einem XLM-Makroblatt oder von einem VBA-Modul mit der **Application.Run-Methode aufgerufen** wird.</span><span class="sxs-lookup"><span data-stu-id="17299-133">This command function example requires an argument, and so will only work if called from an XLM macro sheet, or from a VBA module using the **Application.Run** method.</span></span> 
  
`\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlSetExample(short int iVal)
{
   XLOPER12 xRef, xValue;
   xRef.xltype = xltypeSRef;
   xRef.val.sref.count = 1;
   xRef.val.sref.ref.rwFirst = 204;
   xRef.val.sref.ref.rwLast = 205;
   xRef.val.sref.ref.colFirst = 1;
   xRef.val.sref.ref.colLast = 1;
   xValue.xltype = xltypeInt;
   xValue.val.w = iVal;
   Excel12(xlSet, 0, 2, (LPXLOPER12)&xRef, (LPXLOPER12)&xValue);
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="17299-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="17299-134">See also</span></span>

- [<span data-ttu-id="17299-135">xlCoerce</span><span class="sxs-lookup"><span data-stu-id="17299-135">xlCoerce</span></span>](xlcoerce.md)
- [<span data-ttu-id="17299-136">C-API-Funktionen, die nur aus einer DLL oder XLL aufgerufen werden können</span><span class="sxs-lookup"><span data-stu-id="17299-136">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

