---
title: Zelle "ImgWidth" (Abschnitt "Foreign Image Info")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm460
localization_priority: Normal
ms.assetid: b57fb962-0b3e-f2e5-3b88-3edf33e40496
description: 'Definiert die Breite des Objektbilds innerhalb seines Rahmens. Die Standardformel lautet:'
ms.openlocfilehash: 9da5e06a7fbf6ae77a49fb0410aefb406e2afecb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422831"
---
# <a name="imgwidth-cell-foreign-image-info-section"></a><span data-ttu-id="b1af5-104">Zelle "ImgWidth" (Abschnitt "Foreign Image Info")</span><span class="sxs-lookup"><span data-stu-id="b1af5-104">ImgWidth Cell (Foreign Image Info Section)</span></span>

<span data-ttu-id="b1af5-p102">Definiert die Breite des Objektbilds innerhalb seines Rahmens. Die Standardformel lautet:</span><span class="sxs-lookup"><span data-stu-id="b1af5-p102">Determines the width of the object's image within its border. The default formula is:</span></span>
  
<span data-ttu-id="b1af5-107">= Breite \* 1</span><span class="sxs-lookup"><span data-stu-id="b1af5-107">= Width \* 1</span></span>
  
<span data-ttu-id="b1af5-108">Beim Zuschneiden des Objekts ändert sich der Faktor, mit dem die Breite multipliziert wird.</span><span class="sxs-lookup"><span data-stu-id="b1af5-108">Cropping the object changes the factor by which Width is multiplied.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b1af5-109">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b1af5-109">Remarks</span></span>

<span data-ttu-id="b1af5-110">Um einen Verweis auf die ImgWidth-Zelle anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="b1af5-110">To get a reference to the ImgWidth cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b1af5-111">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="b1af5-111">Cell name:</span></span>  <br/> | <span data-ttu-id="b1af5-112">ImgWidth</span><span class="sxs-lookup"><span data-stu-id="b1af5-112">ImgWidth</span></span>  <br/> |
   
<span data-ttu-id="b1af5-113">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die ImgWidth-Zelle nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="b1af5-113">To get a reference to the ImgWidth cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b1af5-114">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="b1af5-114">Section index:</span></span>  <br/> |<span data-ttu-id="b1af5-115">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b1af5-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="b1af5-116">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="b1af5-116">Row index:</span></span>  <br/> |<span data-ttu-id="b1af5-117">**visRowForeign**</span><span class="sxs-lookup"><span data-stu-id="b1af5-117">**visRowForeign**</span></span> <br/> |
| <span data-ttu-id="b1af5-118">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="b1af5-118">Cell index:</span></span>  <br/> |<span data-ttu-id="b1af5-119">**visFrgnImgWidth**</span><span class="sxs-lookup"><span data-stu-id="b1af5-119">**visFrgnImgWidth**</span></span> <br/> |
   

