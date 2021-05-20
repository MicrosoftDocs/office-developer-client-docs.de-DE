---
title: Exp-Funktion (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 09385b75-ec0e-4dde-b9c3-9ade4a7a2b74
description: Gibt den exponentiellen Wert des angegebenen Ausdrucks zurück.
ms.openlocfilehash: 30777c41005dfcf1caad896e9e60f0bcfd9d4361
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436412"
---
# <a name="exp-function-access-custom-web-app"></a><span data-ttu-id="6469c-103">Exp-Funktion (benutzerdefinierte Access-Web-App)</span><span class="sxs-lookup"><span data-stu-id="6469c-103">Exp Function (Access custom web app)</span></span>

<span data-ttu-id="6469c-104">Gibt den exponentiellen Wert des angegebenen Ausdrucks zurück.</span><span class="sxs-lookup"><span data-stu-id="6469c-104">Returns the exponential value of the specified expression.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="6469c-p101">Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen.</span><span class="sxs-lookup"><span data-stu-id="6469c-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="6469c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="6469c-107">Syntax</span></span>

 <span data-ttu-id="6469c-108">**Exp** (*NumericExpression*)</span><span class="sxs-lookup"><span data-stu-id="6469c-108">**Exp** (*NumericExpression*)</span></span> 
  
<span data-ttu-id="6469c-109">Die **Exp-Funktion** enthält das folgende Argument.</span><span class="sxs-lookup"><span data-stu-id="6469c-109">The **Exp** function contains the following argument.</span></span> 
  
|<span data-ttu-id="6469c-110">**Argumentname**</span><span class="sxs-lookup"><span data-stu-id="6469c-110">**Argument name**</span></span>|<span data-ttu-id="6469c-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6469c-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="6469c-112">*NumericExpression*</span><span class="sxs-lookup"><span data-stu-id="6469c-112">*NumericExpression*</span></span>  <br/> |<span data-ttu-id="6469c-113">Ein Ausdruck vom Typ Double oder eines Typs, der implizit in Double konvertiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="6469c-113">An expression of type Double or of a type that can be implicitly converted to Double.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6469c-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6469c-114">Remarks</span></span>

<span data-ttu-id="6469c-115">Die Konstante **e** (2,718281...), ist die Basis natürlicher Logarithmen.</span><span class="sxs-lookup"><span data-stu-id="6469c-115">The constant **e** (2.718281…), is the base of natural logarithms.</span></span> 
  
<span data-ttu-id="6469c-116">Der Exponent einer Zahl ist die Konstante **e,** die auf die Kraft der Zahl angehoben wird.</span><span class="sxs-lookup"><span data-stu-id="6469c-116">The exponent of a number is the constant **e** raised to the power of the number.</span></span> <span data-ttu-id="6469c-117">Beispiel: **Exp** (1.0) = e^1.0 = 2.71828182845905 und **Exp** (10) = e^10 = 22026.4657948067.</span><span class="sxs-lookup"><span data-stu-id="6469c-117">For example **Exp** (1.0) = e^1.0 = 2.71828182845905 and **Exp** (10) = e^10 = 22026.4657948067.</span></span> 
  
<span data-ttu-id="6469c-118">Die Exponentielle des natürlichen Logarithmus einer Zahl ist die Zahl selbst: **Exp** (LOG (n)) = n.</span><span class="sxs-lookup"><span data-stu-id="6469c-118">The exponential of the natural logarithm of a number is the number itself: **Exp** (LOG (n)) = n.</span></span> <span data-ttu-id="6469c-119">Und der natürliche Logarithmus des Exponentiellen einer Zahl ist die Zahl selbst: LOG (**Exp** (n)) = n.</span><span class="sxs-lookup"><span data-stu-id="6469c-119">And the natural logarithm of the exponential of a number is the number itself: LOG (**Exp** (n)) = n.</span></span> 
  

