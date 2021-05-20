---
title: IFERROR-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 232fa528-2375-90be-8e18-7a064ce1345e
description: Gibt das ausgewertete Ergebnis eines primären Ausdrucks zurück, wenn er nicht zu einem Fehler ausgewertet wird. Andernfalls wird das ausgewertete Ergebnis eines alternativen Ausdrucks zurückgegeben.
ms.openlocfilehash: 7b9b42b5c7e7053bae862ddadf17e65015d8ecc3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431176"
---
# <a name="iferror-function"></a><span data-ttu-id="5af97-104">IFERROR Function</span><span class="sxs-lookup"><span data-stu-id="5af97-104">IFERROR Function</span></span>

<span data-ttu-id="5af97-105">Gibt das ausgewertete Ergebnis eines primären Ausdrucks zurück, wenn er nicht zu einem Fehler ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="5af97-105">Returns the evaluated result of a primary expression, if it does not evaluate to an error.</span></span> <span data-ttu-id="5af97-106">Andernfalls wird das ausgewertete Ergebnis eines alternativen Ausdrucks zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5af97-106">Otherwise, returns the evaluated result of an alternate expression.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="5af97-107">Versionsinformationen</span><span class="sxs-lookup"><span data-stu-id="5af97-107">Version Information</span></span>

<span data-ttu-id="5af97-108">Hinzugefügte Version: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="5af97-108">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="5af97-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="5af97-109">Syntax</span></span>

<span data-ttu-id="5af97-110">IFERROR(\*\* *primärer Ausdruck* \*\*, \*\* *alternativer Ausdruck* \*\* )</span><span class="sxs-lookup"><span data-stu-id="5af97-110">IFERROR(\*\* *primary expression* \*\*, \*\* *alternate expression* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="5af97-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="5af97-111">Parameters</span></span>

|<span data-ttu-id="5af97-112">**Name**</span><span class="sxs-lookup"><span data-stu-id="5af97-112">**Name**</span></span>|<span data-ttu-id="5af97-113">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="5af97-113">**Required/Optional**</span></span>|<span data-ttu-id="5af97-114">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="5af97-114">**Data Type**</span></span>|<span data-ttu-id="5af97-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5af97-115">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="5af97-116">_Primärer Ausdruck_</span><span class="sxs-lookup"><span data-stu-id="5af97-116">_primary expression_</span></span> <br/> |<span data-ttu-id="5af97-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="5af97-117">Required</span></span>  <br/> |<span data-ttu-id="5af97-118">**String**</span><span class="sxs-lookup"><span data-stu-id="5af97-118">**String**</span></span> <br/> |<span data-ttu-id="5af97-119">Der erste Ausdruck, der ausgewertet werden soll.</span><span class="sxs-lookup"><span data-stu-id="5af97-119">The first expression to evaluate.</span></span>  <br/> |
| <span data-ttu-id="5af97-120">_Alternativer Ausdruck_</span><span class="sxs-lookup"><span data-stu-id="5af97-120">_alternate expression_</span></span> <br/> |<span data-ttu-id="5af97-121">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="5af97-121">Required</span></span>  <br/> |<span data-ttu-id="5af97-122">**String**</span><span class="sxs-lookup"><span data-stu-id="5af97-122">**String**</span></span> <br/> |<span data-ttu-id="5af97-123">Der alternative Ausdruck, der ausgewertet werden soll, wenn der erste Ausdruck einen Fehler zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="5af97-123">The alternate expression to evaluate if the primary expression evaluates to an error.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="5af97-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5af97-124">Return value</span></span>

<span data-ttu-id="5af97-125">Variiert</span><span class="sxs-lookup"><span data-stu-id="5af97-125">Varies</span></span>
  

