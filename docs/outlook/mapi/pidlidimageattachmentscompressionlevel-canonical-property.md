---
title: Kanonische PidLidImageAttachmentsCompressionLevel-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidImageAttachmentsCompressionLevel
api_type:
- COM
ms.assetid: cc169ba8-e9b7-42ad-8f0e-77b0843f95ea
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 13e2ac93e7e3ba46bf25b26e76bd44c15f2b89e2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793624"
---
# <a name="pidlidimageattachmentscompressionlevel-canonical-property"></a><span data-ttu-id="d0f81-103">Kanonische PidLidImageAttachmentsCompressionLevel-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d0f81-103">PidLidImageAttachmentsCompressionLevel Canonical Property</span></span>

  
  
<span data-ttu-id="d0f81-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d0f81-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d0f81-105">Definiert eine Komprimierungsebene auf Bildanlagen angewendet.</span><span class="sxs-lookup"><span data-stu-id="d0f81-105">Defines a compression level to apply on image attachments.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d0f81-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="d0f81-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d0f81-107">dispidImgAttchmtsCompressLevel</span><span class="sxs-lookup"><span data-stu-id="d0f81-107">dispidImgAttchmtsCompressLevel</span></span>  <br/> |
|<span data-ttu-id="d0f81-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="d0f81-108">Property set:</span></span>  <br/> |<span data-ttu-id="d0f81-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="d0f81-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="d0f81-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="d0f81-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="d0f81-111">0x00008593</span><span class="sxs-lookup"><span data-stu-id="d0f81-111">0x00008593</span></span>  <br/> |
|<span data-ttu-id="d0f81-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="d0f81-112">Data type:</span></span>  <br/> |<span data-ttu-id="d0f81-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="d0f81-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="d0f81-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="d0f81-114">Area:</span></span>  <br/> |<span data-ttu-id="d0f81-115">Laufzeit-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="d0f81-115">Run-time configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d0f81-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d0f81-116">Remarks</span></span>

<span data-ttu-id="d0f81-117">Im folgenden sind die gültigen Komprimierung Ebenen:</span><span class="sxs-lookup"><span data-stu-id="d0f81-117">The following are valid compression levels:</span></span>
  
```cpp
enum PictureCompressLevel
{
 pclOriginal = 0,
 pclEmail = 1,
 pclWeb = 2,
 pclDocuments = 3,
};
```

## <a name="related-resources"></a><span data-ttu-id="d0f81-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="d0f81-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d0f81-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="d0f81-119">Protocol specifications</span></span>

<span data-ttu-id="d0f81-120">[[MS-OXPROPS]]</span><span class="sxs-lookup"><span data-stu-id="d0f81-120">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="d0f81-121">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="d0f81-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d0f81-122">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="d0f81-122">Header files</span></span>

<span data-ttu-id="d0f81-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d0f81-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="d0f81-124">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="d0f81-124">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d0f81-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d0f81-125">See also</span></span>



[<span data-ttu-id="d0f81-126">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d0f81-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d0f81-127">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d0f81-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d0f81-128">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="d0f81-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d0f81-129">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="d0f81-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
