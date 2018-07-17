---
title: Arten von Einschränkungen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0d3bd58b-7100-4117-91ac-27139715c85b
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 7e3459c639cac449cdc03361949c9618827515b9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795764"
---
# <a name="types-of-restrictions"></a><span data-ttu-id="780b0-103">Arten von Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="780b0-103">Types of Restrictions</span></span>

  
  
<span data-ttu-id="780b0-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="780b0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="780b0-105">Es gibt viele Arten von Einschränkungen, einige, den Fokus auf bestimmte Spalten.</span><span class="sxs-lookup"><span data-stu-id="780b0-105">There are many types of restrictions, some that focus on specific columns.</span></span> <span data-ttu-id="780b0-106">Alle Tabelle Implementierungen sind zur Unterstützung von Einschränkungen für die Spalten in der aktuellen Spalte Gruppe erwartet.</span><span class="sxs-lookup"><span data-stu-id="780b0-106">All table implementations are expected to support restrictions on the columns in the current column set.</span></span> <span data-ttu-id="780b0-107">Jedoch können Wert Tabelle Implementierer auch unterstützen Einschränkungen basierend auf Objekteigenschaften, die derzeit nicht in der Tabellenansicht sind.</span><span class="sxs-lookup"><span data-stu-id="780b0-107">However, to add value, table implementers can also support restrictions based on object properties that are not currently in the table view.</span></span>
  
<span data-ttu-id="780b0-108">Einige Einschränkungen können mit einer Einschränkung, die eine logische **und**, **oder**oder **nicht** ausführt kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="780b0-108">Some restrictions can be combined using a restriction that performs a logical **AND**, **OR**, or **NOT** operation.</span></span> <span data-ttu-id="780b0-109">Beispielsweise die meisten-Eigenschaft, die mit Einschränkungen verknüpft werden müssen **und** Einschränkungen von Einschränkungen vorhanden.</span><span class="sxs-lookup"><span data-stu-id="780b0-109">For example, most property restrictions must be joined with exist restrictions using **AND** restrictions.</span></span> <span data-ttu-id="780b0-110">Es gibt einige Ausnahmen, z. B., wenn die Eigenschaft in der eigenschaftseinschränkung, die **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md))-Eigenschaft ist oder wenn es sich um eine erforderliche Spalte in einer Tabelle ist.</span><span class="sxs-lookup"><span data-stu-id="780b0-110">There are a few exceptions, such as when the property used in the property restriction is the **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) property or when it is a required column in a table.</span></span> <span data-ttu-id="780b0-111">Ein Client erstellen Einschränkungen zur Begrenzung der Ansicht verwenden sollte Einschränkungen mit den Suchkriterien in Eigenschaft vorhanden sein, da MAPI nicht festlegt, wie Dienstanbieter Suchkriterien in Eigenschaft ausgewertet werden soll, wenn eine Eigenschaft nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="780b0-111">A client building restrictions to limit its view should use exist restrictions with its property restrictions because MAPI does not specify how service providers should evaluate property restrictions when a property does not exist.</span></span> <span data-ttu-id="780b0-112">Es ist angemessen und empfohlen, Dienstanbieter die Einschränkung Fehler, aber es keine Anforderungen sind.</span><span class="sxs-lookup"><span data-stu-id="780b0-112">It is reasonable and recommended that service providers fail the restriction, but there are no requirements.</span></span> 
  
<span data-ttu-id="780b0-113">Eine Einschränkung wird mithilfe der [SRestriction](srestriction.md) -Datenstruktur, die eine Vereinigung von speziellere Einschränkung Strukturen und ein Indikator vom Typ der Union-Struktur enthält definiert.</span><span class="sxs-lookup"><span data-stu-id="780b0-113">A restriction is defined using the [SRestriction](srestriction.md) data structure which contains a union of more specialized restriction structures and an indicator of the type of structure included in the union.</span></span> 
  
<span data-ttu-id="780b0-114">Jede Struktur spezialisierte Einschränkung in der Union stellt eine andere Art von Einschränkung.</span><span class="sxs-lookup"><span data-stu-id="780b0-114">Each of the specialized restriction structures in the union represents a different type of restriction.</span></span> <span data-ttu-id="780b0-115">Die Arten von Einschränkungen und ihre zugehörigen Datenstrukturen sind:</span><span class="sxs-lookup"><span data-stu-id="780b0-115">The types of restrictions and their associated data structures are:</span></span>
  
|<span data-ttu-id="780b0-116">**Typ der Einschränkung**</span><span class="sxs-lookup"><span data-stu-id="780b0-116">**Type of restriction**</span></span>|<span data-ttu-id="780b0-117">**Struktur der zugehörigen Daten**</span><span class="sxs-lookup"><span data-stu-id="780b0-117">**Associated data structure**</span></span>|<span data-ttu-id="780b0-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="780b0-118">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="780b0-119">Vergleichen-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="780b0-119">Compare property</span></span>  <br/> |[<span data-ttu-id="780b0-120">SComparePropsRestriction</span><span class="sxs-lookup"><span data-stu-id="780b0-120">SComparePropsRestriction</span></span>](scomparepropsrestriction.md) <br/> |<span data-ttu-id="780b0-121">Vergleicht zwei Eigenschaften des gleichen Typs.</span><span class="sxs-lookup"><span data-stu-id="780b0-121">Compares two properties of the same type.</span></span>  <br/> |
|<span data-ttu-id="780b0-122">**AND**</span><span class="sxs-lookup"><span data-stu-id="780b0-122">**AND**</span></span> <br/> |[<span data-ttu-id="780b0-123">SAndRestriction</span><span class="sxs-lookup"><span data-stu-id="780b0-123">SAndRestriction</span></span>](sandrestriction.md) <br/> |<span data-ttu-id="780b0-124">Führt eine logische **AND** -Operation mit zwei oder mehr Einschränkungen.</span><span class="sxs-lookup"><span data-stu-id="780b0-124">Performs a logical **AND** operation on two or more restrictions.</span></span>  <br/> |
|<span data-ttu-id="780b0-125">**ODER**</span><span class="sxs-lookup"><span data-stu-id="780b0-125">**OR**</span></span> <br/> |[<span data-ttu-id="780b0-126">SOrRestriction</span><span class="sxs-lookup"><span data-stu-id="780b0-126">SOrRestriction</span></span>](sorrestriction.md) <br/> |<span data-ttu-id="780b0-127">Führt eine logische **OR** -Operation für zwei oder mehr Einschränkungen.</span><span class="sxs-lookup"><span data-stu-id="780b0-127">Performs a logical **OR** operation on two or more restrictions.</span></span>  <br/> |
|<span data-ttu-id="780b0-128">**NOT**</span><span class="sxs-lookup"><span data-stu-id="780b0-128">**NOT**</span></span> <br/> |[<span data-ttu-id="780b0-129">SNotRestriction</span><span class="sxs-lookup"><span data-stu-id="780b0-129">SNotRestriction</span></span>](snotrestriction.md) <br/> |<span data-ttu-id="780b0-130">Führt eine logische **NOT** -Operation für zwei oder mehr Einschränkungen.</span><span class="sxs-lookup"><span data-stu-id="780b0-130">Performs a logical **NOT** operation on two or more restrictions.</span></span>  <br/> |
|<span data-ttu-id="780b0-131">Inhalt</span><span class="sxs-lookup"><span data-stu-id="780b0-131">Content</span></span>  <br/> |[<span data-ttu-id="780b0-132">SContentRestriction</span><span class="sxs-lookup"><span data-stu-id="780b0-132">SContentRestriction</span></span>](scontentrestriction.md) <br/> |<span data-ttu-id="780b0-133">Sucht angegebene Daten.</span><span class="sxs-lookup"><span data-stu-id="780b0-133">Locates specified data.</span></span>  <br/> |
|<span data-ttu-id="780b0-134">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="780b0-134">Property</span></span>  <br/> |[<span data-ttu-id="780b0-135">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="780b0-135">SPropertyRestriction</span></span>](spropertyrestriction.md) <br/> |<span data-ttu-id="780b0-136">Gibt den Wert einer bestimmten Eigenschaft als Kriterium für den Abgleich.</span><span class="sxs-lookup"><span data-stu-id="780b0-136">Specifies a particular property value as criteria for matching.</span></span> <span data-ttu-id="780b0-137">Kann beispielsweise verwendet werden für einen bestimmten Typ Anlage suchen.</span><span class="sxs-lookup"><span data-stu-id="780b0-137">Can be used, for example, to search for a particular type of attachment.</span></span>  <br/> |
|<span data-ttu-id="780b0-138">Bitmaske</span><span class="sxs-lookup"><span data-stu-id="780b0-138">Bitmask</span></span>  <br/> |[<span data-ttu-id="780b0-139">SBitMaskRestriction</span><span class="sxs-lookup"><span data-stu-id="780b0-139">SBitMaskRestriction</span></span>](sbitmaskrestriction.md) <br/> |<span data-ttu-id="780b0-140">Eine Bitmaske gilt in der Regel zu einer Eigenschaft PT_LONG, um festzustellen, ob bestimmte Flags festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="780b0-140">Applies a bitmask to a PT_LONG property, typically to determine whether particular flags are set.</span></span>  <br/> |
|<span data-ttu-id="780b0-141">Größe</span><span class="sxs-lookup"><span data-stu-id="780b0-141">Size</span></span>  <br/> |[<span data-ttu-id="780b0-142">SSizeRestriction</span><span class="sxs-lookup"><span data-stu-id="780b0-142">SSizeRestriction</span></span>](ssizerestriction.md) <br/> |<span data-ttu-id="780b0-143">Die Größe einer Eigenschaft über die standardmäßigen relationale Operatoren getestet.</span><span class="sxs-lookup"><span data-stu-id="780b0-143">Tests the size of a property using standard relational operators.</span></span>  <br/> |
|<span data-ttu-id="780b0-144">Vorhanden</span><span class="sxs-lookup"><span data-stu-id="780b0-144">Exist</span></span>  <br/> |[<span data-ttu-id="780b0-145">SExistRestriction</span><span class="sxs-lookup"><span data-stu-id="780b0-145">SExistRestriction</span></span>](sexistrestriction.md) <br/> |<span data-ttu-id="780b0-146">Überprüft, ob ein Objekt einen Wert für eine Eigenschaft verfügt.</span><span class="sxs-lookup"><span data-stu-id="780b0-146">Tests whether an object has a value for a property.</span></span>  <br/> |
|<span data-ttu-id="780b0-147">Unterobjekt</span><span class="sxs-lookup"><span data-stu-id="780b0-147">Subobject</span></span>  <br/> |[<span data-ttu-id="780b0-148">SSubRestriction</span><span class="sxs-lookup"><span data-stu-id="780b0-148">SSubRestriction</span></span>](ssubrestriction.md) <br/> |<span data-ttu-id="780b0-149">Verwendet für die Suche über Unterobjekte oder -Objekten, die mit einem Eintrag Bezeichner, wie Empfänger und Anlagen nicht zugegriffen werden können.</span><span class="sxs-lookup"><span data-stu-id="780b0-149">Used for searching through subobjects, or objects that cannot be accessed with an entry identifier, such as recipients and attachments.</span></span> <span data-ttu-id="780b0-150">Kann beispielsweise verwendet werden nach einem bestimmten Empfänger nach Nachrichten gesucht.</span><span class="sxs-lookup"><span data-stu-id="780b0-150">Can be used, for example, to look for messages for a particular recipient.</span></span>  <br/> |
|<span data-ttu-id="780b0-151">Comment</span><span class="sxs-lookup"><span data-stu-id="780b0-151">Comment</span></span>  <br/> |[<span data-ttu-id="780b0-152">SCommentRestriction</span><span class="sxs-lookup"><span data-stu-id="780b0-152">SCommentRestriction</span></span>](scommentrestriction.md) <br/> |<span data-ttu-id="780b0-153">Ordnet eine Reihe von benannten Eigenschaften ein Objekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="780b0-153">Associates an object with a set of named properties.</span></span>  <br/> |
   
<span data-ttu-id="780b0-154">Einige Einschränkungen mithilfe von regulären Ausdrücken und MAPI unterstützt eingeschränkte des regulären Ausdrucks Notation im Format, die viele Text Clientanwendungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="780b0-154">Some restrictions use regular expressions, and MAPI supports a limited form of regular expression notation in the style that is used many text applications.</span></span>
  
<span data-ttu-id="780b0-155">Die Einschränkung der Kommentar wird von Clients verwendet, die auf dem Datenträger beibehalten anwendungsspezifische Informationen mit der Einschränkung Einschränkungen speichern.</span><span class="sxs-lookup"><span data-stu-id="780b0-155">The comment restriction is used by clients that save restrictions on disk to keep application-specific information with the restriction.</span></span> <span data-ttu-id="780b0-156">Beispielsweise kann ein Client, speichern den Namen einer benannten Eigenschaft verwendet, in einer eigenschaftseinschränkung mit einer Einschränkung Kommentar tun.</span><span class="sxs-lookup"><span data-stu-id="780b0-156">For example, a client saving the name of a named property used in a property restriction can do so with a comment restriction.</span></span> <span data-ttu-id="780b0-157">Speichern den Namen ist nicht möglich in eine eigenschaftseinschränkung; die [SPropertyRestriction](spropertyrestriction.md) -Datenstruktur enthält das Eigenschafts-Tag.</span><span class="sxs-lookup"><span data-stu-id="780b0-157">Saving the name is not possible in a property restriction; the [SPropertyRestriction](spropertyrestriction.md) data structure holds only the property tag.</span></span> <span data-ttu-id="780b0-158">Kommentar Einschränkungen werden durch die [Methode IMAPITable:: Restrict](imapitable-restrict.md) ignoriert, sie haben keinen Einfluss auf die Zeilen von [IMAPITable::QueryRows](imapitable-queryrows.md) zurückgegeben wird, nachdem ein Anruf **Restrict** vorgenommen wurde.</span><span class="sxs-lookup"><span data-stu-id="780b0-158">Comment restrictions are ignored by [IMAPITable::Restrict](imapitable-restrict.md) in that they have no effect on the rows returned by [IMAPITable::QueryRows](imapitable-queryrows.md) after a **Restrict** call has been made.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="780b0-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="780b0-159">See also</span></span>



[<span data-ttu-id="780b0-160">MAPI-Tabellen</span><span class="sxs-lookup"><span data-stu-id="780b0-160">MAPI Tables</span></span>](mapi-tables.md)
