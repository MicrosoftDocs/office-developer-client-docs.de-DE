---
title: LEFT-Funktion (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1021757
localization_priority: Normal
ms.assetid: 0c2f6e06-b772-2006-ec7b-8695d097f146
description: Gibt das linke Zeichen oder die zeichenreichsten Zeichen in einer Textzeichenfolge basierend auf der angegebenen Anzahl von Zeichen zurück.
ms.openlocfilehash: aa4141cfc53bd41a6d58e8bc666b18a06fc80245
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427521"
---
# <a name="left-function-visioshapesheet"></a><span data-ttu-id="515e6-103">LEFT-Funktion (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="515e6-103">LEFT Function (VisioShapeSheet)</span></span>

<span data-ttu-id="515e6-104">Gibt das linke Zeichen oder die zeichenreichsten Zeichen in einer Textzeichenfolge basierend auf der angegebenen Anzahl von Zeichen zurück.</span><span class="sxs-lookup"><span data-stu-id="515e6-104">Returns the left-most character or characters in a text string, based on the number of characters you specify.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="515e6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="515e6-105">Syntax</span></span>

<span data-ttu-id="515e6-106">LEFT(\*\* *text* \*\*, [, \*\* *num_chars_opt* \*\* ])</span><span class="sxs-lookup"><span data-stu-id="515e6-106">LEFT(\*\* *text* \*\*, [, \*\* *num_chars_opt* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="515e6-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="515e6-107">Parameters</span></span>

|<span data-ttu-id="515e6-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="515e6-108">**Name**</span></span>|<span data-ttu-id="515e6-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="515e6-109">**Required/Optional**</span></span>|<span data-ttu-id="515e6-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="515e6-110">**Data Type**</span></span>|<span data-ttu-id="515e6-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="515e6-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="515e6-112">_text_</span><span class="sxs-lookup"><span data-stu-id="515e6-112">_text_</span></span> <br/> |<span data-ttu-id="515e6-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="515e6-113">Required</span></span>  <br/> |<span data-ttu-id="515e6-114">**String**</span><span class="sxs-lookup"><span data-stu-id="515e6-114">**String**</span></span> <br/> |<span data-ttu-id="515e6-115">Die Zeichenfolge mit den zu extrahierenden Zeichen.</span><span class="sxs-lookup"><span data-stu-id="515e6-115">The text string that contains the characters you want to extract.</span></span>  <br/> |
| <span data-ttu-id="515e6-116">_num_chars_opt_</span><span class="sxs-lookup"><span data-stu-id="515e6-116">_num_chars_opt_</span></span> <br/> |<span data-ttu-id="515e6-117">Optional.</span><span class="sxs-lookup"><span data-stu-id="515e6-117">Optional</span></span>  <br/> |<span data-ttu-id="515e6-118">**Numeric**</span><span class="sxs-lookup"><span data-stu-id="515e6-118">**Numeric**</span></span> <br/> |<span data-ttu-id="515e6-119">Die Anzahl der Zeichen, die extrahiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="515e6-119">The number of characters you want to extract.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="515e6-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="515e6-120">Return value</span></span>

<span data-ttu-id="515e6-121">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="515e6-121">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="515e6-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="515e6-122">Remarks</span></span>

<span data-ttu-id="515e6-123">Der Wert der  _num_chars_opt_ muss größer oder gleich Null (0) sein.</span><span class="sxs-lookup"><span data-stu-id="515e6-123">The value of  _num_chars_opt_ must be greater than or equal to zero (0).</span></span> 
  
<span data-ttu-id="515e6-124">Wenn  _num_chars_opt_ die Länge des Texts überwieg, gibt LEFT den ganzen Text zurück.</span><span class="sxs-lookup"><span data-stu-id="515e6-124">If  _num_chars_opt_ is greater than the length of the text, LEFT returns all of the text.</span></span> <span data-ttu-id="515e6-125">Wenn  _num_chars_opt_ nicht angegeben wird, wird angenommen, dass es 1 ist.</span><span class="sxs-lookup"><span data-stu-id="515e6-125">If  _num_chars_opt_ is omitted, it is assumed to be 1.</span></span> 
  
## <a name="example"></a><span data-ttu-id="515e6-126">Beispiel</span><span class="sxs-lookup"><span data-stu-id="515e6-126">Example</span></span>

<span data-ttu-id="515e6-127">LEFT ("Januar 1, 2004", 3)</span><span class="sxs-lookup"><span data-stu-id="515e6-127">LEFT ("January 1, 2004", 3)</span></span> 
  
<span data-ttu-id="515e6-128">Ergibt den Wert Jan.</span><span class="sxs-lookup"><span data-stu-id="515e6-128">Returns the value "Jan".</span></span> 
  

