---
title: Zelle "Gamma" (Abschnitt "Image Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm410
localization_priority: Normal
ms.assetid: 3dcaee26-391c-0494-4380-890ee825dc47
description: Passt die Intensität einer Grafik für ein spezifisches Ausgabegerät (z. B. Monitor oder Scanner) an. Der Standardwert ist 1 (keine Korrektur).
ms.openlocfilehash: d00eb11ff1feffacf0d758bb25cdd56281e91327
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409013"
---
# <a name="gamma-cell-image-properties-section"></a><span data-ttu-id="5f5bc-104">Zelle "Gamma" (Abschnitt "Image Properties")</span><span class="sxs-lookup"><span data-stu-id="5f5bc-104">Gamma Cell (Image Properties Section)</span></span>

<span data-ttu-id="5f5bc-p102">Passt die Intensität einer Grafik für ein spezifisches Ausgabegerät (z. B. Monitor oder Scanner) an. Der Standardwert ist 1 (keine Korrektur).</span><span class="sxs-lookup"><span data-stu-id="5f5bc-p102">Adjusts or corrects the intensity of an image for a particular output device, such as a monitor or scanner. The default value is 1 (no correction).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5f5bc-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5f5bc-107">Remarks</span></span>

<span data-ttu-id="5f5bc-108">Um einen Verweis auf die Gammazelle anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="5f5bc-108">To get a reference to the Gamma cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5f5bc-109">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="5f5bc-109">Cell name:</span></span>  <br/> | <span data-ttu-id="5f5bc-110">Gamma</span><span class="sxs-lookup"><span data-stu-id="5f5bc-110">Gamma</span></span>  <br/> |
   
<span data-ttu-id="5f5bc-111">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Gammazelle nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="5f5bc-111">To get a reference to the Gamma cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5f5bc-112">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="5f5bc-112">Section index:</span></span>  <br/> |<span data-ttu-id="5f5bc-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="5f5bc-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="5f5bc-114">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="5f5bc-114">Row index:</span></span>  <br/> |<span data-ttu-id="5f5bc-115">**visRowImage**</span><span class="sxs-lookup"><span data-stu-id="5f5bc-115">**visRowImage**</span></span> <br/> |
| <span data-ttu-id="5f5bc-116">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="5f5bc-116">Cell index:</span></span>  <br/> |<span data-ttu-id="5f5bc-117">**visImageGamma**</span><span class="sxs-lookup"><span data-stu-id="5f5bc-117">**visImageGamma**</span></span> <br/> |
   

