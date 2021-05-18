---
title: Eigenschaftsnamen und Eigenschaftensätze
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cb216f5c-c965-4372-a15b-82090a410266
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: fa9d6afcaf1b360f37e8c8873c9d1a823fcd4888
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328546"
---
# <a name="property-names-and-property-sets"></a><span data-ttu-id="75e82-103">Eigenschaftsnamen und Eigenschaftensätze</span><span class="sxs-lookup"><span data-stu-id="75e82-103">Property Names and Property Sets</span></span>

  
  
<span data-ttu-id="75e82-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="75e82-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="75e82-105">Der Name jeder benannten Eigenschaft hat zwei Teile:</span><span class="sxs-lookup"><span data-stu-id="75e82-105">The name of every named property has two parts:</span></span>
  
- <span data-ttu-id="75e82-106">Eine global eindeutige ID oder GUID, die einen Eigenschaftensatz angibt.</span><span class="sxs-lookup"><span data-stu-id="75e82-106">A globally unique identifier, or GUID, that specifies a property set.</span></span>
    
- <span data-ttu-id="75e82-107">Eine Unicode-Zeichenzeichenfolge oder ein numerischer 32-Bit-Wert.</span><span class="sxs-lookup"><span data-stu-id="75e82-107">A Unicode character string or 32-bit numeric value.</span></span> 
    
<span data-ttu-id="75e82-108">Namen benannter Eigenschaften werden mithilfe einer [MAPINAMEID-Struktur](mapinameid.md) beschrieben.</span><span class="sxs-lookup"><span data-stu-id="75e82-108">Names of named properties are described using a [MAPINAMEID](mapinameid.md) structure.</span></span> <span data-ttu-id="75e82-109">Diese Struktur enthält ein Element des Eigenschaftensatzs, ein Element zum Angeben des Namens im Numerischen oder Zeichenfolgenformat und ein Element zum Identifizieren des verwendeten Formats.</span><span class="sxs-lookup"><span data-stu-id="75e82-109">This structure contains a property set member, a member for specifying the name in either numeric or string format, and a member for identifying which format is used.</span></span> <span data-ttu-id="75e82-110">Da der Eigenschaftensatz Teil des Namens der Eigenschaft ist, ist er nicht optional.</span><span class="sxs-lookup"><span data-stu-id="75e82-110">Because the property set is part of the property's name, it is not optional.</span></span> <span data-ttu-id="75e82-111">MAPI hat mehrere Eigenschaftssätze für die Verwendung durch Clients und Dienstanbieter definiert, aber wenn ein vorhandener Eigenschaftensatz nicht geeignet ist, kann ein neuer Eigenschaftensatz definiert werden.</span><span class="sxs-lookup"><span data-stu-id="75e82-111">MAPI has defined several property sets for use by clients and service providers, but if an existing property set is inappropriate, a new property set can be defined.</span></span> <span data-ttu-id="75e82-112">Clients und Dienstanbieter können ihre eigenen Eigenschaftensätze definieren, indem sie [die CoCreateGUID-Funktion](https://msdn.microsoft.com/library/ms688568.aspx) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="75e82-112">Clients and service providers can define their own property sets by calling [CoCreateGUID](https://msdn.microsoft.com/library/ms688568.aspx) function.</span></span> <span data-ttu-id="75e82-113">In der Regel werden diese Eigenschaftssätze für benutzerdefinierte Clientanwendungen erstellt.</span><span class="sxs-lookup"><span data-stu-id="75e82-113">Typically these property sets are created for custom client applications.</span></span> 
  
<span data-ttu-id="75e82-114">Die Eigenschaftssätze von MAPI werden durch die folgenden Konstanten dargestellt:</span><span class="sxs-lookup"><span data-stu-id="75e82-114">MAPI's property sets are represented by the following constants:</span></span>
  
<span data-ttu-id="75e82-115">PS_MAPI</span><span class="sxs-lookup"><span data-stu-id="75e82-115">PS_MAPI</span></span>
  
<span data-ttu-id="75e82-116">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="75e82-116">PS_PUBLIC_STRINGS</span></span>
  
<span data-ttu-id="75e82-117">PS_ROUTING_EMAIL_ADDRESSES</span><span class="sxs-lookup"><span data-stu-id="75e82-117">PS_ROUTING_EMAIL_ADDRESSES</span></span>
  
<span data-ttu-id="75e82-118">PS_ROUTING_ADDRTYPE</span><span class="sxs-lookup"><span data-stu-id="75e82-118">PS_ROUTING_ADDRTYPE</span></span>
  
<span data-ttu-id="75e82-119">PS_ROUTING_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="75e82-119">PS_ROUTING_SEARCH_KEY</span></span>
  
<span data-ttu-id="75e82-120">PS_ROUTING_DISPLAY_NAME</span><span class="sxs-lookup"><span data-stu-id="75e82-120">PS_ROUTING_DISPLAY_NAME</span></span>
  
<span data-ttu-id="75e82-121">PS_ROUTING_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="75e82-121">PS_ROUTING_ENTRYID</span></span>
  
<span data-ttu-id="75e82-122">Der PS_MAPI-Eigenschaftssatz ist reserviert. Es wird von Dienstanbietern verwendet, um Namen für Eigenschaften mit Bezeichnern unterhalb des benannten Eigenschaftenbereichs zu generieren.</span><span class="sxs-lookup"><span data-stu-id="75e82-122">The PS_MAPI property set is reserved; it is used by service providers to generate names for properties with identifiers below the named property range.</span></span> <span data-ttu-id="75e82-123">Der PS_PUBLIC_STRINGS wird von Clients für benannte Eigenschaften von IPM-Nachrichten verwendet.</span><span class="sxs-lookup"><span data-stu-id="75e82-123">The PS_PUBLIC_STRINGS property set is used by clients for named properties of IPM messages.</span></span> <span data-ttu-id="75e82-124">Da benannte Eigenschaften im PS_PUBLIC_STRINGS-Eigenschaftssatz auf der Benutzeroberfläche eines Clients angezeigt werden, sollten nicht lesbare Nachrichten, z. B. solche, die zur IPC-Nachrichtenklasse gehören, vermeiden, benannte Eigenschaften mit diesem Eigenschaftensatz zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="75e82-124">Because named properties in the PS_PUBLIC_STRINGS property set appear in a client's user interface, nonvisible messages such as those that belong to the IPC message class should avoid creating named properties with this property set.</span></span> <span data-ttu-id="75e82-125">Stattdessen sollten sie Eigenschaften im nachrichtenklassenspezifischen Bereich erstellen, 0x6800 bis 0x7FFF.</span><span class="sxs-lookup"><span data-stu-id="75e82-125">Instead, they should create properties in the message class-specific range, 0x6800 through 0x7FFF.</span></span>
  
<span data-ttu-id="75e82-126">Die anderen Eigenschaftensätze enthalten benannte Eigenschaften, die Empfänger beschreiben, die in der Regel Mitglieder einer Routingliste sind.</span><span class="sxs-lookup"><span data-stu-id="75e82-126">The other property sets hold named properties describing recipients that are typically members of a routing list.</span></span> <span data-ttu-id="75e82-127">Mit demselben Informationstyp wie die Eigenschaften, die Empfängerlisteneigenschaften zugeordnet sind, werden Eigenschaften in diesen Eigenschaftensätzen von Gateways verstanden, um eine Zuordnung für ein Zielnachrichtensystem zu erfordern.</span><span class="sxs-lookup"><span data-stu-id="75e82-127">Containing the same type of information as the properties that are associated with recipient list properties, properties in these property sets are understood by gateways to require mapping for a target messaging system.</span></span> <span data-ttu-id="75e82-128">Da es fünf Arten von Informationen zum Beschreiben von Eigenschaften gibt, hat MAPI fünf verschiedene Eigenschaftensätze definiert.</span><span class="sxs-lookup"><span data-stu-id="75e82-128">Because there are five types of information for describing properties, MAPI has defined five different property sets.</span></span> <span data-ttu-id="75e82-129">Ein Client, der eine Nachricht sendet, die eine Adresse und einen Adresstyp für seine Routinglistenmitglieder enthalten muss, weist jedem Element in den Eigenschaftensätzen PS_ROUTING_EMAIL_ADDRESSES und PS_ROUTING_ADDRTYPE eine benannte Eigenschaft zu.</span><span class="sxs-lookup"><span data-stu-id="75e82-129">A client sending a message that must include an address and address type for its routing list members assigns a named property for each member in the PS_ROUTING_EMAIL_ADDRESSES and PS_ROUTING_ADDRTYPE property sets.</span></span> <span data-ttu-id="75e82-130">Dadurch wird sichergestellt, dass die Adresse und der Adresstyp beim Senden an ein fremdes Messagingsystem weiterhin praktikabel sind.</span><span class="sxs-lookup"><span data-stu-id="75e82-130">This ensures that the address and address type remain viable when sent to a foreign messaging system.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="75e82-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="75e82-131">See also</span></span>



[<span data-ttu-id="75e82-132">Benannte Eigenschaften MAPI</span><span class="sxs-lookup"><span data-stu-id="75e82-132">MAPI Named Properties</span></span>](mapi-named-properties.md)

