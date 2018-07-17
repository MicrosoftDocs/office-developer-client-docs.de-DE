---
title: Zelle "Prompt" (Abschnitt "User-Defined Cells")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm840
localization_priority: Normal
ms.assetid: d0f91e7d-2373-cfef-e105-fb17e77c7f2d
description: Gibt eine beschreibende Eingabeaufforderung bzw. einen Kommentar für die benutzerdefinierte Zelle an. Die Anwendung schließt den Prompt Text automatisch in Anführungszeichen (), um anzugeben, dass es sich um eine Textzeichenfolge ist. Wenn Sie ein Gleichheitszeichen (=) eingeben und die Anführungszeichen auslassen, können Sie eine Formel in dieser Zelle eingeben, die die Anwendung ausgewertet wird.
ms.openlocfilehash: a7f8757af3e324a89f49bf5d19185b7a22173ff5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797749"
---
# <a name="prompt-cell-user-defined-cells-section"></a><span data-ttu-id="2991a-105">Zelle "Prompt" (Abschnitt "User-Defined Cells")</span><span class="sxs-lookup"><span data-stu-id="2991a-105">Prompt Cell (User-Defined Cells Section)</span></span>

<span data-ttu-id="2991a-p102">Gibt eine beschreibende Eingabeaufforderung bzw. einen Kommentar für die benutzerdefinierte Zelle an. Die Anwendung schließt den Aufforderungstext automatisch in Anführungszeichen (" ") ein, um anzuzeigen, dass es sich um eine Textzeichenfolge handelt. Wenn Sie ein Gleichheitszeichen (=) eingeben und die Anführungszeichen auslassen, können Sie eine Formel in diese Zelle eingeben, die von der Anwendung berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="2991a-p102">Specifies a descriptive prompt or comment for the user-defined cell. The application automatically encloses the prompt text in quotation marks (" ") to indicate that it is a text string. If you type an equal sign (=) and omit the quotation marks, you can enter a formula in this cell that the application evaluates.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2991a-109">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2991a-109">Remarks</span></span>

<span data-ttu-id="2991a-110">Wenn Sie einen Verweis auf die Zelle Prompt nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="2991a-110">To get a reference to the Prompt cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2991a-111">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="2991a-111">Cell name:</span></span>  <br/> | <span data-ttu-id="2991a-112">Benutzer.</span><span class="sxs-lookup"><span data-stu-id="2991a-112">User.</span></span>  <span data-ttu-id="2991a-113">*Name* . Prompt Where Benutzer.</span><span class="sxs-lookup"><span data-stu-id="2991a-113">*Name*  .Prompt            where User.</span></span>  <span data-ttu-id="2991a-114">*Name* ist der Zeilenname</span><span class="sxs-lookup"><span data-stu-id="2991a-114">*Name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="2991a-115">Wenn Sie einen Verweis auf die Zelle Prompt aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="2991a-115">To get a reference to the Prompt cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2991a-116">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="2991a-116">Section index:</span></span>  <br/> |<span data-ttu-id="2991a-117">**visSectionUser**</span><span class="sxs-lookup"><span data-stu-id="2991a-117">**visSectionUser**</span></span> <br/> |
| <span data-ttu-id="2991a-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="2991a-118">Row index:</span></span>  <br/> |<span data-ttu-id="2991a-119">**VisRowUser +** *i* wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="2991a-119">**visRowUser +** *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="2991a-120">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="2991a-120">Cell index:</span></span>  <br/> |<span data-ttu-id="2991a-121">**visUserPrompt**</span><span class="sxs-lookup"><span data-stu-id="2991a-121">**visUserPrompt**</span></span> <br/> |
   
