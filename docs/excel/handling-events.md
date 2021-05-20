---
title: Behandeln von Ereignissen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: b67fcb83-a0e2-4349-88f5-bcc181306eac
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: c989bc39c22f4e566c18feb4fdeaa8582c5525f2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438267"
---
# <a name="handling-events"></a><span data-ttu-id="b8c43-103">Behandeln von Ereignissen</span><span class="sxs-lookup"><span data-stu-id="b8c43-103">Handling Events</span></span>

 <span data-ttu-id="b8c43-104">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="b8c43-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="b8c43-105">Ab Excel 2010 können XLLs Ereignisse empfangen, die zum Verwalten des asynchronen Funktionslebenszyklus entwickelt wurden.</span><span class="sxs-lookup"><span data-stu-id="b8c43-105">Starting in Excel 2010, XLLs can receive events designed to manage the asynchronous function life cycle.</span></span> <span data-ttu-id="b8c43-106">Die Ereignisse sind wie folgt:</span><span class="sxs-lookup"><span data-stu-id="b8c43-106">The events are as follows:</span></span>
  
- <span data-ttu-id="b8c43-107">**CalculationEnded**: Wird ausgelöst, wenn Excel Berechnung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="b8c43-107">**CalculationEnded**: Raised when Excel is finished calculating.</span></span> <span data-ttu-id="b8c43-108">Nach diesem Ereignis können Sie ressourcen frei, die während der Berechnung zugewiesen wurden.</span><span class="sxs-lookup"><span data-stu-id="b8c43-108">After this event, you can free resources allocated during the calculation.</span></span>
    
- <span data-ttu-id="b8c43-109">**CalculationCanceled**: Wird ausgelöst, wenn der Benutzer die Berechnung unterbricht.</span><span class="sxs-lookup"><span data-stu-id="b8c43-109">**CalculationCanceled**: Raised when the user interrupts the calculation.</span></span> <span data-ttu-id="b8c43-110">Die XLL beendet alle asynchronen Aktivitäten.</span><span class="sxs-lookup"><span data-stu-id="b8c43-110">The XLL stops any asynchronous activities.</span></span> <span data-ttu-id="b8c43-111">Unmittelbar nach diesem Ereignis wird **das CalculationEnded-Ereignis** ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="b8c43-111">Immediately following this event, the **CalculationEnded** event is raised.</span></span> 
    
<span data-ttu-id="b8c43-112">Zum Behandeln dieser Ereignisse verwendet die XLL die C-API-Funktion [xlEventRegister](xleventregister.md).</span><span class="sxs-lookup"><span data-stu-id="b8c43-112">To handle these events, the XLL uses the C API function [xlEventRegister](xleventregister.md).</span></span> 
  
> [!NOTE]
> <span data-ttu-id="b8c43-113">**CalculationEnded** und **CalculationCanceled** werden während der programmgesteuerten Neuberechnung nicht ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="b8c43-113">**CalculationEnded** and **CalculationCanceled** are not raised during programmatic recalculation.</span></span> 
  

