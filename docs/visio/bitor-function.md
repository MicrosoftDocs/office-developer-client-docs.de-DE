---
title: BITOR-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251400
localization_priority: Normal
ms.assetid: 1d0954c5-b2cb-6c5d-62b3-a68011cf0c85
description: Gibt eine 16-Bit-Binärzahl zurück, in der jedes Bit auf 1 festgelegt ist, wenn das entsprechende Bit in binärer Zahl1 oder binärer Zahl2 1 ist. Das Bit wird nur dann auf 0 festgelegt, wenn das entsprechende Bit sowohl in binärer Zahl1 als auch in binärer Zahl2 0 ist.
ms.openlocfilehash: 13bda2c6c65557b1f8372432cf919b2aaf2d75de
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408082"
---
# <a name="bitor-function"></a><span data-ttu-id="e883e-104">BITOR Function</span><span class="sxs-lookup"><span data-stu-id="e883e-104">BITOR Function</span></span>

<span data-ttu-id="e883e-105">Gibt eine 16-Bit-Binärzahl zurück, in der jedes Bit auf 1 festgelegt ist, wenn das entsprechende Bit in binärer  *Zahl1*  oder  *binärer Zahl2*  1 ist.</span><span class="sxs-lookup"><span data-stu-id="e883e-105">Returns a 16-bit binary number in which each bit is set to 1 if the corresponding bit in either  *binary number1*  or  *binary number2*  is 1.</span></span> <span data-ttu-id="e883e-106">Das Bit wird nur dann auf 0 festgelegt, wenn das entsprechende Bit sowohl in binärer *Zahl1* als auch in *binärer Zahl2 0 ist.*</span><span class="sxs-lookup"><span data-stu-id="e883e-106">The bit is set to 0 only if the corresponding bit is 0 in both  *binary number1*  and  *binary number2*  .</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="e883e-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e883e-107">Syntax</span></span>

<span data-ttu-id="e883e-108">BITOR(\*\* *binary number1* \*\*, \*\* *binary number2* \*\* )</span><span class="sxs-lookup"><span data-stu-id="e883e-108">BITOR(\*\* *binary number1* \*\*, \*\* *binary number2* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="e883e-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="e883e-109">Parameters</span></span>

|<span data-ttu-id="e883e-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="e883e-110">**Name**</span></span>|<span data-ttu-id="e883e-111">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="e883e-111">**Required/Optional**</span></span>|<span data-ttu-id="e883e-112">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="e883e-112">**Data Type**</span></span>|<span data-ttu-id="e883e-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e883e-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="e883e-114">_binäre Zahl1_</span><span class="sxs-lookup"><span data-stu-id="e883e-114">_binary number1_</span></span> <br/> |<span data-ttu-id="e883e-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="e883e-115">Required</span></span>  <br/> |<span data-ttu-id="e883e-116">**Numeric**</span><span class="sxs-lookup"><span data-stu-id="e883e-116">**Numeric**</span></span> <br/> |<span data-ttu-id="e883e-117">Die erste 16-Bit-Binärzahl.</span><span class="sxs-lookup"><span data-stu-id="e883e-117">The first 16-bit binary number.</span></span>  <br/> |
| <span data-ttu-id="e883e-118">_binäre Zahl2_</span><span class="sxs-lookup"><span data-stu-id="e883e-118">_binary number2_</span></span> <br/> |<span data-ttu-id="e883e-119">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="e883e-119">Required</span></span>  <br/> |<span data-ttu-id="e883e-120">**Numeric**</span><span class="sxs-lookup"><span data-stu-id="e883e-120">**Numeric**</span></span> <br/> |<span data-ttu-id="e883e-121">Die zweite 16-Bit-Binärzahl.</span><span class="sxs-lookup"><span data-stu-id="e883e-121">The second 16-bit binary number.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="e883e-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e883e-122">Return value</span></span>

<span data-ttu-id="e883e-123">16-bit Binary</span><span class="sxs-lookup"><span data-stu-id="e883e-123">16-bit Binary</span></span>
  
## <a name="example"></a><span data-ttu-id="e883e-124">Beispiel</span><span class="sxs-lookup"><span data-stu-id="e883e-124">Example</span></span>

<span data-ttu-id="e883e-125">BITOR(12,6)</span><span class="sxs-lookup"><span data-stu-id="e883e-125">BITOR(12,6)</span></span>
  
<span data-ttu-id="e883e-p103">Gibt 14 zurück. Die Zahl 12 entspricht 0...01100. Die Zahl 6 entspricht 0...00110. Daher ergibt BITOR(12,6) den Wert 0...01110.</span><span class="sxs-lookup"><span data-stu-id="e883e-p103">Returns 14. The 12 = 0...01100. The 6 = 0...00110. Therefore, BITOR(12,6) = 0...01110.</span></span>
  

