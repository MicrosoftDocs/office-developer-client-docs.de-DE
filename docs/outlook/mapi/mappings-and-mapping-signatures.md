---
title: Zuordnungen und Zuordnung Signaturen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 773f6671-cc21-4d1f-a11d-308bc71c852d
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 16f192ae816aba2dd0e34a42fba211c3ef70ba47
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793165"
---
# <a name="mappings-and-mapping-signatures"></a><span data-ttu-id="17cf0-103">Zuordnungen und Zuordnung Signaturen</span><span class="sxs-lookup"><span data-stu-id="17cf0-103">Mappings and Mapping Signatures</span></span>

  
  
<span data-ttu-id="17cf0-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="17cf0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="17cf0-105">Bei ein Dienstanbieter benannte Eigenschaften unterstützt, wird jeder Gruppe von-ID und Name-Paare als eine Zuordnung bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="17cf0-105">When a service provider supports named properties, each set of identifier and name pairs is referred to as a mapping.</span></span> <span data-ttu-id="17cf0-106">Dienstanbieter können eine Zuordnung eines oder mehrere unterstützen.</span><span class="sxs-lookup"><span data-stu-id="17cf0-106">Service providers can support one mapping or several.</span></span> <span data-ttu-id="17cf0-107">Dass wird eine Nachricht Speicheranbieter, z. B., können die Methoden **GetIDsFromNames** und **GetNamesFromIDs** für alle seine Nachricht, Ordner und Message Store Objekte arbeiten mit einer einzelnen Liste mit Namen und ihren entsprechenden IDs implementieren.</span><span class="sxs-lookup"><span data-stu-id="17cf0-107">That is, one message store provider, for example, can implement the **GetIDsFromNames** and **GetNamesFromIDs** methods for all of its message, folder, and message store objects to work with a single list of names and their corresponding identifiers.</span></span> <span data-ttu-id="17cf0-108">Eine andere Nachricht Speicheranbieter möglicherweise haben eine Liste für jeden Ordner und die darin enthaltenen Nachrichten oder eine eindeutige Liste für jede Nachricht und jeder Ordner implementieren.</span><span class="sxs-lookup"><span data-stu-id="17cf0-108">Another message store provider might have one list for every folder and the messages contained within it, or implement a unique list for every message and every folder.</span></span> <span data-ttu-id="17cf0-109">Nachricht-Anbieter, die eine eindeutige Zuordnung für jede Nachricht verwenden darf keine benannte Eigenschaften in ihren Ordner Inhalt Tabellen angezeigt werden, da für einen bestimmten Eigenschaftennamen, der Bezeichner für die Nachricht zu Nachricht unterscheiden sich zulassen.</span><span class="sxs-lookup"><span data-stu-id="17cf0-109">Message store providers that use a unique mapping for every message must not allow named properties to appear in their folder contents tables because for a given property name, the property identifier will differ from message to message.</span></span> <span data-ttu-id="17cf0-110">MAPI empfiehlt, dass der Anbieter ganz einfach und Arbeiten mit einer einzelnen Liste für alle ihre Objekte, einschließlich Tabellen.</span><span class="sxs-lookup"><span data-stu-id="17cf0-110">MAPI recommends that providers keep it simple and operate with a single list for all of their objects including tables.</span></span> 
  
<span data-ttu-id="17cf0-111">Für jede Zuordnung müssen Dienstanbieter eine Zuordnung Signatur angeben.</span><span class="sxs-lookup"><span data-stu-id="17cf0-111">For every mapping, service providers must supply a mapping signature.</span></span> <span data-ttu-id="17cf0-112">Eine Signatur Zuordnung ist ein Binärwert, in der Regel eine GUID, die eine Reihe von eigenschaftskennungen und ihre entsprechenden Namen eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="17cf0-112">A mapping signature is a binary value, usually a GUID, that uniquely identifies a set of property identifiers and their corresponding names.</span></span> <span data-ttu-id="17cf0-113">Zuordnung Signaturen werden in der Eigenschaft eines Objekts **PR_MAPPING_SIGNATURE** ([PidTagMappingSignature](pidtagmappingsignature-canonical-property.md)) gespeichert.</span><span class="sxs-lookup"><span data-stu-id="17cf0-113">Mapping signatures are stored in an object's **PR_MAPPING_SIGNATURE** ([PidTagMappingSignature](pidtagmappingsignature-canonical-property.md)) property.</span></span> <span data-ttu-id="17cf0-114">Dienstanbieter müssen ändern Sie den Wert für die **PR_MAPPING_SIGNATURE** -Eigenschaft immer auf die Zuordnung, das es darstellt, eine Änderung vorgenommen wird.</span><span class="sxs-lookup"><span data-stu-id="17cf0-114">Service providers must change the value for their **PR_MAPPING_SIGNATURE** property whenever a change is made to the mapping that it represents.</span></span> <span data-ttu-id="17cf0-115">Beispielsweise muss **PR_MAPPING_SIGNATURE** aktualisiert werden, wenn eine neue-ID zugeordnet, einen Namen oder einen neuen Namen ist und Bezeichner-Paar wird hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="17cf0-115">For example, **PR_MAPPING_SIGNATURE** must be updated if a new identifier is assigned to a name or a new name and identifier pair is added.</span></span> 
  
<span data-ttu-id="17cf0-116">Arbeiten mit der benannten Eigenschaft der Objekte Clients verwenden der Objekte **PR_MAPPING_SIGNATURE** Eigenschaften in Vergleiche und kopieren.</span><span class="sxs-lookup"><span data-stu-id="17cf0-116">Clients working with the named properties of objects use the objects' **PR_MAPPING_SIGNATURE** properties in comparison and copy operations.</span></span> <span data-ttu-id="17cf0-117">Zum Vergleichen mit der Eigenschaft Bezeichner, die auf zwei Objekte gehören, Clients, die nicht mit Zuordnung Signaturen [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) für beide Objekte zum Abrufen der Names für jede der Bezeichner aufrufen müssen.</span><span class="sxs-lookup"><span data-stu-id="17cf0-117">To compare named property identifiers belonging to two objects, clients not using mapping signatures must call [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) on both objects to retrieve the names for each of the identifiers.</span></span> <span data-ttu-id="17cf0-118">Verwenden die Zuordnung Signaturen von Objekten kann dieses Anrufs unnötige rendern.</span><span class="sxs-lookup"><span data-stu-id="17cf0-118">Using the mapping signatures of objects can render this call unnecessary.</span></span> <span data-ttu-id="17cf0-119">Wenn zwei Objekte den gleichen Wert für ihre **PR_MAPPING_SIGNATURE** Eigenschaften aufweisen, verwenden sie die gleiche Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="17cf0-119">When two objects have the same value for their **PR_MAPPING_SIGNATURE** properties, they use the same mapping.</span></span> <span data-ttu-id="17cf0-120">Bezeichner, die die gleiche Zuordnung verwenden können direkt verglichen werden.</span><span class="sxs-lookup"><span data-stu-id="17cf0-120">Identifiers that use the same mapping can be compared directly.</span></span> <span data-ttu-id="17cf0-121">Dienstanbieter, die die Implementierung [IMAPIProp::CopyTo](imapiprop-copyto.md) und [IMAPIProp::CopyProps](imapiprop-copyprops.md) können auch ein Objekt Zuordnung Signatur nutzen.</span><span class="sxs-lookup"><span data-stu-id="17cf0-121">Service providers that implement [IMAPIProp::CopyTo](imapiprop-copyto.md) and [IMAPIProp::CopyProps](imapiprop-copyprops.md) can also take advantage of an object's mapping signature.</span></span> <span data-ttu-id="17cf0-122">Beim Kopieren zwischen Objekten Eigenschaften namens können Dienstanbieter den Konvertierungsschritt vermeiden, wenn die Quell- und Ziel-Objekte dieselbe Zuordnung Signatur aufweisen.</span><span class="sxs-lookup"><span data-stu-id="17cf0-122">When copying named properties between objects, service providers can avoid the conversion step when the source and destination objects have the same mapping signature.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="17cf0-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="17cf0-123">See also</span></span>



[<span data-ttu-id="17cf0-124">IMAPIProp: IUnknown</span><span class="sxs-lookup"><span data-stu-id="17cf0-124">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="17cf0-125">Benannte Eigenschaften MAPI</span><span class="sxs-lookup"><span data-stu-id="17cf0-125">MAPI Named Properties</span></span>](mapi-named-properties.md)
