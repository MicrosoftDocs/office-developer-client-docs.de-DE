---
title: TONE-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c2d6a7dd-9f15-27bd-9623-2a047683ff98
description: Ändert die Farbe durch verringern die Sättigung entsprechend der Angabe in der Int-Parameter.
ms.openlocfilehash: be89764c849299288963c272f8ffb2d5d728f270
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798298"
---
# <a name="tone-function"></a><span data-ttu-id="3f9cd-103">TONE-Funktion</span><span class="sxs-lookup"><span data-stu-id="3f9cd-103">TONE Function</span></span>

<span data-ttu-id="3f9cd-104">Ändert die Farbe durch verringern die Sättigung entsprechend der Angabe in der _Int_ -Parameter.</span><span class="sxs-lookup"><span data-stu-id="3f9cd-104">Modifies the color by decreasing its saturation by the amount specified in the  _int_ parameter.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="3f9cd-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3f9cd-105">Syntax</span></span>

<span data-ttu-id="3f9cd-106">TONE (** *Farbe* **, ** *Int* **)</span><span class="sxs-lookup"><span data-stu-id="3f9cd-106">TONE(** *color* **, ** *int* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="3f9cd-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="3f9cd-107">Parameters</span></span>

|<span data-ttu-id="3f9cd-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="3f9cd-108">**Name**</span></span>|<span data-ttu-id="3f9cd-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="3f9cd-109">**Required/Optional**</span></span>|<span data-ttu-id="3f9cd-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="3f9cd-110">**Data Type**</span></span>|<span data-ttu-id="3f9cd-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3f9cd-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="3f9cd-112">_Farbe_</span><span class="sxs-lookup"><span data-stu-id="3f9cd-112">_color_</span></span> <br/> |<span data-ttu-id="3f9cd-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="3f9cd-113">Required</span></span>  <br/> |<span data-ttu-id="3f9cd-114">**Numerische**</span><span class="sxs-lookup"><span data-stu-id="3f9cd-114">**Numeric**</span></span> <br/> |<span data-ttu-id="3f9cd-115">Der Farbindex von Microsoft Visio oder der RGB-Wert der Farbe.</span><span class="sxs-lookup"><span data-stu-id="3f9cd-115">The Microsoft Visio color index or RGB value of the color.</span></span>  <br/> |
| <span data-ttu-id="3f9cd-116">_int_</span><span class="sxs-lookup"><span data-stu-id="3f9cd-116">_int_</span></span> <br/> |<span data-ttu-id="3f9cd-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="3f9cd-117">Required</span></span>  <br/> |<span data-ttu-id="3f9cd-118">**Integer**</span><span class="sxs-lookup"><span data-stu-id="3f9cd-118">**Integer**</span></span> <br/> |<span data-ttu-id="3f9cd-p101">Der Wert, um den die Farbsättigung verringert werden soll. Kann positiv oder negativ sein.</span><span class="sxs-lookup"><span data-stu-id="3f9cd-p101">The amount by which to decrease the saturation of the color. Can be positive or negative.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="3f9cd-121">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="3f9cd-121">Return value</span></span>

 <span data-ttu-id="3f9cd-122">**RGB**</span><span class="sxs-lookup"><span data-stu-id="3f9cd-122">**RGB**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3f9cd-123">Hinweise</span><span class="sxs-lookup"><span data-stu-id="3f9cd-123">Remarks</span></span>

<span data-ttu-id="3f9cd-124">Die unteren und oberen Grenzwerte der Sättigung sind 0 und 240.</span><span class="sxs-lookup"><span data-stu-id="3f9cd-124">The upper and lower limits of saturation are 0 and 240 respectively.</span></span> <span data-ttu-id="3f9cd-125">Es gibt keine Beschränkung der Größe von die ganze Zahl, die Sie für den Parameter _Int_ weitergeben können, aber Sättigung überschreitet nie diese Grenzwerte.</span><span class="sxs-lookup"><span data-stu-id="3f9cd-125">There is no limit on the size of the integer you can pass for the  _int_ parameter, but saturation never exceeds these limits.</span></span> 
  
