---
title: PidNameAcceptLanguage (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidNameAcceptLanguage
api_type:
- COM
ms.assetid: 4b202bc1-f718-446a-950f-634ffee47baf
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 855610c43cfaa64fa69e6987743b137b188d84a4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360942"
---
# <a name="pidnameacceptlanguage-canonical-property"></a><span data-ttu-id="778de-103">PidNameAcceptLanguage (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="778de-103">PidNameAcceptLanguage Canonical Property</span></span>

  
  
<span data-ttu-id="778de-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="778de-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="778de-105">Enthält einen [RFC3282] Accept-Language Kopfzeilenfeldwert.</span><span class="sxs-lookup"><span data-stu-id="778de-105">Contains an [RFC3282] Accept-Language header field value.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="778de-106">Anzeigenamen:</span><span class="sxs-lookup"><span data-stu-id="778de-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="778de-107">AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="778de-107">AcceptLanguage</span></span>  <br/> |
|<span data-ttu-id="778de-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="778de-108">Property set:</span></span>  <br/> |<span data-ttu-id="778de-109">PS_INTERNET_HEADERS</span><span class="sxs-lookup"><span data-stu-id="778de-109">PS_INTERNET_HEADERS</span></span>  <br/> |
|<span data-ttu-id="778de-110">Eigenschaftsname:</span><span class="sxs-lookup"><span data-stu-id="778de-110">Property name:</span></span>  <br/> |<span data-ttu-id="778de-111">Accept-Language</span><span class="sxs-lookup"><span data-stu-id="778de-111">Accept-Language</span></span>  <br/> |
|<span data-ttu-id="778de-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="778de-112">Data type:</span></span>  <br/> |<span data-ttu-id="778de-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="778de-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="778de-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="778de-114">Area:</span></span>  <br/> |<span data-ttu-id="778de-115">E-Mails</span><span class="sxs-lookup"><span data-stu-id="778de-115">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="778de-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="778de-116">Remarks</span></span>

<span data-ttu-id="778de-117">Zum Festlegen des Werts dieser Eigenschaft sollten Multipurpose Internet Message Extensions (MIME)-Clients ein Accept-Language mit dem gewünschten Wert schreiben.</span><span class="sxs-lookup"><span data-stu-id="778de-117">To set the value of this property, Multipurpose Internet Message Extensions (MIME) clients should write an Accept-Language header field with the desired value.</span></span> <span data-ttu-id="778de-118">MIME-Clients können stattdessen ein X-Accept-Language-Kopfzeilenfeld schreiben.</span><span class="sxs-lookup"><span data-stu-id="778de-118">MIME clients may write an X-Accept-Language header field instead.</span></span> <span data-ttu-id="778de-119">MIME-Reader sollten den Wert eines der beiden Kopfzeilenfelds in den Wert dieser Eigenschaft kopieren.</span><span class="sxs-lookup"><span data-stu-id="778de-119">MIME readers should copy the value of either header field to the value of this property.</span></span> <span data-ttu-id="778de-120">Wenn beide Kopfzeilenfelder vorhanden sind, sollten MIME-Leser das Accept-Language verwenden.</span><span class="sxs-lookup"><span data-stu-id="778de-120">If both header fields are present, MIME readers should use the Accept-Language header field.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="778de-121">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="778de-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="778de-122">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="778de-122">Protocol specifications</span></span>

<span data-ttu-id="778de-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="778de-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="778de-124">Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="778de-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="778de-125">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="778de-125">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="778de-126">Konvertiert von Internetstandard-E-Mail-Konventionen in Nachrichtenobjekte.</span><span class="sxs-lookup"><span data-stu-id="778de-126">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="778de-127">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="778de-127">Header files</span></span>

<span data-ttu-id="778de-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="778de-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="778de-129">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="778de-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="778de-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="778de-130">See also</span></span>



[<span data-ttu-id="778de-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="778de-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="778de-132">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="778de-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="778de-133">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="778de-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="778de-134">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="778de-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

