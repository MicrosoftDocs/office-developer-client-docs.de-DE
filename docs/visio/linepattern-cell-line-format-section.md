---
title: Zelle "LinePattern" (Abschnitt "Line Format")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm560
localization_priority: Normal
ms.assetid: a416762b-7294-c99f-d9f1-332c3ed35dff
description: Definiert das Linienmuster eines Shapes. Der in die Zelle LinePattern eingegebene Wert ist eine Zahl, die einen Index für eine Linienmustersammlung darstellt.
ms.openlocfilehash: cccc6028de21299942e62c53aba48622baa95f98
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797331"
---
# <a name="linepattern-cell-line-format-section"></a><span data-ttu-id="1be18-104">LinePattern Cell (Line Format Section)</span><span class="sxs-lookup"><span data-stu-id="1be18-104">LinePattern Cell (Line Format Section)</span></span>

<span data-ttu-id="1be18-p102">Definiert das Linienmuster eines Shapes. Der in die Zelle LinePattern eingegebene Wert ist eine Zahl, die einen Index für eine Linienmustersammlung darstellt.</span><span class="sxs-lookup"><span data-stu-id="1be18-p102">Determines the line pattern of the shape. The value entered in the LinePattern cell is a number that is an index into a collection of line patterns.</span></span>
  
|<span data-ttu-id="1be18-107">**Wert**</span><span class="sxs-lookup"><span data-stu-id="1be18-107">**Value**</span></span>|<span data-ttu-id="1be18-108">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1be18-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1be18-109">0</span><span class="sxs-lookup"><span data-stu-id="1be18-109">0</span></span>  <br/> |<span data-ttu-id="1be18-110">Kein Linienmuster</span><span class="sxs-lookup"><span data-stu-id="1be18-110">No line pattern</span></span>  <br/> |
|<span data-ttu-id="1be18-111">1</span><span class="sxs-lookup"><span data-stu-id="1be18-111">1</span></span>  <br/> |<span data-ttu-id="1be18-112">Einfarbig</span><span class="sxs-lookup"><span data-stu-id="1be18-112">Solid</span></span>  <br/> |
|<span data-ttu-id="1be18-113">2 - 23</span><span class="sxs-lookup"><span data-stu-id="1be18-113">2 - 23</span></span>  <br/> |<span data-ttu-id="1be18-114">Verschiedene Linienmuster</span><span class="sxs-lookup"><span data-stu-id="1be18-114">Assorted line patterns</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1be18-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1be18-115">Remarks</span></span>

<span data-ttu-id="1be18-116">Sie können die Linienmustersammlung im Dialogfeld **Linie** ansehen (klicken Sie auf der Registerkarte **Start** in der Gruppe **Shape** klicken Sie auf **Zeile**, **Bindestriche**, und klicken Sie dann auf **Weitere Linien**).</span><span class="sxs-lookup"><span data-stu-id="1be18-116">You can view the line pattern collection in the **Line** dialog box (on the **Home** tab, in the **Shape** group, click **Line**, point to **Dashes**, and then click **More Lines**).</span></span>
  
<span data-ttu-id="1be18-117">Um ein benutzerdefiniertes Linienmuster anzugeben, verwenden Sie die Funktion VERWENDUNG in dieser Zelle.</span><span class="sxs-lookup"><span data-stu-id="1be18-117">To specify a custom line pattern, use the USE function in this cell.</span></span>
  
<span data-ttu-id="1be18-118">Wenn Sie einen Verweis auf die Zelle LinePattern nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="1be18-118">To get a reference to the LinePattern cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1be18-119">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="1be18-119">Cell name:</span></span>  <br/> |<span data-ttu-id="1be18-120">LinePattern</span><span class="sxs-lookup"><span data-stu-id="1be18-120">LinePattern</span></span>  <br/> |
   
<span data-ttu-id="1be18-121">Wenn Sie einen Verweis auf die Zelle LinePattern aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="1be18-121">To get a reference to the LinePattern cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1be18-122">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="1be18-122">Section index:</span></span>  <br/> |<span data-ttu-id="1be18-123">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="1be18-123">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="1be18-124">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="1be18-124">Row index:</span></span>  <br/> |<span data-ttu-id="1be18-125">**visRowLine**</span><span class="sxs-lookup"><span data-stu-id="1be18-125">**visRowLine**</span></span> <br/> |
|<span data-ttu-id="1be18-126">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="1be18-126">Cell index:</span></span>  <br/> |<span data-ttu-id="1be18-127">**visLinePattern**</span><span class="sxs-lookup"><span data-stu-id="1be18-127">**visLinePattern**</span></span> <br/> |
   
