---
title: Funktionen in allgemeinen DLL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- generic dll [excel 2007], functions,functions [Excel 2007], Generic DLL
localization_priority: Normal
ms.assetid: 80ce2247-d69d-45b0-b5e2-4ff0d7078a2c
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 3064e1a09ad8850e121da678f3702a6236574599
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420598"
---
# <a name="functions-in-the-generic-dll"></a><span data-ttu-id="ceafc-104">Funktionen in allgemeinen DLL</span><span class="sxs-lookup"><span data-stu-id="ceafc-104">Functions in the Generic DLL</span></span>

 <span data-ttu-id="ceafc-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="ceafc-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="ceafc-106">Der Ordner enthält Microsoft Visual Studio Projektdateien und Quellcodedateien, die zum `\EXAMPLES\GENERIC\` Kompilieren der Beispiel-DLL GENERIC.xll erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="ceafc-106">The folder  `\EXAMPLES\GENERIC\` contains Microsoft Visual Studio project files and source code files that are needed to compile the example DLL GENERIC.xll.</span></span> <span data-ttu-id="ceafc-107">Sie können dieses Projekt als Vorlage zum Schreiben eigener xlLs Microsoft Excel verwenden.</span><span class="sxs-lookup"><span data-stu-id="ceafc-107">You can use this project as a template for writing your own Microsoft Excel XLLs.</span></span> <span data-ttu-id="ceafc-108">Der Quellcode in diesem Projekt veranschaulicht viele der Features der Excel C-API.</span><span class="sxs-lookup"><span data-stu-id="ceafc-108">The source code in this project demonstrates many of the features of the Excel C API.</span></span> 
  
<span data-ttu-id="ceafc-109">Beim Laden von GENERIC.xll wird ein neues Menü **"Generic"** mit vier Befehlen erstellt:</span><span class="sxs-lookup"><span data-stu-id="ceafc-109">When you load GENERIC.xll, it creates a new **Generic** menu with four commands:</span></span> 
  
- <span data-ttu-id="ceafc-110">**Dialogfeld** – Zeigt ein Microsoft Excel an.</span><span class="sxs-lookup"><span data-stu-id="ceafc-110">**Dialog** - Displays a Microsoft Excel dialog box.</span></span> 
    
- <span data-ttu-id="ceafc-111">**Tanz** – Verschiebt die Auswahl, bis Sie die **ESC-TASTE** drücken.</span><span class="sxs-lookup"><span data-stu-id="ceafc-111">**Dance** - Moves the selection around until you press the **ESC** key.</span></span> 
    
- <span data-ttu-id="ceafc-112">**Systemeigenes** Dialogfeld – Zeigt ein Windows dialogfeld an.</span><span class="sxs-lookup"><span data-stu-id="ceafc-112">**Native Dialog** - Displays a Windows dialog box.</span></span> 
    
- <span data-ttu-id="ceafc-113">**Exit** – Entladen Sie GENERIC.xll und entfernt das Menü **Generisch.**</span><span class="sxs-lookup"><span data-stu-id="ceafc-113">**Exit** - Unloads GENERIC.xll and removes the **Generic** menu.</span></span> 
    
<span data-ttu-id="ceafc-114">GENERIC.xll bietet außerdem drei Arbeitsblattfunktionen, Func1, FuncSum und FuncFib, die verwendet werden können, wenn GENERIC.xll geladen wird.</span><span class="sxs-lookup"><span data-stu-id="ceafc-114">GENERIC.xll also provides three worksheet functions, Func1, FuncSum, and FuncFib, which can be used whenever GENERIC.xll is loaded.</span></span> <span data-ttu-id="ceafc-115">GENERIC.xll kann mit dem Add-In-Manager geladen werden, oder es wird geladen, wenn es am normalen Ende der letzten Sitzung aktiv Excel war.</span><span class="sxs-lookup"><span data-stu-id="ceafc-115">GENERIC.xll can be loaded using the Add-in Manager, or it is loaded if it was active at the normal end of the last Excel session.</span></span>
  
<span data-ttu-id="ceafc-116">Dieses Projekt verwendet die Framework library (FRMWRK32.lib).</span><span class="sxs-lookup"><span data-stu-id="ceafc-116">This project uses the framework library (FRMWRK32.lib).</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="ceafc-117">Inhalt dieses Abschnitts</span><span class="sxs-lookup"><span data-stu-id="ceafc-117">In this section</span></span>

[<span data-ttu-id="ceafc-118">DIALOGMsgProc</span><span class="sxs-lookup"><span data-stu-id="ceafc-118">DIALOGMsgProc</span></span>](dialogmsgproc.md)
  
[<span data-ttu-id="ceafc-119">ExcelCursorProc</span><span class="sxs-lookup"><span data-stu-id="ceafc-119">ExcelCursorProc</span></span>](excelcursorproc.md)
  
[<span data-ttu-id="ceafc-120">HookExcelWindow</span><span class="sxs-lookup"><span data-stu-id="ceafc-120">HookExcelWindow</span></span>](hookexcelwindow.md)
  
[<span data-ttu-id="ceafc-121">UnhookExcelWindow</span><span class="sxs-lookup"><span data-stu-id="ceafc-121">UnhookExcelWindow</span></span>](unhookexcelwindow.md)
  
[<span data-ttu-id="ceafc-122">fShowDialog</span><span class="sxs-lookup"><span data-stu-id="ceafc-122">fShowDialog</span></span>](fshowdialog.md)
  
[<span data-ttu-id="ceafc-123">fDance</span><span class="sxs-lookup"><span data-stu-id="ceafc-123">fDance</span></span>](fdance.md)
  
[<span data-ttu-id="ceafc-124">fDialog/fDialog12</span><span class="sxs-lookup"><span data-stu-id="ceafc-124">fDialog/fDialog12</span></span>](fdialog-fdialog12.md)
  
[<span data-ttu-id="ceafc-125">fExit</span><span class="sxs-lookup"><span data-stu-id="ceafc-125">fExit</span></span>](fexit.md)
  
[<span data-ttu-id="ceafc-126">Func1</span><span class="sxs-lookup"><span data-stu-id="ceafc-126">Func1</span></span>](func1.md)
  
[<span data-ttu-id="ceafc-127">FuncSum</span><span class="sxs-lookup"><span data-stu-id="ceafc-127">FuncSum</span></span>](funcsum.md)
  
[<span data-ttu-id="ceafc-128">FuncFib</span><span class="sxs-lookup"><span data-stu-id="ceafc-128">FuncFib</span></span>](funcfib.md)
  
## <a name="see-also"></a><span data-ttu-id="ceafc-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ceafc-129">See also</span></span>



[<span data-ttu-id="ceafc-130">Funktionen in der Framework-Klassenbibliothek</span><span class="sxs-lookup"><span data-stu-id="ceafc-130">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

