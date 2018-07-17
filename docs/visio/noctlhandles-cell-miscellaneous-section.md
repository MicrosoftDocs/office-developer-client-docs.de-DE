---
title: Zelle "NoCtlHandles" (Abschnitt "Miscellaneous")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251319
localization_priority: Normal
ms.assetid: 4345b3e5-f522-e300-307c-4f8992a3ddce
description: Aktiviert bzw. deaktiviert die Anzeige der Steuerpunkte für das ausgewählte Shape.
ms.openlocfilehash: 897e4cd97eeab8797f2652285ba395603c41a8e7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797538"
---
# <a name="noctlhandles-cell-miscellaneous-section"></a><span data-ttu-id="ff201-103">Zelle "NoCtlHandles" (Abschnitt "Miscellaneous")</span><span class="sxs-lookup"><span data-stu-id="ff201-103">NoCtlHandles Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="ff201-104">Aktiviert bzw. deaktiviert die Anzeige der Steuerpunkte für das ausgewählte Shape.</span><span class="sxs-lookup"><span data-stu-id="ff201-104">Switches the display of control handles on and off for the selected shape.</span></span>
  
|<span data-ttu-id="ff201-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="ff201-105">**Value**</span></span>|<span data-ttu-id="ff201-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ff201-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="ff201-107">WAHR</span><span class="sxs-lookup"><span data-stu-id="ff201-107">TRUE</span></span>  <br/> | <span data-ttu-id="ff201-108">Steuerpunkte werden nicht angezeigt, wenn ein Shape ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="ff201-108">Control handles are not displayed when a shape is selected.</span></span>  <br/> |
| <span data-ttu-id="ff201-109">FALSCH</span><span class="sxs-lookup"><span data-stu-id="ff201-109">FALSE</span></span>  <br/> | <span data-ttu-id="ff201-110">Steuerpunkte werden angezeigt, wenn ein Shape ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="ff201-110">Control handles are displayed when a shape is selected.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ff201-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ff201-111">Remarks</span></span>

<span data-ttu-id="ff201-112">Wenn Sie einen Verweis auf die Zelle NoCtlHandles nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="ff201-112">To get a reference to the NoCtlHandles cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ff201-113">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="ff201-113">Cell name:</span></span>  <br/> | <span data-ttu-id="ff201-114">NoCtlHandles</span><span class="sxs-lookup"><span data-stu-id="ff201-114">NoCtlHandles</span></span>  <br/> |
   
<span data-ttu-id="ff201-115">Wenn Sie einen Verweis auf die Zelle NoCtlHandles aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="ff201-115">To get a reference to the NoCtlHandles cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ff201-116">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="ff201-116">Section index:</span></span>  <br/> |<span data-ttu-id="ff201-117">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="ff201-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="ff201-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="ff201-118">Row index:</span></span>  <br/> |<span data-ttu-id="ff201-119">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="ff201-119">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="ff201-120">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="ff201-120">Cell index:</span></span>  <br/> |<span data-ttu-id="ff201-121">**visNoCtlHandles**</span><span class="sxs-lookup"><span data-stu-id="ff201-121">**visNoCtlHandles**</span></span> <br/> |
   
