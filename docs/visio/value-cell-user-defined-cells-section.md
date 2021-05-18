---
title: Zelle "Value" (Abschnitt "User-Defined Cells")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1100
localization_priority: Normal
ms.assetid: 495b2aec-e197-75eb-9974-e7c92d26546f
description: Gibt einen Wert für die entsprechende benutzerdefinierte Zelle an.
ms.openlocfilehash: 137d22430829f96a9c6ad69a73a6b44e964d5f4f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422989"
---
# <a name="value-cell-user-defined-cells-section"></a><span data-ttu-id="76391-103">Zelle "Value" (Abschnitt "User-Defined Cells")</span><span class="sxs-lookup"><span data-stu-id="76391-103">Value Cell (User-Defined Cells Section)</span></span>

<span data-ttu-id="76391-104">Gibt einen Wert für die entsprechende benutzerdefinierte Zelle an.</span><span class="sxs-lookup"><span data-stu-id="76391-104">Specifies a value for the corresponding user-defined cell.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="76391-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="76391-105">Remarks</span></span>

<span data-ttu-id="76391-106">Wenn Sie auf diesen Wert in einer anderen Zelle verweisen möchten, geben Sie den in die Zeilenbeschriftung User.Row benutzerdefinierten Namen an.</span><span class="sxs-lookup"><span data-stu-id="76391-106">To refer to this value in another cell, specify the user-defined name entered in the row label User.Row.</span></span>
  
<span data-ttu-id="76391-107">Um einen Verweis auf die Zelle Value anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="76391-107">To get a reference to the Value cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="76391-108">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="76391-108">Cell name:</span></span>  <br/> | <span data-ttu-id="76391-109">User.</span><span class="sxs-lookup"><span data-stu-id="76391-109">User.</span></span>  <span data-ttu-id="76391-110">*Name*  . Wert, wobei User.</span><span class="sxs-lookup"><span data-stu-id="76391-110">*Name*  .Value            where User.</span></span>  <span data-ttu-id="76391-111">*Name*  ist der Zeilenname</span><span class="sxs-lookup"><span data-stu-id="76391-111">*Name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="76391-112">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle Value nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="76391-112">To get a reference to the Value cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="76391-113">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="76391-113">Section index:</span></span>  <br/> |<span data-ttu-id="76391-114">**visSectionUser**</span><span class="sxs-lookup"><span data-stu-id="76391-114">**visSectionUser**</span></span> <br/> |
| <span data-ttu-id="76391-115">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="76391-115">Row index:</span></span>  <br/> |<span data-ttu-id="76391-116">**visRowUser**  +   *i,* *wobei i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="76391-116">**visRowUser** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="76391-117">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="76391-117">Cell index:</span></span>  <br/> |<span data-ttu-id="76391-118">**visUserValue**</span><span class="sxs-lookup"><span data-stu-id="76391-118">**visUserValue**</span></span> <br/> |
   

