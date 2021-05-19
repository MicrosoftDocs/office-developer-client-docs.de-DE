---
title: Zelle "Y" (Abschnitt "Connection Points")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_SDR.chm1175
localization_priority: Normal
ms.assetid: 3af6c949-d6a0-9560-54d7-b01a2ad99960
description: Stellt die y-Koordinate für einen Verbindungspunkt in lokalen Koordinaten dar.
ms.openlocfilehash: b408dc3c07e7bd28c0530b09f649453b4f08c770
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410847"
---
# <a name="y-cell-connection-points-section"></a><span data-ttu-id="5ee9a-103">Zelle "Y" (Abschnitt "Connection Points")</span><span class="sxs-lookup"><span data-stu-id="5ee9a-103">Y Cell (Connection Points Section)</span></span>

<span data-ttu-id="5ee9a-104">Stellt  die y-Koordinate für einen Verbindungspunkt in lokalen Koordinaten dar.</span><span class="sxs-lookup"><span data-stu-id="5ee9a-104">Represents the  *y*  -coordinate for a connection point in local coordinates.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="5ee9a-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5ee9a-105">Remarks</span></span>

<span data-ttu-id="5ee9a-106">Um einen Verweis auf die Zelle Y anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="5ee9a-106">To get a reference to the Y cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5ee9a-107">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="5ee9a-107">Cell name:</span></span>  <br/> | <span data-ttu-id="5ee9a-108">Connections.Y  *i*            where  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="5ee9a-108">Connections.Y  *i*            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="5ee9a-109">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle Y nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="5ee9a-109">To get a reference to the Y cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5ee9a-110">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="5ee9a-110">Section index:</span></span>  <br/> |<span data-ttu-id="5ee9a-111">**visSectionConnectionPts**</span><span class="sxs-lookup"><span data-stu-id="5ee9a-111">**visSectionConnectionPts**</span></span> <br/> |
| <span data-ttu-id="5ee9a-112">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="5ee9a-112">Row index:</span></span>  <br/> |<span data-ttu-id="5ee9a-113">**visRowConnectionPts**  +   *i,* *wobei i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="5ee9a-113">**visRowConnectionPts** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="5ee9a-114">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="5ee9a-114">Cell index:</span></span>  <br/> |<span data-ttu-id="5ee9a-115">**visY**</span><span class="sxs-lookup"><span data-stu-id="5ee9a-115">**visY**</span></span> <br/> |
   

