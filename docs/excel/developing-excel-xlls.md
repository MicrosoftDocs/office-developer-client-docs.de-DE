---
title: Entwickeln von Excel-XLLs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- -Add-ins - [excel 2007], Entwickeln von XLLs - [Excel 2007], XLLs - [Excel 2007], entwickeln
localization_priority: Normal
ms.assetid: dd27ae4d-ef97-47db-885c-ddd955816900
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: cb2483b9cd1b11bcfeee81bba02b6d593e8818fc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790403"
---
# <a name="developing-excel-xlls"></a><span data-ttu-id="8c5d1-104">Entwickeln von Excel-XLLs</span><span class="sxs-lookup"><span data-stu-id="8c5d1-104">Developing Excel XLLs</span></span>

<span data-ttu-id="8c5d1-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="8c5d1-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="8c5d1-p101">Der Hauptgrund f�r das Schreiben von Microsoft Excel XLLs und verwenden der C-API ist die Erstellung von Hochleistungs-Tabellenfunktionen. Die Anwendungsszenarien leistungsstarker Funktionen � und ab Excel 2007 die M�glichkeit, Multithread-Schnittstellen auf leistungsstarke Serverressourcen zu schreiben � machen sie zu einem wichtigen Bestandteil der Excel-Erweiterbarkeit. Die Leistung von XLLs wurde in Excel 2007 durch das Hinzuf�gen neuer Datentypen und die Unterst�tzung von Multithreading weiter verbessert.</span><span class="sxs-lookup"><span data-stu-id="8c5d1-p101">The primary reason for writing Microsoft Excel XLLs and using the C API is to create high-performance worksheet functions. The applications of high-performance functions—and, starting in Excel 2007, the ability to write multithreaded interfaces to powerful server resources—make it a very important part of Excel extensibility. The performance of XLLs was further enhanced in Excel 2007 by the addition of new data types and, most important, support for multithreading.</span></span>
  
<span data-ttu-id="8c5d1-p102">Die C-API verf�gt nicht �ber die leistungsstarken Features zur schnellen Entwicklung von Microsoft Visual Basic for Applications (VBA) �ber COM oder Microsoft .NET Framework. Die Speicherverwaltung ist lediglich rudiment�r, weswegen mehr Verantwortung beim Entwickler liegt. Viele Excel-Features, die �ber COM durch VBA und .NET Framework verf�gbar sind, sind in der C-API nicht verf�gbar.</span><span class="sxs-lookup"><span data-stu-id="8c5d1-p102">The C API has none of the higher-level rapid development features of Microsoft Visual Basic for Applications (VBA), COM, or the Microsoft .NET Framework. Memory management is low level, and therefore puts greater responsibility on the developer. Many Excel features that are exposed through COM, making them available through VBA and the .NET Framework, are not exposed to the C API.</span></span>


- [<span data-ttu-id="8c5d1-112">Excel-Programmierkonzepte</span><span class="sxs-lookup"><span data-stu-id="8c5d1-112">Excel Programming Concepts</span></span>](excel-programming-concepts.md)
  
- [<span data-ttu-id="8c5d1-113">Arbeiten mit DLLs</span><span class="sxs-lookup"><span data-stu-id="8c5d1-113">Working with DLLs</span></span>](working-with-dlls.md)
  
- [<span data-ttu-id="8c5d1-114">Zugriff auf XLL-Code in Excel (engl.)</span><span class="sxs-lookup"><span data-stu-id="8c5d1-114">Accessing XLL Code in Excel</span></span>](accessing-xll-code-in-excel.md)
  
- [<span data-ttu-id="8c5d1-115">Anruf XLL-Funktionen aus der Funktions-Assistenten oder Dialogfelder ersetzen</span><span class="sxs-lookup"><span data-stu-id="8c5d1-115">Call XLL Functions from the Function Wizard or Replace Dialog Boxes</span></span>](how-to-call-xll-functions-from-the-function-wizard-or-replace-dialog-boxes.md)
  
- [<span data-ttu-id="8c5d1-116">Aufrufen von Excel von der DLL oder XLL aus</span><span class="sxs-lookup"><span data-stu-id="8c5d1-116">Calling into Excel from the DLL or XLL</span></span>](calling-into-excel-from-the-dll-or-xll.md)
  
- [<span data-ttu-id="8c5d1-117">Erstellen von XLLs</span><span class="sxs-lookup"><span data-stu-id="8c5d1-117">Creating XLLs</span></span>](creating-xlls.md)
  
- [<span data-ttu-id="8c5d1-118">Auswerten von Namen und andere Arbeitsblatt Formula-Ausdr�cke</span><span class="sxs-lookup"><span data-stu-id="8c5d1-118">Evaluating Names and Other Worksheet Formula Expressions</span></span>](evaluating-names-and-other-worksheet-formula-expressions.md)
  
- [<span data-ttu-id="8c5d1-119">Multithreading und Speicherverwaltung</span><span class="sxs-lookup"><span data-stu-id="8c5d1-119">Multithreading and Memory Management</span></span>](multithreading-and-memory-management.md)
  
- [<span data-ttu-id="8c5d1-120">Asynchrone benutzerdefinierte Funktionen</span><span class="sxs-lookup"><span data-stu-id="8c5d1-120">Asynchronous User-Defined Functions</span></span>](asynchronous-user-defined-functions.md)
  
- [<span data-ttu-id="8c5d1-121">Clustersichere Funktionen</span><span class="sxs-lookup"><span data-stu-id="8c5d1-121">Cluster Safe Functions</span></span>](cluster-safe-functions.md)
  
- [<span data-ttu-id="8c5d1-122">Genehmigungsverfahren Benutzer Zeilenumbr�che in langen Vorg�nge</span><span class="sxs-lookup"><span data-stu-id="8c5d1-122">Permitting User Breaks in Lengthy Operations</span></span>](permitting-user-breaks-in-lengthy-operations.md)
  
- [<span data-ttu-id="8c5d1-123">Anzeigen von Dialogfeldern aus innerhalb einer DLL oder XLL</span><span class="sxs-lookup"><span data-stu-id="8c5d1-123">Displaying Dialog Boxes from Within a DLL or XLL</span></span>](displaying-dialog-boxes-from-within-a-dll-or-xll.md)
  
- [<span data-ttu-id="8c5d1-124">Zugriff auf Excel-Instanz und im Hauptfenster von Handles</span><span class="sxs-lookup"><span data-stu-id="8c5d1-124">Access Excel Instance and Main Window Handles</span></span>](how-to-access-excel-instance-and-main-window-handles.md)
  
- [<span data-ttu-id="8c5d1-125">Abw�rtskompatibilit�t</span><span class="sxs-lookup"><span data-stu-id="8c5d1-125">Backward Compatibility</span></span>](backward-compatibility.md)
  
