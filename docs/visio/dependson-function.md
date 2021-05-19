---
title: DEPENDSON-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251420
localization_priority: Normal
ms.assetid: 8fcfcfdd-69e2-b061-fdb6-d29389d14403
description: Erstellt eine Abhängigkeit von Zellverweisen.
ms.openlocfilehash: 26e7f5fb0620a5f1812d878f02d5bedd43afe524
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423468"
---
# <a name="dependson-function"></a><span data-ttu-id="9c22d-103">DEPENDSON Function</span><span class="sxs-lookup"><span data-stu-id="9c22d-103">DEPENDSON Function</span></span>

<span data-ttu-id="9c22d-104">Erstellt eine Abhängigkeit von Zellverweisen.</span><span class="sxs-lookup"><span data-stu-id="9c22d-104">Creates a cell reference dependency.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="9c22d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9c22d-105">Syntax</span></span>

<span data-ttu-id="9c22d-106">DEPENDSON(\*\* *cellref* \*\* [, \*\* *cellref2* \*\*,...])</span><span class="sxs-lookup"><span data-stu-id="9c22d-106">DEPENDSON(\*\* *cellref* \*\* [, \*\* *cellref2* \*\*,...])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="9c22d-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="9c22d-107">Parameters</span></span>

|<span data-ttu-id="9c22d-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="9c22d-108">**Name**</span></span>|<span data-ttu-id="9c22d-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="9c22d-109">**Required/Optional**</span></span>|<span data-ttu-id="9c22d-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="9c22d-110">**Data Type**</span></span>|<span data-ttu-id="9c22d-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9c22d-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="9c22d-112">_cellref_</span><span class="sxs-lookup"><span data-stu-id="9c22d-112">_cellref_</span></span> <br/> |<span data-ttu-id="9c22d-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="9c22d-113">Required</span></span>  <br/> |<span data-ttu-id="9c22d-114">**String**</span><span class="sxs-lookup"><span data-stu-id="9c22d-114">**String**</span></span> <br/> |<span data-ttu-id="9c22d-115">Der erste Zellbezug.</span><span class="sxs-lookup"><span data-stu-id="9c22d-115">The first cell reference.</span></span>  <br/> |
| <span data-ttu-id="9c22d-116">_cellref2_</span><span class="sxs-lookup"><span data-stu-id="9c22d-116">_cellref2_</span></span> <br/> |<span data-ttu-id="9c22d-117">Optional</span><span class="sxs-lookup"><span data-stu-id="9c22d-117">Optional</span></span>  <br/> |<span data-ttu-id="9c22d-118">**String**</span><span class="sxs-lookup"><span data-stu-id="9c22d-118">**String**</span></span> <br/> |<span data-ttu-id="9c22d-119">Der zweite Zellbezug.</span><span class="sxs-lookup"><span data-stu-id="9c22d-119">The second cell reference.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9c22d-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9c22d-120">Remarks</span></span>

<span data-ttu-id="9c22d-p101">Diese Funktion gibt immer FALSE zurück. Sie hat keine Auswirkung, wenn Sie in einer Ereigniszeile oder in einer Aktionszelle verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9c22d-p101">This function always returns FALSE. It has no effect when used in an Event row or an Action cell.</span></span> 
  
## <a name="example"></a><span data-ttu-id="9c22d-123">Beispiel</span><span class="sxs-lookup"><span data-stu-id="9c22d-123">Example</span></span>

<span data-ttu-id="9c22d-124">OPENTEXTWIN() + DEPENDSON(PinX,PinY)</span><span class="sxs-lookup"><span data-stu-id="9c22d-124">OPENTEXTWIN() + DEPENDSON(PinX,PinY)</span></span> 
  
<span data-ttu-id="9c22d-125">Öffnet den Textblock eines Shapes, sobald sich die Zellen PinX oder PinY des Shapes ändern.</span><span class="sxs-lookup"><span data-stu-id="9c22d-125">Opens the text block for a shape whenever the shape's PinX or PinY cells change.</span></span> 
  

