---
title: Kanonische PidLidCustomFlag-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidCustomFlag
api_type:
- COM
ms.assetid: bfb7fd1e-774f-9a2f-fbbe-ba7f68ed8663
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 5d97f56946512266bb7a08aa6b4a4ff78dded56a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793491"
---
# <a name="pidlidcustomflag-canonical-property"></a><span data-ttu-id="5cae4-103">Kanonische PidLidCustomFlag-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="5cae4-103">PidLidCustomFlag Canonical Property</span></span>

  
  
<span data-ttu-id="5cae4-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5cae4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5cae4-105">Eine Bitmaske, die angibt, wie eine Nachricht angepasst ist, beispielsweise mit benutzerdefinierten Eigenschaften gespeichert.</span><span class="sxs-lookup"><span data-stu-id="5cae4-105">A bitmask that specifies how a message is customized, for example, saved with custom properties.</span></span>
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="5cae4-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="5cae4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5cae4-107">dispidCustomFlag</span><span class="sxs-lookup"><span data-stu-id="5cae4-107">dispidCustomFlag</span></span>  <br/> |
|<span data-ttu-id="5cae4-108">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="5cae4-108">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="5cae4-109">0x00008251</span><span class="sxs-lookup"><span data-stu-id="5cae4-109">0x00008251</span></span>  <br/> |
|<span data-ttu-id="5cae4-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="5cae4-110">Data type:</span></span>  <br/> |<span data-ttu-id="5cae4-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="5cae4-111">PT_LONG</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5cae4-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5cae4-112">Remarks</span></span>

<span data-ttu-id="5cae4-113">Um den Wert dieser Eigenschaft abzurufen, zunächst mit dem **[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)** um das Eigenschafts-Tag zu erhalten, und geben Sie in **[IMAPIProp::GetProps](imapiprop-getprops.md)** zum Abrufen des Werts dieser Eigenschaftentag.</span><span class="sxs-lookup"><span data-stu-id="5cae4-113">To retrieve the value of this property, first use **[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)** to obtain the property tag, and then specify this property tag in **[IMAPIProp::GetProps](imapiprop-getprops.md)** to get the value.</span></span> 
  
<span data-ttu-id="5cae4-114">Mögliche Flags lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="5cae4-114">Possible Flags are as follows:</span></span>
  
****

|<span data-ttu-id="5cae4-115">**Konstante**</span><span class="sxs-lookup"><span data-stu-id="5cae4-115">**Constant**</span></span>|<span data-ttu-id="5cae4-116">**Wert**</span><span class="sxs-lookup"><span data-stu-id="5cae4-116">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5cae4-117">INSP_ONEOFFFLAGS</span><span class="sxs-lookup"><span data-stu-id="5cae4-117">INSP_ONEOFFFLAGS</span></span>  <br/> |<span data-ttu-id="5cae4-118">0x0D000000</span><span class="sxs-lookup"><span data-stu-id="5cae4-118">0x0D000000</span></span>  <br/> |
|<span data-ttu-id="5cae4-119">INSP_PROPDEFINITION</span><span class="sxs-lookup"><span data-stu-id="5cae4-119">INSP_PROPDEFINITION</span></span>  <br/> |<span data-ttu-id="5cae4-120">0x02000000</span><span class="sxs-lookup"><span data-stu-id="5cae4-120">0x02000000</span></span>  <br/> |
   
<span data-ttu-id="5cae4-121">Beim Aufruf von **IMAPIProp::GetIDsFromNames**, geben Sie die folgenden Werte für die **[MAPINAMEID](mapinameid.md)** -Struktur, die auf den Eingabeparameter *LppPropNames* zeigt.</span><span class="sxs-lookup"><span data-stu-id="5cae4-121">When calling **IMAPIProp::GetIDsFromNames**, specify the following values for the **[MAPINAMEID](mapinameid.md)** structure pointed to by the input parameter  *lppPropNames*  .</span></span> 
  
****

|<span data-ttu-id="5cae4-122">**Member**</span><span class="sxs-lookup"><span data-stu-id="5cae4-122">**Member**</span></span>|<span data-ttu-id="5cae4-123">**Value**</span><span class="sxs-lookup"><span data-stu-id="5cae4-123">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5cae4-124">x LpGuid:</span><span class="sxs-lookup"><span data-stu-id="5cae4-124">lpGuid:</span></span>  <br/> |<span data-ttu-id="5cae4-125">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="5cae4-125">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="5cae4-126">UlKind:</span><span class="sxs-lookup"><span data-stu-id="5cae4-126">ulKind:</span></span>  <br/> |<span data-ttu-id="5cae4-127">MNID_ID</span><span class="sxs-lookup"><span data-stu-id="5cae4-127">MNID_ID</span></span>  <br/> |
|<span data-ttu-id="5cae4-128">Kind.lID:</span><span class="sxs-lookup"><span data-stu-id="5cae4-128">Kind.lID:</span></span>  <br/> |<span data-ttu-id="5cae4-129">dispidCustomFlag</span><span class="sxs-lookup"><span data-stu-id="5cae4-129">dispidCustomFlag</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="5cae4-130">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="5cae4-130">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5cae4-131">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="5cae4-131">Protocol specifications</span></span>

<span data-ttu-id="5cae4-132">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5cae4-132">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5cae4-133">Enthält Eigenschaftendefinitionen an.</span><span class="sxs-lookup"><span data-stu-id="5cae4-133">Provides property set definitions.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5cae4-134">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="5cae4-134">Header files</span></span>

<span data-ttu-id="5cae4-135">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5cae4-135">Mapidefs.h</span></span>
  
> <span data-ttu-id="5cae4-136">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="5cae4-136">Provides data type definitions.</span></span>
    
<span data-ttu-id="5cae4-137">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="5cae4-137">Mapitags.h</span></span>
  
> <span data-ttu-id="5cae4-138">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="5cae4-138">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5cae4-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5cae4-139">See also</span></span>



[<span data-ttu-id="5cae4-140">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5cae4-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5cae4-141">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5cae4-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5cae4-142">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="5cae4-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5cae4-143">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="5cae4-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
