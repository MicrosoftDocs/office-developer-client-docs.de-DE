---
title: Zelle "EnableLineProps" (Abschnitt "Style Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251696
localization_priority: Normal
ms.assetid: 9f619416-36ff-1479-6232-225c11827e01
description: Bestimmt, ob eine Formatvorlage Linieneigenschaften enthält.
ms.openlocfilehash: 0e1eb67528b3e87bcfff5281dd1e0b2db3a0a4d5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796927"
---
# <a name="enablelineprops-cell-style-properties-section"></a><span data-ttu-id="df9c9-103">EnableLineProps Cell (Style Properties Section)</span><span class="sxs-lookup"><span data-stu-id="df9c9-103">EnableLineProps Cell (Style Properties Section)</span></span>

<span data-ttu-id="df9c9-104">Bestimmt, ob eine Formatvorlage Linieneigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="df9c9-104">Determines whether a style includes line properties.</span></span>
  
|<span data-ttu-id="df9c9-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="df9c9-105">**Value**</span></span>|<span data-ttu-id="df9c9-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="df9c9-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="df9c9-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="df9c9-107">TRUE</span></span>  <br/> |<span data-ttu-id="df9c9-108">Linieneigenschaften einschließen.</span><span class="sxs-lookup"><span data-stu-id="df9c9-108">Include line properties.</span></span>  <br/> |
|<span data-ttu-id="df9c9-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="df9c9-109">FALSE</span></span>  <br/> |<span data-ttu-id="df9c9-110">Linieneigenschaften ausschließen.</span><span class="sxs-lookup"><span data-stu-id="df9c9-110">Exclude line properties.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="df9c9-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="df9c9-111">Remarks</span></span>

<span data-ttu-id="df9c9-112">Wenn Sie einen Verweis auf die Zelle EnableLineProps nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="df9c9-112">To get a reference to the EnableLineProps cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="df9c9-113">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="df9c9-113">Cell name:</span></span>  <br/> |<span data-ttu-id="df9c9-114">EnableLineProps</span><span class="sxs-lookup"><span data-stu-id="df9c9-114">EnableLineProps</span></span>  <br/> |
   
<span data-ttu-id="df9c9-115">Wenn Sie einen Verweis auf die Zelle EnableLineProps aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="df9c9-115">To get a reference to the EnableLineProps cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="df9c9-116">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="df9c9-116">Section index:</span></span>  <br/> |<span data-ttu-id="df9c9-117">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="df9c9-117">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="df9c9-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="df9c9-118">Row index:</span></span>  <br/> |<span data-ttu-id="df9c9-119">**visRowStyle**</span><span class="sxs-lookup"><span data-stu-id="df9c9-119">**visRowStyle**</span></span> <br/> |
|<span data-ttu-id="df9c9-120">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="df9c9-120">Cell index:</span></span>  <br/> |<span data-ttu-id="df9c9-121">**visStyleIncludesLine**</span><span class="sxs-lookup"><span data-stu-id="df9c9-121">**visStyleIncludesLine**</span></span> <br/> |
   
