---
title: Zelle "Description" (Abschnitt "Hyperlinks")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm230
localization_priority: Normal
ms.assetid: 2f571c65-6b7a-5a3a-c075-3c52d3ab989b
description: Stellt eine beschreibende Textzeichenfolge für einen Hyperlink dar.
ms.openlocfilehash: 567a90b3162c109582c3149c156a994392980577
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796859"
---
# <a name="description-cell-hyperlinks-section"></a><span data-ttu-id="52766-103">Zelle "Description" (Abschnitt "Hyperlinks")</span><span class="sxs-lookup"><span data-stu-id="52766-103">Description Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="52766-104">Stellt eine beschreibende Textzeichenfolge für einen Hyperlink dar.</span><span class="sxs-lookup"><span data-stu-id="52766-104">Represents a descriptive text string for a hyperlink.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="52766-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="52766-105">Remarks</span></span>

<span data-ttu-id="52766-106">Verwenden Sie diese Zelle, um Kommentare zum Hyperlink zu speichern, beispielsweise "Link zu unserer Website mit den Preisinformationen".</span><span class="sxs-lookup"><span data-stu-id="52766-106">Use this cell to store comments about the hyperlink; for example, "Link to our pricing Web site."</span></span>
  
<span data-ttu-id="52766-107">Sie können den Wert dieser Zelle auch im Dialogfeld **Hyperlinks** festlegen (klicken Sie auf der Registerkarte **Einfügen** auf **Hyperlink** ).</span><span class="sxs-lookup"><span data-stu-id="52766-107">You can also set the value of this cell in the **Hyperlinks** dialog box (click **Hyperlink** on the **Insert** tab).</span></span> 
  
<span data-ttu-id="52766-108">Wenn Sie einen Verweis auf die Zelle Description nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="52766-108">To get a reference to the Description cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="52766-109">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="52766-109">Cell name:</span></span>  <br/> | <span data-ttu-id="52766-110">Hyperlink.</span><span class="sxs-lookup"><span data-stu-id="52766-110">Hyperlink.</span></span>  <span data-ttu-id="52766-111">*Name* . Beschreibung, in dem Hyperlink.</span><span class="sxs-lookup"><span data-stu-id="52766-111">*Name*  .Description where Hyperlink.</span></span>  <span data-ttu-id="52766-112">*Ist der Name der Hyperlinkzeile*</span><span class="sxs-lookup"><span data-stu-id="52766-112">*Name*  is the name of the hyperlink row</span></span>  <br/> |
   
<span data-ttu-id="52766-113">Wenn Sie einen Verweis auf die Zelle Description aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="52766-113">To get a reference to the Description cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="52766-114">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="52766-114">Section index:</span></span>  <br/> |<span data-ttu-id="52766-115">**visSectionHyperlink**</span><span class="sxs-lookup"><span data-stu-id="52766-115">**visSectionHyperlink**</span></span> <br/> |
| <span data-ttu-id="52766-116">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="52766-116">Row index:</span></span>  <br/> |<span data-ttu-id="52766-117">**visRow1stHyperlink** +  *i* wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="52766-117">**visRow1stHyperlink** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="52766-118">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="52766-118">Cell index:</span></span>  <br/> |<span data-ttu-id="52766-119">**visHLinkDescription**</span><span class="sxs-lookup"><span data-stu-id="52766-119">**visHLinkDescription**</span></span> <br/> |
   
