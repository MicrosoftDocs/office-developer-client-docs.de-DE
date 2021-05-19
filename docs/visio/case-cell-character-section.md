---
title: Zelle "Case" (Abschnitt "Character")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251250
localization_priority: Normal
ms.assetid: cf063c05-5789-e037-700b-1e70df00e254
description: Bestimmt die Groß- und Kleinschreibung für den Text des Shapes. Die Optionen Nur Großbuchstaben (1) und Große Anfangsbuchstaben (2) ändern die Darstellung eines komplett in Großbuchstaben eingegebenen Texts nicht. Der Text muss in Kleinbuchstaben eingegeben werden, damit diese Optionen eine Wirkung zeigen.
ms.openlocfilehash: 50ceaa1188caded40d36b8837c346fbbba2e14d2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434347"
---
# <a name="case-cell-character-section"></a><span data-ttu-id="9d1a8-105">Zelle "Case" (Abschnitt "Character")</span><span class="sxs-lookup"><span data-stu-id="9d1a8-105">Case Cell (Character Section)</span></span>

<span data-ttu-id="9d1a8-p102">Bestimmt die Groß- und Kleinschreibung für den Text des Shapes. Die Optionen Nur Großbuchstaben (1) und Große Anfangsbuchstaben (2) ändern die Darstellung eines komplett in Großbuchstaben eingegebenen Texts nicht. Der Text muss in Kleinbuchstaben eingegeben werden, damit diese Optionen eine Wirkung zeigen.</span><span class="sxs-lookup"><span data-stu-id="9d1a8-p102">Determines the case of a shape's text. All capital (uppercase) letters (1) and initial capital letters (2) do not change the appearance of text that was entered in all capital letters. The text must be entered in lowercase letters for these options to show an effect.</span></span>
  
|<span data-ttu-id="9d1a8-109">**Wert**</span><span class="sxs-lookup"><span data-stu-id="9d1a8-109">**Value**</span></span>|<span data-ttu-id="9d1a8-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9d1a8-110">**Description**</span></span>|<span data-ttu-id="9d1a8-111">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="9d1a8-111">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="9d1a8-112">0</span><span class="sxs-lookup"><span data-stu-id="9d1a8-112">0</span></span>  <br/> | <span data-ttu-id="9d1a8-113">Normalschreibung</span><span class="sxs-lookup"><span data-stu-id="9d1a8-113">Normal case</span></span>  <br/> |<span data-ttu-id="9d1a8-114">**visCaseNormal**</span><span class="sxs-lookup"><span data-stu-id="9d1a8-114">**visCaseNormal**</span></span> <br/> |
| <span data-ttu-id="9d1a8-115">1</span><span class="sxs-lookup"><span data-stu-id="9d1a8-115">1</span></span>  <br/> | <span data-ttu-id="9d1a8-116">Nur Großbuchstaben</span><span class="sxs-lookup"><span data-stu-id="9d1a8-116">All capital (uppercase) letters</span></span>  <br/> |<span data-ttu-id="9d1a8-117">**visCaseAllCaps**</span><span class="sxs-lookup"><span data-stu-id="9d1a8-117">**visCaseAllCaps**</span></span> <br/> |
| <span data-ttu-id="9d1a8-118">2</span><span class="sxs-lookup"><span data-stu-id="9d1a8-118">2</span></span>  <br/> | <span data-ttu-id="9d1a8-119">Große Anfangsbuchstaben</span><span class="sxs-lookup"><span data-stu-id="9d1a8-119">Initial capital letters only</span></span>  <br/> |<span data-ttu-id="9d1a8-120">**visCaseInitialCaps**</span><span class="sxs-lookup"><span data-stu-id="9d1a8-120">**visCaseInitialCaps**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9d1a8-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9d1a8-121">Remarks</span></span>

<span data-ttu-id="9d1a8-122">Um einen Verweis auf die Zelle Case anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="9d1a8-122">To get a reference to the Case cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9d1a8-123">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="9d1a8-123">Cell name:</span></span>  <br/> | <span data-ttu-id="9d1a8-124">Char.Case[  *i*  ] where  *i*  = <1>, 2, 3, ...</span><span class="sxs-lookup"><span data-stu-id="9d1a8-124">Char.Case[  *i*  ]            where  *i*  = <1>, 2, 3, ...</span></span>  <br/> |
   
<span data-ttu-id="9d1a8-125">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle Case nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="9d1a8-125">To get a reference to the Case cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9d1a8-126">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="9d1a8-126">Section index:</span></span>  <br/> |<span data-ttu-id="9d1a8-127">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="9d1a8-127">**visSectionCharacter**</span></span> <br/> |
| <span data-ttu-id="9d1a8-128">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="9d1a8-128">Row index:</span></span>  <br/> |<span data-ttu-id="9d1a8-129">**visRowCharacter**  +   *i* where *i* = 0, 1, 2, ...</span><span class="sxs-lookup"><span data-stu-id="9d1a8-129">**visRowCharacter** +  *i*            where  *i*  = 0, 1, 2, ...</span></span>  <br/> |
| <span data-ttu-id="9d1a8-130">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="9d1a8-130">Cell index:</span></span>  <br/> |<span data-ttu-id="9d1a8-131">**visCharacterCase**</span><span class="sxs-lookup"><span data-stu-id="9d1a8-131">**visCharacterCase**</span></span> <br/> |
   

