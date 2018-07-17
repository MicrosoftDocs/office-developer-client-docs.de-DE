---
title: IABContainer IMAPIContainer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABContainer
api_type:
- COM
ms.assetid: 1f5ce6e0-b79a-4da2-b014-8c00cd72912e
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 0eb6d62b64595474957415e94275d0ac52cc2b6b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791954"
---
# <a name="iabcontainer--imapicontainer"></a><span data-ttu-id="40f63-103">IABContainer: IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="40f63-103">IABContainer : IMAPIContainer</span></span>

<span data-ttu-id="40f63-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="40f63-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="40f63-105">Bietet Zugriff auf Address Book Container.</span><span class="sxs-lookup"><span data-stu-id="40f63-105">Provides access to address book containers.</span></span> <span data-ttu-id="40f63-106">MAPI-und Clientanwendungen rufen Sie die Methoden des **IABContainer** namensauflösung ausführen, und kopieren Sie Sie zum Erstellen und Löschen von Empfängern.</span><span class="sxs-lookup"><span data-stu-id="40f63-106">MAPI and client applications call the methods of **IABContainer** to perform name resolution and to create, copy, and delete recipients.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="40f63-107">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="40f63-107">Header file:</span></span>  <br/> |<span data-ttu-id="40f63-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="40f63-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="40f63-109">Verf�gbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="40f63-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="40f63-110">Address Book Container-Objekte</span><span class="sxs-lookup"><span data-stu-id="40f63-110">Address book container objects</span></span>  <br/> |
|<span data-ttu-id="40f63-111">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="40f63-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="40f63-112">Von adressbuchanbietern implementierte</span><span class="sxs-lookup"><span data-stu-id="40f63-112">Address book providers</span></span>  <br/> |
|<span data-ttu-id="40f63-113">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="40f63-113">Called by:</span></span>  <br/> |<span data-ttu-id="40f63-114">MAPI-und Clientanwendungen</span><span class="sxs-lookup"><span data-stu-id="40f63-114">MAPI and client applications</span></span>  <br/> |
|<span data-ttu-id="40f63-115">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="40f63-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="40f63-116">IID_IABContainer</span><span class="sxs-lookup"><span data-stu-id="40f63-116">IID_IABContainer</span></span>  <br/> |
|<span data-ttu-id="40f63-117">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="40f63-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="40f63-118">LPABCONT</span><span class="sxs-lookup"><span data-stu-id="40f63-118">LPABCONT</span></span>  <br/> |
|<span data-ttu-id="40f63-119">Transaktionsmodell:</span><span class="sxs-lookup"><span data-stu-id="40f63-119">Transaction model:</span></span>  <br/> |<span data-ttu-id="40f63-120">Durchgeführt</span><span class="sxs-lookup"><span data-stu-id="40f63-120">Transacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="40f63-121">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="40f63-121">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="40f63-122">CreateEntry</span><span class="sxs-lookup"><span data-stu-id="40f63-122">CreateEntry</span></span>](iabcontainer-createentry.md) <br/> |<span data-ttu-id="40f63-123">Erstellt einen neuen Eintrag, der ein messaging-Benutzer, eine Verteilerliste oder einen anderen Container sein kann.</span><span class="sxs-lookup"><span data-stu-id="40f63-123">Creates a new entry, which can be a messaging user, a distribution list, or another container.</span></span>  <br/> |
|[<span data-ttu-id="40f63-124">CopyEntries</span><span class="sxs-lookup"><span data-stu-id="40f63-124">CopyEntries</span></span>](iabcontainer-copyentries.md) <br/> |<span data-ttu-id="40f63-125">Kopiert eine oder mehrere Einträge, in der Regel messaging Benutzer oder Verteilerlisten.</span><span class="sxs-lookup"><span data-stu-id="40f63-125">Copies one or more entries, typically messaging users or distribution lists.</span></span>  <br/> |
|[<span data-ttu-id="40f63-126">DeleteEntries</span><span class="sxs-lookup"><span data-stu-id="40f63-126">DeleteEntries</span></span>](iabcontainer-deleteentries.md) <br/> |<span data-ttu-id="40f63-127">Entfernt einen oder mehrere Einträge in der Regel messaging Benutzern, Verteilerlisten oder andere Container.</span><span class="sxs-lookup"><span data-stu-id="40f63-127">Removes one or more entries, typically messaging users, distribution lists, or other containers.</span></span>  <br/> |
|[<span data-ttu-id="40f63-128">ResolveNames</span><span class="sxs-lookup"><span data-stu-id="40f63-128">ResolveNames</span></span>](iabcontainer-resolvenames.md) <br/> |<span data-ttu-id="40f63-129">Führt die Auflösung für einen oder mehrere Empfänger Einträge.</span><span class="sxs-lookup"><span data-stu-id="40f63-129">Performs name resolution for one or more recipient entries.</span></span>  <br/> |
   
|<span data-ttu-id="40f63-130">**Erforderliche Eigenschaften**</span><span class="sxs-lookup"><span data-stu-id="40f63-130">**Required properties**</span></span>|<span data-ttu-id="40f63-131">**Zugriff**</span><span class="sxs-lookup"><span data-stu-id="40f63-131">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="40f63-132">**PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="40f63-132">**PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="40f63-133">Lese-/Schreibzugriff</span><span class="sxs-lookup"><span data-stu-id="40f63-133">Read/write</span></span>  <br/> |
|<span data-ttu-id="40f63-134">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="40f63-134">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="40f63-135">Lese-/Schreibzugriff</span><span class="sxs-lookup"><span data-stu-id="40f63-135">Read/write</span></span>  <br/> |
|<span data-ttu-id="40f63-136">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="40f63-136">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="40f63-137">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="40f63-137">Read-only</span></span>  <br/> |
|<span data-ttu-id="40f63-138">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="40f63-138">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="40f63-139">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="40f63-139">Read-only</span></span>  <br/> |
|<span data-ttu-id="40f63-140">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="40f63-140">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="40f63-141">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="40f63-141">Read-only</span></span>  <br/> |
   
|<span data-ttu-id="40f63-142">**Optionale Eigenschaften**</span><span class="sxs-lookup"><span data-stu-id="40f63-142">**Optional properties**</span></span>|<span data-ttu-id="40f63-143">**Zugriff**</span><span class="sxs-lookup"><span data-stu-id="40f63-143">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="40f63-144">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="40f63-144">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="40f63-145">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="40f63-145">Read-only</span></span>  <br/> |
|<span data-ttu-id="40f63-146">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="40f63-146">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="40f63-147">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="40f63-147">Read-only</span></span>  <br/> |
|<span data-ttu-id="40f63-148">**PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="40f63-148">**PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="40f63-149">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="40f63-149">Read-only</span></span>  <br/> |
|<span data-ttu-id="40f63-150">**PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="40f63-150">**PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="40f63-151">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="40f63-151">Read-only</span></span>  <br/> |
|<span data-ttu-id="40f63-152">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="40f63-152">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="40f63-153">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="40f63-153">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="40f63-154">Hinweise</span><span class="sxs-lookup"><span data-stu-id="40f63-154">Remarks</span></span>

<span data-ttu-id="40f63-155">Die **IABContainer** -Schnittstelle erbt indirekt von [IUnknown](http://msdn.microsoft.com/de-de/library/ms680509%28VS.85%29.aspx) -Schnittstelle, über die [IMAPIContainer: IMAPIProp](imapicontainerimapiprop.md) und [IMAPIProp: IUnknown](imapipropiunknown.md) Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="40f63-155">The **IABContainer** interface inherits indirectly from the [IUnknown](http://msdn.microsoft.com/de-de/library/ms680509%28VS.85%29.aspx) interface through the [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md) and [IMAPIProp : IUnknown](imapipropiunknown.md) interfaces.</span></span> <span data-ttu-id="40f63-156">Von adressbuchanbietern implementierte implementieren die **IABContainer** -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="40f63-156">Address book providers implement the **IABContainer** interface.</span></span> 
  
<span data-ttu-id="40f63-157">Eine beliebige Anzahl von messaging User-Objekte, Verteilerlisten und andere Address Book-Container kann in einer Adressbuchcontainer vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="40f63-157">Any number of messaging user objects, distribution lists, and other address book containers can exist in an address book container.</span></span> <span data-ttu-id="40f63-158">Wie bei einem beliebigen Container können Clients oder Dienstanbieter ein Adressbuchcontainer öffnen Sie eine der zugehörigen Einträge oder einer Hierarchietabelle oder Inhaltstabelle abrufen.</span><span class="sxs-lookup"><span data-stu-id="40f63-158">As with any container, clients or service providers can use an address book container to open one of its entries or to retrieve a hierarchy table or contents table.</span></span> <span data-ttu-id="40f63-159">Adressbuch Container auch eine namensauflösung und, abhängig von des Anbieters die Möglichkeit zum Hinzufügen, entfernen oder Ändern von Einträgen.</span><span class="sxs-lookup"><span data-stu-id="40f63-159">Address book containers also provide name resolution and, depending on the provider, the ability to add, remove, or modify entries.</span></span>
  
<span data-ttu-id="40f63-160">MAPI definiert eine spezielle Adressbuchcontainer bezeichnet das persönliche Adressbuch (PAB), das von anderen Containern kopierten Einträge enthält.</span><span class="sxs-lookup"><span data-stu-id="40f63-160">MAPI defines a special address book container called the personal address book (PAB) that holds entries copied from other containers.</span></span> <span data-ttu-id="40f63-161">Ein PAB kann jederzeit geändert werden.</span><span class="sxs-lookup"><span data-stu-id="40f63-161">A PAB is always modifiable.</span></span> <span data-ttu-id="40f63-162">Benutzer füllen ihre PAB in der Regel mit Einträgen Festlegen der Empfänger an, mit denen sie am häufigsten kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="40f63-162">Users typically populate their PAB with entries designating the recipients with which they most frequently communicate.</span></span> <span data-ttu-id="40f63-163">Ein PAB kann auch einmal-Adressen und neue Empfänger noch nicht Teil der alle Adressbuchcontainer halten.</span><span class="sxs-lookup"><span data-stu-id="40f63-163">A PAB can also hold one-off addresses and new recipients not yet a part of any address book container.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="40f63-164">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="40f63-164">See also</span></span>

- [<span data-ttu-id="40f63-165">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="40f63-165">MAPI Interfaces</span></span>](mapi-interfaces.md)
