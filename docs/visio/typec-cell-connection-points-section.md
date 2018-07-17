---
title: Zelle "Type / C" (Abschnitt "Connection Points")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251723
localization_priority: Normal
ms.assetid: 2264d026-2041-3855-2b23-553ce67ae69d
description: Legt den Verbindungspunkttyp fest.
ms.openlocfilehash: 12c953a160ab99aad007e9b2bb9089d651aee553
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798331"
---
# <a name="type--c-cell-connection-points-section"></a><span data-ttu-id="21aff-103">Type / C Cell (Connection Points Section)</span><span class="sxs-lookup"><span data-stu-id="21aff-103">Type / C Cell (Connection Points Section)</span></span>

<span data-ttu-id="21aff-104">Legt den Verbindungspunkttyp fest.</span><span class="sxs-lookup"><span data-stu-id="21aff-104">Determines the connection point type.</span></span>
  
|<span data-ttu-id="21aff-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="21aff-105">**Value**</span></span>|<span data-ttu-id="21aff-106">**Typ**</span><span class="sxs-lookup"><span data-stu-id="21aff-106">**Type**</span></span>|<span data-ttu-id="21aff-107">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="21aff-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="21aff-108">0</span><span class="sxs-lookup"><span data-stu-id="21aff-108">0</span></span>  <br/> |<span data-ttu-id="21aff-109">Nach innen</span><span class="sxs-lookup"><span data-stu-id="21aff-109">Inward</span></span>  <br/> |<span data-ttu-id="21aff-110">**visCnnctTypeInward**</span><span class="sxs-lookup"><span data-stu-id="21aff-110">**visCnnctTypeInward**</span></span> <br/> |
|<span data-ttu-id="21aff-111">1</span><span class="sxs-lookup"><span data-stu-id="21aff-111">1</span></span>  <br/> |<span data-ttu-id="21aff-112">Nach außen</span><span class="sxs-lookup"><span data-stu-id="21aff-112">Outward</span></span>  <br/> |<span data-ttu-id="21aff-113">**visCnnctTypeOutward**</span><span class="sxs-lookup"><span data-stu-id="21aff-113">**visCnnctTypeOutward**</span></span> <br/> |
|<span data-ttu-id="21aff-114">2</span><span class="sxs-lookup"><span data-stu-id="21aff-114">2</span></span>  <br/> |<span data-ttu-id="21aff-115">Nach innen &amp; nach außen</span><span class="sxs-lookup"><span data-stu-id="21aff-115">Inward &amp; Outward</span></span>  <br/> |<span data-ttu-id="21aff-116">**visCnnctTypeInwardOutward**</span><span class="sxs-lookup"><span data-stu-id="21aff-116">**visCnnctTypeInwardOutward**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="21aff-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="21aff-117">Remarks</span></span>

<span data-ttu-id="21aff-118">Sie können den Verbindungspunkttyp auch festlegen, indem **die Verbinder** auswählen, indem ein Shape und klicken Sie dann mit der rechten Maustaste eines Verbindungspunkts.</span><span class="sxs-lookup"><span data-stu-id="21aff-118">You can also set the connection point type by choosing the **Connector** tool, selecting a shape, and then right-clicking a connection point.</span></span> <span data-ttu-id="21aff-119">Zu diesem Zweck müssen Sie im [Entwicklermodus](run-in-developer-mode-display-the-developer-tab.md) ausführen.</span><span class="sxs-lookup"><span data-stu-id="21aff-119">To do this, you need to run in [developer](run-in-developer-mode-display-the-developer-tab.md) mode.</span></span> 
  
<span data-ttu-id="21aff-120">Ein Verweis auf den Typ / C Zelle nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft verwenden:</span><span class="sxs-lookup"><span data-stu-id="21aff-120">To get a reference to the Type / C cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="21aff-121">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="21aff-121">Cell name:</span></span>  <br/> |<span data-ttu-id="21aff-122">Verbindungen.Typ [ *i* ] wobei *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="21aff-122">Connections.Type[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="21aff-123">Ein Verweis auf den Typ / Zelle C aus einem Programm nach Index verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="21aff-123">To get a reference to the Type / C cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="21aff-124">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="21aff-124">Section index:</span></span>  <br/> |<span data-ttu-id="21aff-125">**visSectionConnectionPts**</span><span class="sxs-lookup"><span data-stu-id="21aff-125">**visSectionConnectionPts**</span></span> <br/> |
|<span data-ttu-id="21aff-126">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="21aff-126">Row index:</span></span>  <br/> |<span data-ttu-id="21aff-127">**VisRowConnectionPts** +  *i* wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="21aff-127">**visRowConnectionPts** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="21aff-128">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="21aff-128">Cell index:</span></span>  <br/> |<span data-ttu-id="21aff-129">**visCnnctType** (nicht erweiterte Zeilen) **visCnnctC** (erweiterte Zeilen)</span><span class="sxs-lookup"><span data-stu-id="21aff-129">**visCnnctType** (non-extended rows) **visCnnctC** (extended rows)</span></span>  <br/> |
   
<span data-ttu-id="21aff-130">Informationen zu erweiterten und nicht erweiterten Zeilen finden Sie in der Zeile Connections Points.</span><span class="sxs-lookup"><span data-stu-id="21aff-130">For information about non-extended and extended rows, see Connection Points row.</span></span>
  
