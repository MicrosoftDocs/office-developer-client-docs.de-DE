---
title: RUNMACRO-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033809
localization_priority: Normal
ms.assetid: 86b0f071-5e0b-56de-ff5b-63c114ad823a
description: Ruft ein Makro in einem Microsoft Visual Basic for Applications (VBA)-Projekt auf.
ms.openlocfilehash: 77045bd67fe9be9aab14e73199b33b93c6d70c2c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428088"
---
# <a name="runmacro-function"></a><span data-ttu-id="65a8b-103">RUNMACRO Function</span><span class="sxs-lookup"><span data-stu-id="65a8b-103">RUNMACRO Function</span></span>

<span data-ttu-id="65a8b-104">Ruft ein Makro in einem Microsoft Visual Basic for Applications (VBA)-Projekt auf.</span><span class="sxs-lookup"><span data-stu-id="65a8b-104">Calls a macro in a Microsoft Visual Basic for Applications (VBA) project.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="65a8b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="65a8b-105">Syntax</span></span>

<span data-ttu-id="65a8b-106">RUNMACRO (\*\* *macroname* \*\* [, \*\* *projname_opt* \*\* ])</span><span class="sxs-lookup"><span data-stu-id="65a8b-106">RUNMACRO (\*\* *macroname* \*\* [, \*\* *projname_opt* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="65a8b-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="65a8b-107">Parameters</span></span>

|<span data-ttu-id="65a8b-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="65a8b-108">**Name**</span></span>|<span data-ttu-id="65a8b-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="65a8b-109">**Required/Optional**</span></span>|<span data-ttu-id="65a8b-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="65a8b-110">**Data Type**</span></span>|<span data-ttu-id="65a8b-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="65a8b-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="65a8b-112">_macroname_</span><span class="sxs-lookup"><span data-stu-id="65a8b-112">_macroname_</span></span> <br/> |<span data-ttu-id="65a8b-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="65a8b-113">Required</span></span>  <br/> |<span data-ttu-id="65a8b-114">**String**</span><span class="sxs-lookup"><span data-stu-id="65a8b-114">**String**</span></span> <br/> |<span data-ttu-id="65a8b-115">Der Name des aufzurufenden Makros.</span><span class="sxs-lookup"><span data-stu-id="65a8b-115">The name of the macro to call.</span></span>  <br/> |
| <span data-ttu-id="65a8b-116">_projname_opt_</span><span class="sxs-lookup"><span data-stu-id="65a8b-116">_projname_opt_</span></span> <br/> |<span data-ttu-id="65a8b-117">Optional</span><span class="sxs-lookup"><span data-stu-id="65a8b-117">Optional</span></span>  <br/> |<span data-ttu-id="65a8b-118">**String**</span><span class="sxs-lookup"><span data-stu-id="65a8b-118">**String**</span></span> <br/> | <span data-ttu-id="65a8b-119">Das Projekt, das den Makro enthält.</span><span class="sxs-lookup"><span data-stu-id="65a8b-119">The project that contains the macro.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="65a8b-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="65a8b-120">Remarks</span></span>

<span data-ttu-id="65a8b-121">Wenn ein Projekt angegeben wird, überprüft Microsoft Visio alle  geöffneten Dokumente auf das Dokument, das projname_opt enthält, und ruft den _Makronamen_ in diesem Projekt auf.</span><span class="sxs-lookup"><span data-stu-id="65a8b-121">If a project is specified, Microsoft Visio scans all open documents for the one containing  _projname_opt_ and calls  _macroname_ in that project.</span></span> <span data-ttu-id="65a8b-122">Wenn  _projname_opt_ oder Null ("") ausgelassen wird, wird davon ausgegangen, dass  _sich macroname_ im #A0 des Dokuments befindet, das die zu bewertende RUNMACRO-Formel enthält.</span><span class="sxs-lookup"><span data-stu-id="65a8b-122">If  _projname_opt_ is omitted or null (""),  _macroname_ is assumed to be in the VBA project of the document that contains the RUNMACRO formula being evaluated.</span></span> 
  
<span data-ttu-id="65a8b-123">Die RUNMACRO-Funktion unterscheidet sich von der CALLTHIS-Funktion, da sie keinen Verweis auf die Form übernimmt, deren Name die Formel ist, die an _macroname ausgewertet wird._</span><span class="sxs-lookup"><span data-stu-id="65a8b-123">The RUNMACRO function differs from the CALLTHIS function in that it does not pass a reference to the shape that owns the formula being evaluated to  _macroname_.</span></span> <span data-ttu-id="65a8b-124">Wie CALLTHIS erfordert die RUNMACRO-Funktion keinen Verweis  _auf_ projname_opt aufrufen.</span><span class="sxs-lookup"><span data-stu-id="65a8b-124">Like CALLTHIS, the RUNMACRO function doesn't require a reference to  _projname_opt_ to call into it.</span></span> 
  
 <span data-ttu-id="65a8b-125">VBA-Code, der aufgerufen wird, wenn die Visio-Instanz eine RUNMACRO-Funktion in einer Formel auswertet, darf das Dokument mit der Zelle, die die Funktion verwendet, nicht schließen, da dies zu einem Anwendungsfehler führt und Visio beendet wird.</span><span class="sxs-lookup"><span data-stu-id="65a8b-125">VBA code that is invoked when the Visio instance evaluates a RUNMACRO function in a formula should not close the document containing the cell using the function because an application error results and Visio terminates.</span></span> 
  
<span data-ttu-id="65a8b-126">Wenn Sie das Dokument mit der Zelle, die die RUNMACRO-Funktion verwendet, schließen müssen, wenden Sie eines der folgenden Verfahren an:</span><span class="sxs-lookup"><span data-stu-id="65a8b-126">If you need to close the document containing the cell that uses the RUNMACRO function, use one of the following techniques:</span></span>
  
- <span data-ttu-id="65a8b-127">Schließen Sie das Dokument über anderen Code als VBA-Code.</span><span class="sxs-lookup"><span data-stu-id="65a8b-127">Close the document from code that is not VBA.</span></span>
    
- <span data-ttu-id="65a8b-128">Schließen Sie das Dokument von einem anderen Projekt aus als von jenem, das gerade geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="65a8b-128">Close the document from a project other than the one that is closing.</span></span>
    
- <span data-ttu-id="65a8b-129">Fügen Sie Fenster-Nachrichten zum Schließen der Fenster ein, anstatt das Dokument zu schließen.</span><span class="sxs-lookup"><span data-stu-id="65a8b-129">Post window messages to close windows in the document rather than closing the document.</span></span>
    
<span data-ttu-id="65a8b-130">Weitere Informationen zum Ausführen von Code in Visio finden Sie unter [Informationen zu Sicherheitseinstellungen und zum Ausführen von Code in Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) in dieser ShapeSheet-Referenz.</span><span class="sxs-lookup"><span data-stu-id="65a8b-130">For more information about running code in Visio, see [About security settings and running code in Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) in this ShapeSheet Reference.</span></span> 
  
## <a name="example"></a><span data-ttu-id="65a8b-131">Beispiel</span><span class="sxs-lookup"><span data-stu-id="65a8b-131">Example</span></span>

<span data-ttu-id="65a8b-132">Im folgenden Beispiel wird das Makro MyTest im Klassenmodul ThisDocument des VBA-Projekts aufgerufen, das die RUNMACRO-Formel enthält.</span><span class="sxs-lookup"><span data-stu-id="65a8b-132">The following example invokes a macro called MyTest in the ThisDocument class module of the VBA project containing the RUNMACRO formula.</span></span> 
  
<span data-ttu-id="65a8b-133">RUNMACRO ("ThisDocument.MyTest")</span><span class="sxs-lookup"><span data-stu-id="65a8b-133">RUNMACRO ("ThisDocument.MyTest")</span></span> 
  

