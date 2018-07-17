---
title: ScCopyProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScCopyProps
api_type:
- COM
ms.assetid: 08bc256c-9706-4f3e-9a12-3e9cca5e4caa
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 979415f1d792f92e593a7073cc84cfd6ba832b6c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795437"
---
# <a name="sccopyprops"></a><span data-ttu-id="fc6f1-103">ScCopyProps</span><span class="sxs-lookup"><span data-stu-id="fc6f1-103">ScCopyProps</span></span>

  
  
<span data-ttu-id="fc6f1-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fc6f1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fc6f1-105">Kopiert die Eigenschaften, die durch ein Array von [SPropValue](spropvalue.md) Strukturen zu einem neuen Ziel definiert.</span><span class="sxs-lookup"><span data-stu-id="fc6f1-105">Copies the properties defined by an array of [SPropValue](spropvalue.md) structures to a new destination.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fc6f1-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="fc6f1-106">Header file:</span></span>  <br/> |<span data-ttu-id="fc6f1-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="fc6f1-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="fc6f1-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="fc6f1-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="fc6f1-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="fc6f1-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="fc6f1-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="fc6f1-110">Called by:</span></span>  <br/> |<span data-ttu-id="fc6f1-111">Clientanwendungen und -Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="fc6f1-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScCopyProps(
  int cprop,
  LPSPropValue rgprop,
  LPVOID pvDst,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a><span data-ttu-id="fc6f1-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="fc6f1-112">Parameters</span></span>

 <span data-ttu-id="fc6f1-113">_cprop_</span><span class="sxs-lookup"><span data-stu-id="fc6f1-113">_cprop_</span></span>
  
> <span data-ttu-id="fc6f1-114">[in] Anzahl der Eigenschaften kopiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="fc6f1-114">[in] Count of properties to be copied.</span></span> 
    
 <span data-ttu-id="fc6f1-115">_rgprop_</span><span class="sxs-lookup"><span data-stu-id="fc6f1-115">_rgprop_</span></span>
  
> <span data-ttu-id="fc6f1-116">[in] Zeiger auf ein Array von [SPropValue](spropvalue.md) -Strukturen, die definieren die Eigenschaften kopiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="fc6f1-116">[in] Pointer to an array of [SPropValue](spropvalue.md) structures that define the properties to be copied.</span></span> <span data-ttu-id="fc6f1-117">Der Parameter _Rgprop_ muss nicht an den Anfang des Arrays zeigen, aber es muss zeigen Sie auf den Anfang einer der **SPropValue** Strukturen im Array.</span><span class="sxs-lookup"><span data-stu-id="fc6f1-117">The  _rgprop_ parameter does not have to point to the beginning of the array, but it must point to the beginning of one of the **SPropValue** structures in the array.</span></span> 
    
 <span data-ttu-id="fc6f1-118">_pvDst_</span><span class="sxs-lookup"><span data-stu-id="fc6f1-118">_pvDst_</span></span>
  
> <span data-ttu-id="fc6f1-119">[in] Zeiger auf die Ausgangsposition im Arbeitsspeicher, dem diese Funktion die Eigenschaften kopiert.</span><span class="sxs-lookup"><span data-stu-id="fc6f1-119">[in] Pointer to the initial position in memory to which this function copies the properties.</span></span> 
    
 <span data-ttu-id="fc6f1-120">_PCB_</span><span class="sxs-lookup"><span data-stu-id="fc6f1-120">_pcb_</span></span>
  
> <span data-ttu-id="fc6f1-121">[out] Optional Zeiger auf die Größe in Bytes, den Block mit Speicher durch den Parameter _PvDst_ .</span><span class="sxs-lookup"><span data-stu-id="fc6f1-121">[out] Optional pointer to the size, in bytes, of the block of memory pointed to by the  _pvDst_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="fc6f1-122">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="fc6f1-122">Return value</span></span>

<span data-ttu-id="fc6f1-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="fc6f1-123">S_OK</span></span>
  
> <span data-ttu-id="fc6f1-124">Eigenschaften wurden erfolgreich kopiert.</span><span class="sxs-lookup"><span data-stu-id="fc6f1-124">Properties were copied successfully.</span></span>
    
<span data-ttu-id="fc6f1-125">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="fc6f1-125">MAPI_E_INVALID_PARAMETER</span></span>
  
> <span data-ttu-id="fc6f1-126">Unbekannte Eigenschaft vom Typ aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="fc6f1-126">An unknown property type was encountered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="fc6f1-127">Hinweise</span><span class="sxs-lookup"><span data-stu-id="fc6f1-127">Remarks</span></span>

<span data-ttu-id="fc6f1-128">Das neue Array und ihre Daten befinden sich in einem Puffer mit einer einzelnen Reservierung erstellt, und die [ScRelocProps](screlocprops.md) -Funktion kann zum Anpassen der Zeiger in den einzelnen [SPropValue](spropvalue.md) Strukturen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fc6f1-128">The new array and its data reside in a buffer created with a single allocation, and the [ScRelocProps](screlocprops.md) function can be used to adjust the pointers in the individual [SPropValue](spropvalue.md) structures.</span></span> <span data-ttu-id="fc6f1-129">Bevor Sie diese Anpassung sind der Zeiger gültig.</span><span class="sxs-lookup"><span data-stu-id="fc6f1-129">Prior to this adjustment, the pointers are valid.</span></span> 
  
 <span data-ttu-id="fc6f1-130">**ScCopyProps** behält die Reihenfolge der ursprünglichen Eigenschaft für Array der kopierten-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="fc6f1-130">**ScCopyProps** maintains the original property order for the copied property array.</span></span> 
  
<span data-ttu-id="fc6f1-131">Der Parameter _pcb_ ist optional. Wenn nicht NULL ist, wird es auf die Anzahl von Bytes, die im Parameter _PvDst_ gespeichert festgelegt.</span><span class="sxs-lookup"><span data-stu-id="fc6f1-131">The  _pcb_ parameter is optional; if it is not NULL, it is set to the number of bytes stored in the  _pvDst_ parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="fc6f1-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fc6f1-132">See also</span></span>



[<span data-ttu-id="fc6f1-133">ScDupPropset</span><span class="sxs-lookup"><span data-stu-id="fc6f1-133">ScDupPropset</span></span>](scduppropset.md)
