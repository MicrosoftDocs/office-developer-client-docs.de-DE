---
title: Kanonische PidLidPostalAddressId-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidPostalAddressId
api_type:
- COM
ms.assetid: 30fdfb20-1e12-442a-bfa0-8c18c15fa5c3
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 6b344986989a47c4f1159fcf50c1d067ae716e98
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793728"
---
# <a name="pidlidpostaladdressid-canonical-property"></a><span data-ttu-id="28c6e-103">Kanonische PidLidPostalAddressId-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="28c6e-103">PidLidPostalAddressId Canonical Property</span></span>

  
  
<span data-ttu-id="28c6e-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="28c6e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="28c6e-105">Gibt an, welche physische Adresse des Kontakts die e-Mail-Adresse ist.</span><span class="sxs-lookup"><span data-stu-id="28c6e-105">Specifies which physical address is the contact's mailing address.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="28c6e-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="28c6e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="28c6e-107">dispidPostalAddressId</span><span class="sxs-lookup"><span data-stu-id="28c6e-107">dispidPostalAddressId</span></span>  <br/> |
|<span data-ttu-id="28c6e-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="28c6e-108">Property set:</span></span>  <br/> |<span data-ttu-id="28c6e-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="28c6e-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="28c6e-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="28c6e-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="28c6e-111">0x00008022</span><span class="sxs-lookup"><span data-stu-id="28c6e-111">0x00008022</span></span>  <br/> |
|<span data-ttu-id="28c6e-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="28c6e-112">Data type:</span></span>  <br/> |<span data-ttu-id="28c6e-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="28c6e-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="28c6e-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="28c6e-114">Area:</span></span>  <br/> |<span data-ttu-id="28c6e-115">Kontakt</span><span class="sxs-lookup"><span data-stu-id="28c6e-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="28c6e-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="28c6e-116">Remarks</span></span>

<span data-ttu-id="28c6e-117">Wenn dieser Parameter angegeben wurde, muss diese Eigenschaft einen der Werte haben, die in der folgenden Tabelle oder in [[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="28c6e-117">If present, this property must have one of the values that are specified in the table below or in [[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx).</span></span> <span data-ttu-id="28c6e-118">Wenn dies nicht festgelegt ist, die Anwendung sollte wird davon ausgegangen, dass der Wert "0 x 00000000" ist.</span><span class="sxs-lookup"><span data-stu-id="28c6e-118">If not set, the application should assume that the value is "0x00000000".</span></span>
  
|<span data-ttu-id="28c6e-119">**Wert**</span><span class="sxs-lookup"><span data-stu-id="28c6e-119">**Value**</span></span>|<span data-ttu-id="28c6e-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="28c6e-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="28c6e-121">0x00000000</span><span class="sxs-lookup"><span data-stu-id="28c6e-121">0x00000000</span></span>  <br/> |<span data-ttu-id="28c6e-122">Keine Adresse ist als die Adresse ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="28c6e-122">No address is selected as the mailing address.</span></span> <span data-ttu-id="28c6e-123">**PR_STREET_ADDRESS** ([PidTagStreetAddress](pidtagstreetaddress-canonical-property.md)) **PR_LOCALITY** ([PidTagLocality](pidtaglocality-canonical-property.md)), **PR_STATE_OR_PROVINCE** ([PidTagStateOrProvince](pidtagstateorprovince-canonical-property.md)), **PR_POSTAL_CODE** ([PidTagPostalCode](pidtagpostalcode-canonical-property.md)), **PR_COUNTRY** ([ PidTagCountry](pidtagcountry-canonical-property.md)), **DispidAddressCountryCode** ([PidLidAddressCountryCode](pidlidaddresscountrycode-canonical-property.md)) und **PR_POSTAL_ADDRESS** ([PidTagPostalAddress](pidtagpostaladdress-canonical-property.md)) muss nicht festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="28c6e-123">**PR_STREET_ADDRESS** ([PidTagStreetAddress](pidtagstreetaddress-canonical-property.md)), **PR_LOCALITY** ([PidTagLocality](pidtaglocality-canonical-property.md)), **PR_STATE_OR_PROVINCE** ([PidTagStateOrProvince](pidtagstateorprovince-canonical-property.md)), **PR_POSTAL_CODE** ([PidTagPostalCode](pidtagpostalcode-canonical-property.md)), **PR_COUNTRY** ([PidTagCountry](pidtagcountry-canonical-property.md)), **dispidAddressCountryCode** ([PidLidAddressCountryCode](pidlidaddresscountrycode-canonical-property.md)), and **PR_POSTAL_ADDRESS** ([PidTagPostalAddress](pidtagpostaladdress-canonical-property.md)) all must not be set.</span></span>  <br/> |
|<span data-ttu-id="28c6e-124">0x00000001</span><span class="sxs-lookup"><span data-stu-id="28c6e-124">0x00000001</span></span>  <br/> |<span data-ttu-id="28c6e-125">Die Home-Adresse ist die Adresse.</span><span class="sxs-lookup"><span data-stu-id="28c6e-125">The Home Address is the mailing address.</span></span> <span data-ttu-id="28c6e-126">Die Werte der **PR_STREET_ADDRESS**, **PR_LOCALITY**, **PR_STATE_OR_PROVINCE**, **PR_POSTAL_CODE**, **PR_POST_OFFICE_BOX** ([PidTagPostOfficeBox](pidtagpostofficebox-canonical-property.md)), **PR_COUNTRY**, **dispidAddressCountryCode **, und **PR_POSTAL_ADDRESS** -Eigenschaften auf die Werte von der **PR_HOME_ADDRESS_STREET** ([PidTagHomeAddressStreet](pidtaghomeaddressstreet-canonical-property.md)) **PR_HOME_ADDRESS_CITY** ([PidTagHomeAddressCity](pidtaghomeaddresscity-canonical-property.md)) **PR_HOME_ gleich sein ADDRESS_STATE_OR_PROVINCE** ([PidTagHomeAddressStateOrProvince](pidtaghomeaddressstateorprovince-canonical-property.md)) **PR_HOME_ADDRESS_POSTAL_CODE** ([PidTagHomeAddressPostalCode](pidtaghomeaddresspostalcode-canonical-property.md)), **PR_HOME_ADDRESS_POST_OFFICE_BOX** ([ PidTagHomeAddressPostOfficeBox](pidtaghomeaddresspostofficebox-canonical-property.md)), **PR_HOME_ADDRESS_COUNTRY** ([PidTagHomeAddressCountry](pidtaghomeaddresscountry-canonical-property.md)), **DispidHomeAddressCountryCode** ([PidLidHomeAddressCountryCode](pidlidhomeaddresscountrycode-canonical-property.md)) und **DispidHomeAddress** () [PidLidHomeAddress](pidlidhomeaddress-canonical-property.md)) Eigenschaften fest.</span><span class="sxs-lookup"><span data-stu-id="28c6e-126">The values of the **PR_STREET_ADDRESS**, **PR_LOCALITY**, **PR_STATE_OR_PROVINCE**, **PR_POSTAL_CODE**, **PR_POST_OFFICE_BOX** ([PidTagPostOfficeBox](pidtagpostofficebox-canonical-property.md)), **PR_COUNTRY**, **dispidAddressCountryCode**, and **PR_POSTAL_ADDRESS** properties must be equal to the values of the **PR_HOME_ADDRESS_STREET** ([PidTagHomeAddressStreet](pidtaghomeaddressstreet-canonical-property.md)), **PR_HOME_ADDRESS_CITY** ([PidTagHomeAddressCity](pidtaghomeaddresscity-canonical-property.md)), **PR_HOME_ADDRESS_STATE_OR_PROVINCE** ([PidTagHomeAddressStateOrProvince](pidtaghomeaddressstateorprovince-canonical-property.md)), **PR_HOME_ADDRESS_POSTAL_CODE** ([PidTagHomeAddressPostalCode](pidtaghomeaddresspostalcode-canonical-property.md)), **PR_HOME_ADDRESS_POST_OFFICE_BOX** ([PidTagHomeAddressPostOfficeBox](pidtaghomeaddresspostofficebox-canonical-property.md)), **PR_HOME_ADDRESS_COUNTRY** ([PidTagHomeAddressCountry](pidtaghomeaddresscountry-canonical-property.md)), **dispidHomeAddressCountryCode** ([PidLidHomeAddressCountryCode](pidlidhomeaddresscountrycode-canonical-property.md)), and **dispidHomeAddress** ([PidLidHomeAddress](pidlidhomeaddress-canonical-property.md)) properties, respectively.</span></span>  <br/> |
|<span data-ttu-id="28c6e-127">0x00000002</span><span class="sxs-lookup"><span data-stu-id="28c6e-127">0x00000002</span></span>  <br/> |<span data-ttu-id="28c6e-128">Die Geschäftsadresse ist die Postanschrift.</span><span class="sxs-lookup"><span data-stu-id="28c6e-128">The Work Address is the mailing address.</span></span> <span data-ttu-id="28c6e-129">Die Werte der **PR_STREET_ADDRESS**, **PR_LOCALITY**, **PR_STATE_OR_PROVINCE**, **PR_POSTAL_CODE**, **PR_POST_OFFICE_BOX**, **PR_COUNTRY**, **DispidAddressCountryCode**und **PR_POSTAL_ADDRESS **Eigenschaften muss die Werte der **DispidWorkAddressStreet** ([PidLidWorkAddressStreet](pidlidworkaddressstreet-canonical-property.md)) **DispidWorkAddressCity** ([PidLidWorkAddressCity](pidlidworkaddresscity-canonical-property.md)) **DispidWorkAddressState** ([ gleich PidLidWorkAddressState](pidlidworkaddressstate-canonical-property.md)), **DispidWorkAddressPostalCode** ([PidLidWorkAddressPostalCode](pidlidworkaddresspostalcode-canonical-property.md)) **DispidWorkAddressPostOfficeBox** ([PidLidWorkAddressPostOfficeBox](pidlidworkaddresspostofficebox-canonical-property.md)) **DispidWorkAddressCountry **([PidLidWorkAddressCountry](pidlidworkaddresscountry-canonical-property.md)) **DispidWorkAddressCountryCode** ([PidLidWorkAddressCountryCode](pidlidworkaddresscountrycode-canonical-property.md)) und **DispidWorkAddress** ([PidLidWorkAddress](pidlidworkaddress-canonical-property.md))-Eigenschaften fest.</span><span class="sxs-lookup"><span data-stu-id="28c6e-129">The values of the **PR_STREET_ADDRESS**, **PR_LOCALITY**, **PR_STATE_OR_PROVINCE**, **PR_POSTAL_CODE**, **PR_POST_OFFICE_BOX**, **PR_COUNTRY**, **dispidAddressCountryCode**, and **PR_POSTAL_ADDRESS** properties must be equal to the values of the **dispidWorkAddressStreet** ([PidLidWorkAddressStreet](pidlidworkaddressstreet-canonical-property.md)), **dispidWorkAddressCity** ([PidLidWorkAddressCity](pidlidworkaddresscity-canonical-property.md)), **dispidWorkAddressState** ([PidLidWorkAddressState](pidlidworkaddressstate-canonical-property.md)), **dispidWorkAddressPostalCode** ([PidLidWorkAddressPostalCode](pidlidworkaddresspostalcode-canonical-property.md)), **dispidWorkAddressPostOfficeBox** ([PidLidWorkAddressPostOfficeBox](pidlidworkaddresspostofficebox-canonical-property.md)), **dispidWorkAddressCountry** ([PidLidWorkAddressCountry](pidlidworkaddresscountry-canonical-property.md)), **dispidWorkAddressCountryCode** ([PidLidWorkAddressCountryCode](pidlidworkaddresscountrycode-canonical-property.md)), and **dispidWorkAddress** ([PidLidWorkAddress](pidlidworkaddress-canonical-property.md)) properties, respectively.</span></span>  <br/> |
|<span data-ttu-id="28c6e-130">0 x 00000003</span><span class="sxs-lookup"><span data-stu-id="28c6e-130">0x00000003</span></span>  <br/> |<span data-ttu-id="28c6e-131">Weitere Adresse ist die Adresse.</span><span class="sxs-lookup"><span data-stu-id="28c6e-131">The Other Address is the mailing address.</span></span> <span data-ttu-id="28c6e-132">Die Werte der, **PR_STREET_ADDRESS** **PR_LOCALITY**, **PR_STATE_OR_PROVINCE**, **PR_POSTAL_CODE**, **PR_POST_OFFICE_BOX**, **PR_COUNTRY**, **DispidAddressCountryCode**und **PR_POSTAL_ADDRESS **Eigenschaften muss die Werte der **PR_OTHER_ADDRESS_STREET** ([PidTagOtherAddressStreet](pidtagotheraddressstreet-canonical-property.md)) **PR_OTHER_ADDRESS_CITY** ([PidTagOtherAddressCity](pidtagotheraddresscity-canonical-property.md)) **PR_OTHER_ADDRESS_STATE_OR_PROVINCE** (gleich [PidTagOtherAddressStateOrProvince](pidtagotheraddressstateorprovince-canonical-property.md)) **PR_OTHER_ADDRESS_POSTAL_CODE** ([PidTagOtherAddressPostalCode](pidtagotheraddresspostalcode-canonical-property.md)), **PR_OTHER_ADDRESS_POST_OFFICE_BOX** ([PidTagOtherAddressPostOfficeBox](pidtagotheraddresspostofficebox-canonical-property.md)), ** DispidOtherAddressCountryCode** ([PidLidOtherAddressCountryCode](pidlidotheraddresscountrycode-canonical-property.md)) und **DispidOtherAddress** ([PidLidOtherAddress](pidlidotheraddress-canonical-property.md))-Eigenschaften fest.</span><span class="sxs-lookup"><span data-stu-id="28c6e-132">The values of the, **PR_STREET_ADDRESS**, **PR_LOCALITY**, **PR_STATE_OR_PROVINCE**, **PR_POSTAL_CODE**, **PR_POST_OFFICE_BOX**, **PR_COUNTRY**, **dispidAddressCountryCode**, and **PR_POSTAL_ADDRESS** properties must be equal to the values of the **PR_OTHER_ADDRESS_STREET** ([PidTagOtherAddressStreet](pidtagotheraddressstreet-canonical-property.md)), **PR_OTHER_ADDRESS_CITY** ([PidTagOtherAddressCity](pidtagotheraddresscity-canonical-property.md)), **PR_OTHER_ADDRESS_STATE_OR_PROVINCE** ([PidTagOtherAddressStateOrProvince](pidtagotheraddressstateorprovince-canonical-property.md)), **PR_OTHER_ADDRESS_POSTAL_CODE** ([PidTagOtherAddressPostalCode](pidtagotheraddresspostalcode-canonical-property.md)), **PR_OTHER_ADDRESS_POST_OFFICE_BOX** ([PidTagOtherAddressPostOfficeBox](pidtagotheraddresspostofficebox-canonical-property.md)), **dispidOtherAddressCountryCode** ([PidLidOtherAddressCountryCode](pidlidotheraddresscountrycode-canonical-property.md)), and **dispidOtherAddress** ([PidLidOtherAddress](pidlidotheraddress-canonical-property.md)) properties, respectively.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="28c6e-133">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="28c6e-133">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="28c6e-134">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="28c6e-134">Protocol specifications</span></span>

<span data-ttu-id="28c6e-135">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="28c6e-135">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="28c6e-136">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="28c6e-136">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="28c6e-137">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="28c6e-137">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="28c6e-138">Gibt die Eigenschaften und Operationen, die für Kontakte und persönliche Verteilerlisten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="28c6e-138">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="28c6e-139">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="28c6e-139">Header files</span></span>

<span data-ttu-id="28c6e-140">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="28c6e-140">Mapidefs.h</span></span>
  
> <span data-ttu-id="28c6e-141">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="28c6e-141">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="28c6e-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="28c6e-142">See also</span></span>



[<span data-ttu-id="28c6e-143">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="28c6e-143">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="28c6e-144">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="28c6e-144">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="28c6e-145">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="28c6e-145">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="28c6e-146">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="28c6e-146">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
