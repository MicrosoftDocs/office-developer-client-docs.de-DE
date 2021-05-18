---
title: XLOper12ToXLOper
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- XLOper12ToXLOper
keywords:
- xloper12toxloper-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: b46f87c4-778b-4502-be57-c3725f73a644
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 148353dcec1cc051aa44d18c0a081b6623e3759a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422908"
---
# <a name="xloper12toxloper"></a><span data-ttu-id="d1a73-104">XLOper12ToXLOper</span><span class="sxs-lookup"><span data-stu-id="d1a73-104">XLOper12ToXLOper</span></span>

<span data-ttu-id="d1a73-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="d1a73-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="d1a73-106">Konvertierungsroutine, die zum Konvertieren von der neuen **XLOPER12 in** die alte **XLOPER verwendet wird.**</span><span class="sxs-lookup"><span data-stu-id="d1a73-106">Conversion routine used to convert from the new **XLOPER12** to the old **XLOPER**.</span></span>
  
```cs
BOOL XLOper12ToXLOper(LPXLOPER12 pxloper12, LPXLOPER pxloper);
```

## <a name="parameters"></a><span data-ttu-id="d1a73-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="d1a73-107">Parameters</span></span>

<span data-ttu-id="d1a73-108">_pxloper12_ (**LPXLOPER12**)</span><span class="sxs-lookup"><span data-stu-id="d1a73-108">_pxloper12_ (**LPXLOPER12**)</span></span>
  
<span data-ttu-id="d1a73-109">Zeiger auf die zu **konvertierte XlOPER12-Quelle.**</span><span class="sxs-lookup"><span data-stu-id="d1a73-109">Pointer to the source **XLOPER12** to be converted.</span></span> 
  
<span data-ttu-id="d1a73-110">_pxloper_ (**LPXLOPER**)</span><span class="sxs-lookup"><span data-stu-id="d1a73-110">_pxloper_ (**LPXLOPER**)</span></span>
  
<span data-ttu-id="d1a73-111">Zeiger auf das **XlOPER-Ziel,** das den konvertierten Wert enthalten soll.</span><span class="sxs-lookup"><span data-stu-id="d1a73-111">Pointer to the target **XLOPER** to contain the converted value.</span></span> 
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="d1a73-112">Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d1a73-112">Property value/Return value</span></span>

<span data-ttu-id="d1a73-113">**TRUE,** wenn die Konvertierung erfolgreich war, **andernfalls FALSE.**</span><span class="sxs-lookup"><span data-stu-id="d1a73-113">**TRUE** if the conversion succeeded, **FALSE** otherwise.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="d1a73-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d1a73-114">Remarks</span></span>

<span data-ttu-id="d1a73-115">Je nach Typ der **XLOPER12** weist diese Funktion einen neuen Speicherpuffer für die konvertierten Werte zu, auf die im **XlOPER-Zielobjekt verwiesen wird.**</span><span class="sxs-lookup"><span data-stu-id="d1a73-115">Depending on the type of the **XLOPER12**, this function allocates a new memory buffer for the converted values, which are pointed to in the target **XLOPER**.</span></span> <span data-ttu-id="d1a73-116">Der Aufrufer ist dafür verantwortlich, alle der Kopie zugeordneten Arbeitsspeicher frei zu machen, wenn die Konvertierung erfolgreich war. **FreeXLOperT** kann verwendet werden, oder es kann direkt mithilfe von kostenlos **durchgeführt werden.**</span><span class="sxs-lookup"><span data-stu-id="d1a73-116">The caller is responsible for freeing any memory associated with the copy if the conversion is a success; **FreeXLOperT** can be used, or it can be done directly by using **free**.</span></span>
  
<span data-ttu-id="d1a73-117">Wenn die Konvertierung fehlschlägt, muss der Aufrufer keinen Arbeitsspeicher freispeichern.</span><span class="sxs-lookup"><span data-stu-id="d1a73-117">If the conversion fails, the caller does not need to free any memory.</span></span>
  
<span data-ttu-id="d1a73-118">Die Konvertierung von **einem XLOPER12** in einen **XLOPER** kann fehlschlagen, wenn **xlOPER12** ein Array oder einen Verweis enthält, das zu groß oder eine Zeichenfolge ist, die zu lang ist, damit **xlOPER** enthalten kann.</span><span class="sxs-lookup"><span data-stu-id="d1a73-118">Conversion from an **XLOPER12** to an **XLOPER** can fail when the **XLOPER12** contains an array or reference that is too large or a string that is too long for the **XLOPER** to contain.</span></span> 
  
<span data-ttu-id="d1a73-119">**XLOPER12** Unicode-Zeichenfolgen mit breiten  Zeichen werden auf eine vom Locale abhängige Weise in XLOPER-ASCII-Bytezeichenfolgen konvertiert.</span><span class="sxs-lookup"><span data-stu-id="d1a73-119">**XLOPER12** Unicode wide-character strings are converted to **XLOPER** ASCII byte strings in a way that is locale-dependent.</span></span> 
  
<span data-ttu-id="d1a73-120">**XlOPER12** **xltypeInt** ist eine ganzzahlige 32-Bit-Signierte, während **xlOPER** **xltypeInt** eine 16-Bit-ganze Zahl ist.</span><span class="sxs-lookup"><span data-stu-id="d1a73-120">The **XLOPER12** **xltypeInt** is a 32-bit signed integer, whereas the **XLOPER** **xltypeInt** is a 16-bit signed integer.</span></span> <span data-ttu-id="d1a73-121">Wenn eine angegebene **XLOPER12-Ganzzahl** den Grenzwert einer **XLOPER-Ganzzahl** überschreitet, wird die ganze Zahl in ein 8-Byte-Double konvertiert und in einem **XLOPER** vom Typ **xltypeNum** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d1a73-121">When a supplied **XLOPER12** integer exceeds the limit of an **XLOPER** integer, the integer is converted to an 8-byte double and returned in an **XLOPER** of type **xltypeNum**.</span></span> <span data-ttu-id="d1a73-122">Dies ist der einzige Fall, in dem diese Funktion den Typ des konvertierten **XLOPER ändert.**</span><span class="sxs-lookup"><span data-stu-id="d1a73-122">This is the only case in which this function changes the type of the converted **XLOPER**.</span></span>
  
### <a name="example"></a><span data-ttu-id="d1a73-123">Beispiel</span><span class="sxs-lookup"><span data-stu-id="d1a73-123">Example</span></span>

<span data-ttu-id="d1a73-124">In der Datei  `\SAMPLES\FRAMEWRK\FRAMEWRK.C` finden Sie den Code für diese Funktion.</span><span class="sxs-lookup"><span data-stu-id="d1a73-124">See the file  `\SAMPLES\FRAMEWRK\FRAMEWRK.C` for the code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d1a73-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d1a73-125">See also</span></span>

- [<span data-ttu-id="d1a73-126">Funktionen in der Framework-Klassenbibliothek</span><span class="sxs-lookup"><span data-stu-id="d1a73-126">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

