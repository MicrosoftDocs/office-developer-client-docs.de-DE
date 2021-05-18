---
title: PidTagRoamingDictionary (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRoamingDictionary
api_type:
- COM
ms.assetid: 40b50181-f88c-40ee-b3d0-a36dd36c158e
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 4b2aa12b1b81dfd218781a839f5f84881763ef06
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359549"
---
# <a name="pidtagroamingdictionary-canonical-property"></a><span data-ttu-id="4cd88-103">PidTagRoamingDictionary (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="4cd88-103">PidTagRoamingDictionary Canonical Property</span></span>

<span data-ttu-id="4cd88-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4cd88-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4cd88-105">Enthält ein XML-Dokument, das das Roamingwörterbuch beschreibt.</span><span class="sxs-lookup"><span data-stu-id="4cd88-105">Contains an XML document that describes the roaming dictionary.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4cd88-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="4cd88-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4cd88-107">PR_ROAMING_DICTIONARY</span><span class="sxs-lookup"><span data-stu-id="4cd88-107">PR_ROAMING_DICTIONARY</span></span>  <br/> |
|<span data-ttu-id="4cd88-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="4cd88-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4cd88-109">0x7C07</span><span class="sxs-lookup"><span data-stu-id="4cd88-109">0x7C07</span></span>  <br/> |
|<span data-ttu-id="4cd88-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="4cd88-110">Data type:</span></span>  <br/> |<span data-ttu-id="4cd88-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="4cd88-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="4cd88-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="4cd88-112">Area:</span></span>  <br/> |<span data-ttu-id="4cd88-113">Konfiguration</span><span class="sxs-lookup"><span data-stu-id="4cd88-113">Configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4cd88-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4cd88-114">Remarks</span></span>

<span data-ttu-id="4cd88-115">Diese Eigenschaft enthält ein UNICODE-XML-Dokument, das die UTF8-Codierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="4cd88-115">This property contains a UNICODE XML document that is using UTF8 encoding.</span></span> <span data-ttu-id="4cd88-116">Eine Nachricht mit einem Wörterbuchdatenstrom muss diese Eigenschaft mit dem folgenden Schema festlegen:</span><span class="sxs-lookup"><span data-stu-id="4cd88-116">A message with a dictionary stream must set this property with the following schema:</span></span>
  
```xml
<?xml version="1.0" encoding="utf-8"?> 
<xs:schema targetNamespace="Dictionary.xsd" xmlns="Dictionary.xsd" xmlns:xs="https://www.w3.org/2001/XMLSchema"> 
   <xs:element name="UserConfiguration"> 
   <xs:complexType> 
   <xs:sequence> 
   <xs:element name="Info"> 
   <xs:complexType> 
   <xs:sequence /> 
   <xs:attribute name="version" type="VersionString"> 
   </xs:attribute> 
   </xs:complexType>
```

<span data-ttu-id="4cd88-117">Im Folgenden finden Sie ein XML-Beispieldokument, das in dieser Eigenschaft in einer Konfigurationsdatennachricht gespeichert ist:</span><span class="sxs-lookup"><span data-stu-id="4cd88-117">The following is a sample XML document stored in this property on a Configuration Data message:</span></span> 
  
```xml
<?xml version="1.0"?> 
<UserConfiguration> 
<Info version="Outlook.12"/> 
<Data> <e k="18-piAutoProcess" v="3-True"/> 
<e k="18-piRemindDefault" v="9-15"/> 
<e k="18-piReminderUpgradeTime" v="9-212864507"/> 
<e k="18-OLPrefsVersion" v="9-1"/> 
</Data> 
</UserConfiguration>
```

## <a name="related-resources"></a><span data-ttu-id="4cd88-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="4cd88-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4cd88-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="4cd88-119">Protocol specifications</span></span>

<span data-ttu-id="4cd88-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4cd88-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4cd88-121">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="4cd88-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4cd88-122">[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4cd88-122">[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4cd88-123">Gibt den Speicherort und die Eigenschaften von Client- und Serverkonfigurationsdaten an, z. B. freigegebene Kategorielisten und Arbeitszeiten.</span><span class="sxs-lookup"><span data-stu-id="4cd88-123">Specifies the location and properties of client and server configuration data, such as shared category lists and working hours.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4cd88-124">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="4cd88-124">Header files</span></span>

<span data-ttu-id="4cd88-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4cd88-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="4cd88-126">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="4cd88-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="4cd88-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="4cd88-127">Mapitags.h</span></span>
  
> <span data-ttu-id="4cd88-128">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="4cd88-128">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4cd88-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4cd88-129">See also</span></span>



[<span data-ttu-id="4cd88-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4cd88-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4cd88-131">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="4cd88-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4cd88-132">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="4cd88-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4cd88-133">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="4cd88-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

