---
title: PATHLENGTH-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6f47ea08-fb5e-7d48-e84a-2a6570564924
description: Gibt die Länge des Pfads zurück, der im angegebenen Abschnitt "Geometrie" definiert ist.
ms.openlocfilehash: e4f90c2bb886f54164bedab5f8d78fc528758414
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405849"
---
# <a name="pathlength-function"></a><span data-ttu-id="5a4dd-103">PATHLENGTH Function</span><span class="sxs-lookup"><span data-stu-id="5a4dd-103">PATHLENGTH Function</span></span>

<span data-ttu-id="5a4dd-104">Gibt die Länge des Pfads zurück, der im angegebenen Abschnitt "Geometrie" definiert ist.</span><span class="sxs-lookup"><span data-stu-id="5a4dd-104">Returns the length of the path that is defined in the specified Geometry section.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="5a4dd-105">Versionsinformationen</span><span class="sxs-lookup"><span data-stu-id="5a4dd-105">Version Information</span></span>

<span data-ttu-id="5a4dd-106">Hinzugefügte Version: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="5a4dd-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="5a4dd-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="5a4dd-107">Syntax</span></span>

<span data-ttu-id="5a4dd-108">PATHLENGTH(\*\* *section* \*\* \*\* *[,segment]* \*\* )</span><span class="sxs-lookup"><span data-stu-id="5a4dd-108">PATHLENGTH(\*\* *section* \*\* \*\* *[,segment]* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="5a4dd-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="5a4dd-109">Parameters</span></span>

|<span data-ttu-id="5a4dd-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="5a4dd-110">**Name**</span></span>|<span data-ttu-id="5a4dd-111">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="5a4dd-111">**Required/Optional**</span></span>|<span data-ttu-id="5a4dd-112">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="5a4dd-112">**Data Type**</span></span>|<span data-ttu-id="5a4dd-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5a4dd-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="5a4dd-114">_section_</span><span class="sxs-lookup"><span data-stu-id="5a4dd-114">_section_</span></span> <br/> |<span data-ttu-id="5a4dd-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="5a4dd-115">Required</span></span>  <br/> |<span data-ttu-id="5a4dd-116">**String**</span><span class="sxs-lookup"><span data-stu-id="5a4dd-116">**String**</span></span> <br/> |<span data-ttu-id="5a4dd-117">Der Abschnitt "Geometrie", der den Pfad darstellt, angegeben mit einer Referenz auf dessen Zelle "Path" (z. B. Geometrie1.Path).</span><span class="sxs-lookup"><span data-stu-id="5a4dd-117">The Geometry section that represents the path, specified by a reference to its Path cell (for example, Geometry1.Path).</span></span>  <br/> |
| <span data-ttu-id="5a4dd-118">_segment_</span><span class="sxs-lookup"><span data-stu-id="5a4dd-118">_segment_</span></span> <br/> |<span data-ttu-id="5a4dd-119">Optional</span><span class="sxs-lookup"><span data-stu-id="5a4dd-119">Optional</span></span>  <br/> |<span data-ttu-id="5a4dd-120">**Integer**</span><span class="sxs-lookup"><span data-stu-id="5a4dd-120">**Integer**</span></span> <br/> |<span data-ttu-id="5a4dd-121">Das auf 1 basierende Segment des zu messenden Pfads.</span><span class="sxs-lookup"><span data-stu-id="5a4dd-121">The 1-based segment of the path to measure.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="5a4dd-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5a4dd-122">Return value</span></span>

 <span data-ttu-id="5a4dd-123">**Double**</span><span class="sxs-lookup"><span data-stu-id="5a4dd-123">**Double**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5a4dd-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5a4dd-124">Remarks</span></span>

<span data-ttu-id="5a4dd-125">Wenn  _kein Abschnitt_ oder  _Segment_ vorhanden ist, gibt Microsoft Visio #REF! zurück.</span><span class="sxs-lookup"><span data-stu-id="5a4dd-125">If  _section_ or  _segment_ does not exist, Microsoft Visio returns #REF!.</span></span> 
  
<span data-ttu-id="5a4dd-126">Wenn Sie einen  _Segmentwert_ enthalten, gibt PATHLENGTH nur die Länge dieses Abschnitts zurück.</span><span class="sxs-lookup"><span data-stu-id="5a4dd-126">If you include a  _segment_ value, PATHLENGTH returns the length of that segment only.</span></span> 
  

