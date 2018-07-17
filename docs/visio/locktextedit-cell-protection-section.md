---
title: Zelle "LockTextEdit" (Abschnitt "Protection")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm665
localization_priority: Normal
ms.assetid: d8de5fa4-826b-e869-4d9f-997361d05fd8
description: Sperrt den Text eines Shapes, damit dieser nicht bearbeitet werden kann.
ms.openlocfilehash: 7f8800f0b260e808a46ec123d27784f3dd92e847
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797399"
---
# <a name="locktextedit-cell-protection-section"></a><span data-ttu-id="29384-103">Zelle "LockTextEdit" (Abschnitt "Protection")</span><span class="sxs-lookup"><span data-stu-id="29384-103">LockTextEdit Cell (Protection Section)</span></span>

<span data-ttu-id="29384-104">Sperrt den Text eines Shapes, damit dieser nicht bearbeitet werden kann.</span><span class="sxs-lookup"><span data-stu-id="29384-104">Locks the text of a shape so that it cannot be edited.</span></span>
  
|<span data-ttu-id="29384-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="29384-105">**Value**</span></span>|<span data-ttu-id="29384-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="29384-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="29384-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="29384-107">TRUE</span></span>  <br/> |<span data-ttu-id="29384-108">Text kann nicht bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="29384-108">Text cannot be edited.</span></span>  <br/> |
| <span data-ttu-id="29384-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="29384-109">FALSE</span></span>  <br/> | <span data-ttu-id="29384-110">Text kann bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="29384-110">Text can be edited.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="29384-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="29384-111">Remarks</span></span>

<span data-ttu-id="29384-112">Sie können weiterhin Text formatieren, indem Sie eine Formatvorlage im Dialogfeld **Text** anwenden (klicken Sie auf der Registerkarte **Start** auf den Pfeil neben **Schriftart** ).</span><span class="sxs-lookup"><span data-stu-id="29384-112">You can still format text by applying a style in the **Text** dialog box (on the **Home** tab, click the **Font** arrow).</span></span> 
  
<span data-ttu-id="29384-113">Wenn Sie einen Verweis auf die Zelle LockTextEdit nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="29384-113">To get a reference to the LockTextEdit cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="29384-114">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="29384-114">Cell name:</span></span>  <br/> | <span data-ttu-id="29384-115">LockTextEdit</span><span class="sxs-lookup"><span data-stu-id="29384-115">LockTextEdit</span></span>  <br/> |
   
<span data-ttu-id="29384-116">Wenn Sie einen Verweis auf die Zelle LockTextEdit aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="29384-116">To get a reference to the LockTextEdit cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="29384-117">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="29384-117">Section index:</span></span>  <br/> |<span data-ttu-id="29384-118">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="29384-118">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="29384-119">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="29384-119">Row index:</span></span>  <br/> |<span data-ttu-id="29384-120">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="29384-120">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="29384-121">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="29384-121">Cell index:</span></span>  <br/> |<span data-ttu-id="29384-122">**visLockTextEdit**</span><span class="sxs-lookup"><span data-stu-id="29384-122">**visLockTextEdit**</span></span> <br/> |
   
