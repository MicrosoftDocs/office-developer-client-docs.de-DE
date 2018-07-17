---
title: Zelle "ShdwObliqueAngle" (Abschnitt "Page Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033178
localization_priority: Normal
ms.assetid: 2e0b9754-3e3b-3a26-4e1a-e09102055c20
description: Enthält eine Zahl, die den Winkel der Schräge angibt, wenn Sie den Standardzeichenblatt-Schattentyp anwenden.
ms.openlocfilehash: 4549ce7b5202b4649a925b04ea54c0d5df569599
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798097"
---
# <a name="shdwobliqueangle-cell-page-properties-section"></a><span data-ttu-id="68d05-103">ShdwObliqueAngle Cell (Page Properties Section)</span><span class="sxs-lookup"><span data-stu-id="68d05-103">ShdwObliqueAngle Cell (Page Properties Section)</span></span>

<span data-ttu-id="68d05-104">Enthält eine Zahl, die den Winkel der Schräge angibt, wenn Sie den Standardzeichenblatt-Schattentyp anwenden.</span><span class="sxs-lookup"><span data-stu-id="68d05-104">Contains a number specifying the angle of oblique direction when applying the default page shadow type.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="68d05-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="68d05-105">Remarks</span></span>

<span data-ttu-id="68d05-106">Der Wert Null (0) in dieser Zelle zeigt an, dass die Winkelrichtung genau nach oben verläuft, sie wird im Uhrzeigersinn gemessen.</span><span class="sxs-lookup"><span data-stu-id="68d05-106">A value of zero (0) in this cell indicates that the angle direction is straight up and is measured moving clockwise.</span></span>
  
 <span data-ttu-id="68d05-107">Der Winkel in dieser Zelle beschriebene wird verwendet, wenn die Zelle ShapeShdwType (der Schattentyp für ein Shape auf dem Zeichenblatt) auf Seitenstandard (**VisFSTPageDefault** ) festgelegt ist, und der Schattentyp oblique ist.</span><span class="sxs-lookup"><span data-stu-id="68d05-107">The angle described in this cell is used whenever the ShapeShdwType Cell (the shadow type for a shape on the page) is set to Page Default (**visFSTPageDefault** ), and the shadow type is oblique.</span></span> <span data-ttu-id="68d05-108">Der Standardzeichenblatt-Schattentyp wird in der Zelle ShdwType definiert.</span><span class="sxs-lookup"><span data-stu-id="68d05-108">The default page shadow type is defined in the ShdwType cell.</span></span> 
  
<span data-ttu-id="68d05-109">Wenn Sie dieses Verhalten für einen einzelnen Schatten festlegen möchten, verwenden Sie im Abschnitt Fill Format die Zelle ShapeShdwObliqueAngle.</span><span class="sxs-lookup"><span data-stu-id="68d05-109">To set this behavior for an individual shape, use the ShapeShdwObliqueAngle cell in the Fill Format section.</span></span>
  
<span data-ttu-id="68d05-110">Wenn Sie einen Verweis auf die Zelle ShdwObliqueAngle nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="68d05-110">To get a reference to the ShdwObliqueAngle cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="68d05-111">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="68d05-111">Cell name:</span></span>  <br/> | <span data-ttu-id="68d05-112">ShdwObliqueAngle</span><span class="sxs-lookup"><span data-stu-id="68d05-112">ShdwObliqueAngle</span></span>  <br/> |
   
<span data-ttu-id="68d05-113">Wenn Sie einen Verweis auf die Zelle ShdwObliqueAngle aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="68d05-113">To get a reference to the ShdwObliqueAngle cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="68d05-114">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="68d05-114">Section index:</span></span>  <br/> |<span data-ttu-id="68d05-115">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="68d05-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="68d05-116">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="68d05-116">Row index:</span></span>  <br/> |<span data-ttu-id="68d05-117">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="68d05-117">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="68d05-118">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="68d05-118">Cell index:</span></span>  <br/> |<span data-ttu-id="68d05-119">**visPageShdwObliqueAngle**</span><span class="sxs-lookup"><span data-stu-id="68d05-119">**visPageShdwObliqueAngle**</span></span> <br/> |
   
