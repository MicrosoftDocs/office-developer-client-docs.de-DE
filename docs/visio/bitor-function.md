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
description: Gibt eine 16-Bit-Binärzahl in der jedes Bit auf 1 festgelegt ist, wenn das entsprechende Bit in binary number1 oder binary number2 1 ist. Nur, wenn das entsprechende Bit in binary Zahl1 und binäre Zahl2 0 ist, wird das Bit auf 0 festgelegt.
ms.openlocfilehash: db9808f16b32776149abbddf882310c02268cec3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796488"
---
# <a name="bitor-function"></a><span data-ttu-id="58a2f-104">BITOR Function</span><span class="sxs-lookup"><span data-stu-id="58a2f-104">BITOR Function</span></span>

<span data-ttu-id="58a2f-105">Gibt eine 16-Bit-Binärzahl in der jedes Bit auf 1 festgelegt ist, wenn das entsprechende Bit in *binary number1* oder *binary Zahl2* 1 ist.</span><span class="sxs-lookup"><span data-stu-id="58a2f-105">Returns a 16-bit binary number in which each bit is set to 1 if the corresponding bit in either  *binary number1*  or  *binary number2*  is 1.</span></span> <span data-ttu-id="58a2f-106">Nur, wenn das entsprechende Bit in *binary Zahl1* und *binäre Zahl2* 0 ist, wird das Bit auf 0 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="58a2f-106">The bit is set to 0 only if the corresponding bit is 0 in both  *binary number1*  and  *binary number2*  .</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="58a2f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="58a2f-107">Syntax</span></span>

<span data-ttu-id="58a2f-108">BITOR (** *binary Zahl1* **, ** *binary Zahl2* **)</span><span class="sxs-lookup"><span data-stu-id="58a2f-108">BITOR(** *binary number1* **, ** *binary number2* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="58a2f-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="58a2f-109">Parameters</span></span>

|<span data-ttu-id="58a2f-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="58a2f-110">**Name**</span></span>|<span data-ttu-id="58a2f-111">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="58a2f-111">**Required/Optional**</span></span>|<span data-ttu-id="58a2f-112">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="58a2f-112">**Data Type**</span></span>|<span data-ttu-id="58a2f-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="58a2f-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="58a2f-114">_binäre Zahl1_</span><span class="sxs-lookup"><span data-stu-id="58a2f-114">_binary number1_</span></span> <br/> |<span data-ttu-id="58a2f-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="58a2f-115">Required</span></span>  <br/> |<span data-ttu-id="58a2f-116">**Numerische**</span><span class="sxs-lookup"><span data-stu-id="58a2f-116">**Numeric**</span></span> <br/> |<span data-ttu-id="58a2f-117">Die erste 16-Bit-Binärzahl.</span><span class="sxs-lookup"><span data-stu-id="58a2f-117">The first 16-bit binary number.</span></span>  <br/> |
| <span data-ttu-id="58a2f-118">_binäre Zahl2_</span><span class="sxs-lookup"><span data-stu-id="58a2f-118">_binary number2_</span></span> <br/> |<span data-ttu-id="58a2f-119">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="58a2f-119">Required</span></span>  <br/> |<span data-ttu-id="58a2f-120">**Numerische**</span><span class="sxs-lookup"><span data-stu-id="58a2f-120">**Numeric**</span></span> <br/> |<span data-ttu-id="58a2f-121">Die zweite 16-Bit-Binärzahl.</span><span class="sxs-lookup"><span data-stu-id="58a2f-121">The second 16-bit binary number.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="58a2f-122">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="58a2f-122">Return value</span></span>

<span data-ttu-id="58a2f-123">16-bit Binary</span><span class="sxs-lookup"><span data-stu-id="58a2f-123">16-bit Binary</span></span>
  
## <a name="example"></a><span data-ttu-id="58a2f-124">Beispiel</span><span class="sxs-lookup"><span data-stu-id="58a2f-124">Example</span></span>

<span data-ttu-id="58a2f-125">BITOR(12,6)</span><span class="sxs-lookup"><span data-stu-id="58a2f-125">BITOR(12,6)</span></span>
  
<span data-ttu-id="58a2f-p103">Gibt 14 zurück. Die Zahl 12 entspricht 0...01100. Die Zahl 6 entspricht 0...00110. Daher ergibt BITOR(12,6) den Wert 0...01110.</span><span class="sxs-lookup"><span data-stu-id="58a2f-p103">Returns 14. The 12 = 0...01100. The 6 = 0...00110. Therefore, BITOR(12,6) = 0...01110.</span></span>
  
