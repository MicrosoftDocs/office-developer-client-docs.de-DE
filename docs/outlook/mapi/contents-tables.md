---
title: Inhalt von Tabellen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7b8efb4e-b5be-41b8-81bb-9aa1da421433
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 0dd79d9630837b5ec8a709d386ccc0db987dfb5b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791435"
---
# <a name="contents-tables"></a><span data-ttu-id="83b6c-103">Inhalt von Tabellen</span><span class="sxs-lookup"><span data-stu-id="83b6c-103">Contents Tables</span></span>

  
  
<span data-ttu-id="83b6c-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="83b6c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="83b6c-105">Eine Inhaltstabelle enthält Informationen zu Objekten in einem MAPI-Container.</span><span class="sxs-lookup"><span data-stu-id="83b6c-105">A contents table contains information about objects in a MAPI container.</span></span> <span data-ttu-id="83b6c-106">Von adressbuchanbietern implementierte implementieren Sie Inhalt Tabellen für jeden ihrer Container und Nachrichtenspeicher und remote-Transport-Anbieter Inhalt Tabellen für ihre Ordner.</span><span class="sxs-lookup"><span data-stu-id="83b6c-106">Address book providers implement contents tables for each of their containers, and message store and remote transport providers implement contents tables for their folders.</span></span> <span data-ttu-id="83b6c-107">Die Inhaltstabelle ein Adressbuchcontainer enthält Informationen zu den messaging Listenobjekten Benutzer- und Verteilung, während der Inhalt eines Ordners Informationen zu eigenen Nachrichten in der Tabelle ist.</span><span class="sxs-lookup"><span data-stu-id="83b6c-107">The contents table of an address book container lists information about its messaging user and distribution list objects, while the contents table of a folder lists information about its messages.</span></span> <span data-ttu-id="83b6c-108">Inhalt Tabellen werden hauptsächlich von Clientanwendungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="83b6c-108">Contents tables are used primarily by client applications.</span></span> 
  
<span data-ttu-id="83b6c-109">Es gibt zwei Arten von Ordner Inhalt Tabellen:</span><span class="sxs-lookup"><span data-stu-id="83b6c-109">There are two types of folder contents tables:</span></span>
  
- <span data-ttu-id="83b6c-110">Standard-Inhalt Tabellen enthalten standard Nachrichten – Nachrichten, die übertragen und für einen Benutzer sichtbar gemacht werden können.</span><span class="sxs-lookup"><span data-stu-id="83b6c-110">Standard contents tables contain standard messages — messages that can be transmitted and made visible to a user.</span></span> 
    
- <span data-ttu-id="83b6c-111">Zugehörige Inhalt Tabellen enthalten ausgeblendet, Übertragungseinehit Informationen, die von einem Client wie, eine Alternative Darstellung einer standard-Nachricht speichern für einen bestimmten Zweck, erstellt.</span><span class="sxs-lookup"><span data-stu-id="83b6c-111">Associated contents tables contain hidden, non-transmittable information created by a client for a specific purpose, such as to store an alternate representation of a standard message.</span></span> <span data-ttu-id="83b6c-112">Zugehörige Informationen wird erstellt, indem Sie das MAPI_ASSOCIATED-Flag für den Aufruf der [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) übergeben.</span><span class="sxs-lookup"><span data-stu-id="83b6c-112">Associated information is created by passing the MAPI_ASSOCIATED flag to the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) call.</span></span> 
    
<span data-ttu-id="83b6c-113">Die Inhalte, die keine für Tabellen mit den meisten Address Book Containern und viele Ordner Unterstützung kategorisiert sortieren.</span><span class="sxs-lookup"><span data-stu-id="83b6c-113">The contents tables of most address book containers and many folders do not support categorized sorting.</span></span> 
  
<span data-ttu-id="83b6c-114">Eine Inhaltstabelle kann durch Aufrufen von zugegriffen werden:</span><span class="sxs-lookup"><span data-stu-id="83b6c-114">A contents table can be accessed by calling:</span></span>
  
- <span data-ttu-id="83b6c-115">[IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md).</span><span class="sxs-lookup"><span data-stu-id="83b6c-115">[IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md).</span></span>
    
    - <span data-ttu-id="83b6c-116">Oder -</span><span class="sxs-lookup"><span data-stu-id="83b6c-116">Or -</span></span>
    
- <span data-ttu-id="83b6c-117">[IMAPIProp::OpenProperty](imapiprop-openproperty.md) mit **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) oder **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) (nur Ordner) als Eigenschafts-Tag und IID angegeben _IMAPITable als Schnittstellenbezeichner.</span><span class="sxs-lookup"><span data-stu-id="83b6c-117">[IMAPIProp::OpenProperty](imapiprop-openproperty.md) with **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) or **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) (folders only) specified as the property tag and IID_IMAPITable as the interface identifier.</span></span>
    
<span data-ttu-id="83b6c-118">Nachrichtenspeicher und Address Book Anbieter müssen beide Verfahren zum Abrufen von Eigenschaften der Tabelle unterstützen.</span><span class="sxs-lookup"><span data-stu-id="83b6c-118">Message store and address book providers must support both techniques for retrieving table properties.</span></span> <span data-ttu-id="83b6c-119">Es ist nicht zulässig für Anbieter unterstützt nur eine Möglichkeit für den Zugriff auf diese Tabellen, da Clients erwarten, dass die Option haben.</span><span class="sxs-lookup"><span data-stu-id="83b6c-119">It is unacceptable for providers to support only one way for accessing these tables because clients expect to have the choice.</span></span> 
  
 <span data-ttu-id="83b6c-120">**GetContentsTable** , die als Eingabe akzeptiert mehrere Flags, die Voreinstellungen angeben.</span><span class="sxs-lookup"><span data-stu-id="83b6c-120">**GetContentsTable** accepts as input several flags that specify preferences.</span></span> <span data-ttu-id="83b6c-121">Das Flag MAPI_ASSOCIATED bei Festlegung einer zugeordneten Inhaltstabelle abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="83b6c-121">When set, the MAPI_ASSOCIATED flag retrieves an associated contents table.</span></span> <span data-ttu-id="83b6c-122">Da einige Ordner zugeordneten Inhalt nicht unterstützt, und es keine Möglichkeit für Clients gibt, die diese vorausschauendes Bestimmung, gibt **GetContentsTable** manchmal den Fehler MAPI_E_NO_SUPPORT zurück, wenn einer zugeordneten Inhaltstabelle angefordert wird.</span><span class="sxs-lookup"><span data-stu-id="83b6c-122">Because some folders do not support associated contents, and there is no way for clients to determine this ahead of time, **GetContentsTable** sometimes returns the error MAPI_E_NO_SUPPORT when an associated contents table is requested.</span></span> 
  
<span data-ttu-id="83b6c-123">Das Flag MAPI_DEFERRED_ERRORS gibt an, das die Implementierung von der Tabelle, die während des Anrufs aufgetretenen nicht bis zu einem späteren Zeitpunkt gemeldet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="83b6c-123">The MAPI_DEFERRED_ERRORS flag indicates to the implementer of the table that any errors encountered during the call do not need to be reported until some later time.</span></span> 
  
<span data-ttu-id="83b6c-124">Der Aufruf von **IMAPIProp::OpenProperty** umfasst den Zugriff auf eine Inhaltstabelle durch Öffnen der entsprechenden Eigenschaft **PR_CONTAINER_CONTENTS** für Address Book Inhalt Tabellen und Standardordner Inhalt Tabellen und **PR_FOLDER_ASSOCIATED_ Inhalt** für verknüpfte Tabellen Inhalt.</span><span class="sxs-lookup"><span data-stu-id="83b6c-124">The call to **IMAPIProp::OpenProperty** involves accessing a contents table by opening its corresponding property, **PR_CONTAINER_CONTENTS** for address book contents tables and standard folder contents tables, and **PR_FOLDER_ASSOCIATED_CONTENTS** for associated contents tables.</span></span> <span data-ttu-id="83b6c-125">Jedoch weder oder diese Eigenschaften können über einen Ordner oder für den Container [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode abgerufen werden, sie sind in der von der [IMAPIProp::GetPropList](imapiprop-getproplist.md) -Methode zurückgegebene Array Eigenschaft Tag enthalten.</span><span class="sxs-lookup"><span data-stu-id="83b6c-125">Although neither or these properties can be retrieved through a folder or container's [IMAPIProp::GetProps](imapiprop-getprops.md) method, they are included in the property tag array that is returned by the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method.</span></span> 
  
 <span data-ttu-id="83b6c-126">**PR_CONTAINER_CONTENTS** kann auch ein-oder Ausschließen einer Inhaltstabelle aus einem Kopiervorgang verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="83b6c-126">**PR_CONTAINER_CONTENTS** can also be used to include or exclude a contents table from a copy operation.</span></span> <span data-ttu-id="83b6c-127">Wenn ein Client **PR_CONTAINER_CONTENTS** im *LpExcludeProps* -Parameter für **IMAPIProp::CopyTo** in einen Kopiervorgang angibt, wird der neuen Ordner oder im Container nicht der Inhaltstabelle des ursprünglichen Ordner oder des Containers unterstützt.</span><span class="sxs-lookup"><span data-stu-id="83b6c-127">If a client specifies **PR_CONTAINER_CONTENTS** in the  *lpExcludeProps*  parameter for **IMAPIProp::CopyTo** in a copy operation, the new folder or container will not support the contents table of the original folder or container.</span></span> 
  
<span data-ttu-id="83b6c-128">Address Book Container und Ordner Inhalt Tabellen haben eine lange Liste von erforderlichen Spalten – Spalten, die Clients zur Verfügung, nachdem sie die Tabelle aus **GetContentsTable** oder **OpenProperty**abrufen erwarten können.</span><span class="sxs-lookup"><span data-stu-id="83b6c-128">Address book container and folder contents tables have a lengthy list of required columns — columns that clients can expect to be available after they retrieve the table from **GetContentsTable** or **OpenProperty**.</span></span> <span data-ttu-id="83b6c-129">Anbieter können auf diesen Satz von erforderlichen hinzufügen, wenn Bedarf und Clients, mit der **SetColumns** -Methode auch Änderungen angefordert werden können.</span><span class="sxs-lookup"><span data-stu-id="83b6c-129">Providers can add to this required set if necessary and clients, through the **SetColumns** method, can also request modifications.</span></span> 
  
<span data-ttu-id="83b6c-130">Die erforderlichen Spalten für die einzelnen Arten von Inhalt Tabellen sind:</span><span class="sxs-lookup"><span data-stu-id="83b6c-130">The required columns for each of the types of contents tables are:</span></span>
  
|<span data-ttu-id="83b6c-131">**Erforderliche Spalte**</span><span class="sxs-lookup"><span data-stu-id="83b6c-131">**Required column**</span></span>|<span data-ttu-id="83b6c-132">**Typ der Inhaltstabelle**</span><span class="sxs-lookup"><span data-stu-id="83b6c-132">**Type of contents table**</span></span>|
|:-----|:-----|
|<span data-ttu-id="83b6c-133">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="83b6c-133">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="83b6c-134">Address Book Container Tabellen</span><span class="sxs-lookup"><span data-stu-id="83b6c-134">Address book container tables</span></span>  <br/> |
|<span data-ttu-id="83b6c-135">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="83b6c-135">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="83b6c-136">Address Book Container Tabellen</span><span class="sxs-lookup"><span data-stu-id="83b6c-136">Address book container tables</span></span>  <br/> |
|<span data-ttu-id="83b6c-137">**PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="83b6c-137">**PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="83b6c-138">Nachricht Store Ordner Tabellen</span><span class="sxs-lookup"><span data-stu-id="83b6c-138">Message store folder tables</span></span>  <br/> |
|<span data-ttu-id="83b6c-139">**PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="83b6c-139">**PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="83b6c-140">Alle Ordner Inhalt Tabellen</span><span class="sxs-lookup"><span data-stu-id="83b6c-140">All folder contents tables</span></span>  <br/> |
|<span data-ttu-id="83b6c-141">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="83b6c-141">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="83b6c-142">Address Book Container Tabellen</span><span class="sxs-lookup"><span data-stu-id="83b6c-142">Address book container tables</span></span>  <br/> |
|<span data-ttu-id="83b6c-143">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="83b6c-143">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="83b6c-144">Alle Inhalte Tabellen</span><span class="sxs-lookup"><span data-stu-id="83b6c-144">All contents tables</span></span>  <br/> |
|<span data-ttu-id="83b6c-145">**PR_HASATTACH** ([PidTagHasAttachments](pidtaghasattachments-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="83b6c-145">**PR_HASATTACH** ([PidTagHasAttachments](pidtaghasattachments-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="83b6c-146">Alle Ordner Inhalt Tabellen</span><span class="sxs-lookup"><span data-stu-id="83b6c-146">All folder contents tables</span></span>  <br/> |
|<span data-ttu-id="83b6c-147">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="83b6c-147">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="83b6c-148">Alle Inhalte Tabellen</span><span class="sxs-lookup"><span data-stu-id="83b6c-148">All contents tables</span></span>  <br/> |
|<span data-ttu-id="83b6c-149">**PR_LAST_MODIFICATION_TIME** ([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="83b6c-149">**PR_LAST_MODIFICATION_TIME** ([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="83b6c-150">Nachricht Store Ordner Tabellen</span><span class="sxs-lookup"><span data-stu-id="83b6c-150">Message store folder tables</span></span>  <br/> |
|<span data-ttu-id="83b6c-151">**PR_MAPPING_SIGNATURE** ([PidTagMappingSignature](pidtagmappingsignature-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="83b6c-151">**PR_MAPPING_SIGNATURE** ([PidTagMappingSignature](pidtagmappingsignature-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="83b6c-152">Nachricht Store Ordner Tabellen</span><span class="sxs-lookup"><span data-stu-id="83b6c-152">Message store folder tables</span></span>  <br/> |
|<span data-ttu-id="83b6c-153">**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="83b6c-153">**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="83b6c-154">Alle Ordner Inhalt Tabellen</span><span class="sxs-lookup"><span data-stu-id="83b6c-154">All folder contents tables</span></span>  <br/> |
|<span data-ttu-id="83b6c-155">**PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="83b6c-155">**PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="83b6c-156">Remote-Transport Ordner Tabellen</span><span class="sxs-lookup"><span data-stu-id="83b6c-156">Remote transport folder tables</span></span>  <br/> |
|<span data-ttu-id="83b6c-157">**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="83b6c-157">**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="83b6c-158">Alle Ordner Inhalt Tabellen</span><span class="sxs-lookup"><span data-stu-id="83b6c-158">All folder contents tables</span></span>  <br/> |
|<span data-ttu-id="83b6c-159">**PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="83b6c-159">**PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="83b6c-160">Alle Ordner Inhalt Tabellen</span><span class="sxs-lookup"><span data-stu-id="83b6c-160">All folder contents tables</span></span>  <br/> |
|<span data-ttu-id="83b6c-161">**PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="83b6c-161">**PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="83b6c-162">Alle Ordner Inhalt Tabellen</span><span class="sxs-lookup"><span data-stu-id="83b6c-162">All folder contents tables</span></span>  <br/> |
|<span data-ttu-id="83b6c-163">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="83b6c-163">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="83b6c-164">Alle Inhalte Tabellen</span><span class="sxs-lookup"><span data-stu-id="83b6c-164">All contents tables</span></span>  <br/> |
|<span data-ttu-id="83b6c-165">**PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="83b6c-165">**PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="83b6c-166">Nachricht Store Ordner Tabellen</span><span class="sxs-lookup"><span data-stu-id="83b6c-166">Message store folder tables</span></span>  <br/> |
|<span data-ttu-id="83b6c-167">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="83b6c-167">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="83b6c-168">Speichern von Adressbuchcontainer und Nachricht Ordner Tabellen</span><span class="sxs-lookup"><span data-stu-id="83b6c-168">Address book container and message store folder tables</span></span>  <br/> |
|<span data-ttu-id="83b6c-169">**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="83b6c-169">**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="83b6c-170">Remote-Transport Ordner Tabellen</span><span class="sxs-lookup"><span data-stu-id="83b6c-170">Remote transport folder tables</span></span>  <br/> |
|<span data-ttu-id="83b6c-171">**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="83b6c-171">**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="83b6c-172">Nachricht Store Ordner Tabellen</span><span class="sxs-lookup"><span data-stu-id="83b6c-172">Message store folder tables</span></span>  <br/> |
|<span data-ttu-id="83b6c-173">**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="83b6c-173">**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="83b6c-174">Nachricht Store Ordner Tabellen</span><span class="sxs-lookup"><span data-stu-id="83b6c-174">Message store folder tables</span></span>  <br/> |
   
<span data-ttu-id="83b6c-175">Verfügbar mit jeder Zeile die Eintrags-ID kann entweder eine kurz- oder langfristig Eintrags-ID, je nach der Implementierung der Tabelle sein.</span><span class="sxs-lookup"><span data-stu-id="83b6c-175">The entry identifier available with each row can either be a short- or long-term entry identifier, depending on the table implementation.</span></span> <span data-ttu-id="83b6c-176">Kurzfristige-Eintragsbezeichner werden normalerweise in Situationen verwendet, in dem Leistung von Belang ist.</span><span class="sxs-lookup"><span data-stu-id="83b6c-176">Short-term entry identifiers are typically used in situations where performance is an issue.</span></span> <span data-ttu-id="83b6c-177">Beide Arten von Eintrags-ID kann verwendet werden, auf das entsprechende Objekt zugreifen.</span><span class="sxs-lookup"><span data-stu-id="83b6c-177">Either type of entry identifier can be used to access the corresponding object.</span></span> 
  
<span data-ttu-id="83b6c-178">Inhalt Tabellen haben auch eine Reihe von Spalten, die optional, wird jedoch von Dienstanbietern in ihre Implementierungen häufig enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="83b6c-178">Contents tables also have a set of columns that are optional but commonly included by service providers in their implementations.</span></span> <span data-ttu-id="83b6c-179">Diese optionalen Spalten sind:</span><span class="sxs-lookup"><span data-stu-id="83b6c-179">These optional columns are:</span></span>
  
|<span data-ttu-id="83b6c-180">**Optionale Spalte**</span><span class="sxs-lookup"><span data-stu-id="83b6c-180">**Optional column**</span></span>|<span data-ttu-id="83b6c-181">**Typ der Inhaltstabelle**</span><span class="sxs-lookup"><span data-stu-id="83b6c-181">**Type of contents table**</span></span>|
|:-----|:-----|
|<span data-ttu-id="83b6c-182">**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="83b6c-182">**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="83b6c-183">Nachricht Store Ordner Tabellen</span><span class="sxs-lookup"><span data-stu-id="83b6c-183">Message store folder tables</span></span>  <br/> |
|<span data-ttu-id="83b6c-184">**PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="83b6c-184">**PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="83b6c-185">Standardordner Inhalt Tabellen</span><span class="sxs-lookup"><span data-stu-id="83b6c-185">Standard folder contents tables</span></span>  <br/> |
|<span data-ttu-id="83b6c-186">**PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="83b6c-186">**PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="83b6c-187">Standardordner Inhalt Tabellen</span><span class="sxs-lookup"><span data-stu-id="83b6c-187">Standard folder contents tables</span></span>  <br/> |
|<span data-ttu-id="83b6c-188">**PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="83b6c-188">**PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="83b6c-189">Nachricht Store Ordner Tabellen</span><span class="sxs-lookup"><span data-stu-id="83b6c-189">Message store folder tables</span></span>  <br/> |
|<span data-ttu-id="83b6c-190">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="83b6c-190">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="83b6c-191">Address Book Container Tabellen</span><span class="sxs-lookup"><span data-stu-id="83b6c-191">Address book container tables</span></span>  <br/> |
|<span data-ttu-id="83b6c-192">**PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="83b6c-192">**PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="83b6c-193">Alle Ordner Inhalt Tabellen</span><span class="sxs-lookup"><span data-stu-id="83b6c-193">All folder contents tables</span></span>  <br/> |
|<span data-ttu-id="83b6c-194">**PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="83b6c-194">**PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="83b6c-195">Alle Ordner Inhalt Tabellen</span><span class="sxs-lookup"><span data-stu-id="83b6c-195">All folder contents tables</span></span>  <br/> |
|<span data-ttu-id="83b6c-196">**PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="83b6c-196">**PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="83b6c-197">Alle Ordner Inhalt Tabellen</span><span class="sxs-lookup"><span data-stu-id="83b6c-197">All folder contents tables</span></span>  <br/> |
|<span data-ttu-id="83b6c-198">**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="83b6c-198">**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="83b6c-199">Alle Ordner Inhalt Tabellen</span><span class="sxs-lookup"><span data-stu-id="83b6c-199">All folder contents tables</span></span>  <br/> |
|<span data-ttu-id="83b6c-200">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="83b6c-200">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="83b6c-201">Address Book Container Tabellen</span><span class="sxs-lookup"><span data-stu-id="83b6c-201">Address book container tables</span></span>  <br/> |
|<span data-ttu-id="83b6c-202">**PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="83b6c-202">**PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="83b6c-203">Address Book Container Tabellen</span><span class="sxs-lookup"><span data-stu-id="83b6c-203">Address book container tables</span></span>  <br/> |
|<span data-ttu-id="83b6c-204">**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="83b6c-204">**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="83b6c-205">Alle Ordner Inhalt Tabellen</span><span class="sxs-lookup"><span data-stu-id="83b6c-205">All folder contents tables</span></span>  <br/> |
|<span data-ttu-id="83b6c-206">**PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="83b6c-206">**PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="83b6c-207">Alle Ordner Inhalt Tabellen</span><span class="sxs-lookup"><span data-stu-id="83b6c-207">All folder contents tables</span></span>  <br/> |
|<span data-ttu-id="83b6c-208">**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="83b6c-208">**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="83b6c-209">Alle Ordner Inhalt Tabellen</span><span class="sxs-lookup"><span data-stu-id="83b6c-209">All folder contents tables</span></span>  <br/> |
|<span data-ttu-id="83b6c-210">**PR_TRANSMITABLE_DISPLAY_NAME** ([PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="83b6c-210">**PR_TRANSMITABLE_DISPLAY_NAME** ([PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="83b6c-211">Address Book Container Tabellen</span><span class="sxs-lookup"><span data-stu-id="83b6c-211">Address book container tables</span></span>  <br/> |
   
<span data-ttu-id="83b6c-212">Nachricht-Anbieter müssen auch **PR_PARENT_DISPLAY** ([PidTagParentDisplay](pidtagparentdisplay-canonical-property.md)) Suchergebnis Ordner Inhalt nur für Tabellen enthalten.</span><span class="sxs-lookup"><span data-stu-id="83b6c-212">Message store providers must also include **PR_PARENT_DISPLAY** ([PidTagParentDisplay](pidtagparentdisplay-canonical-property.md)) for search-result folders contents tables only.</span></span>
  
<span data-ttu-id="83b6c-213">Benannte Eigenschaften können auf die Spalte einer Tabelle der Ordner-Inhalt hinzugefügt werden, nur, wenn alle Nachrichten in den Ordner die gleiche Zuordnung Signatur, d. h., der Zuordnung von Eigenschaftennamen Eigenschaftenbezeichner haben.</span><span class="sxs-lookup"><span data-stu-id="83b6c-213">Named properties may be added to the column set of a folder contents table only if all messages in the folder have the same mapping signature, that is, the same mapping of property names to property identifiers.</span></span> <span data-ttu-id="83b6c-214">Wenn sie die Erstellung von beliebigen Nachrichten im Ordner unterstützen, sollte Ordner Inhalt Tabellen hinzufügen Nachrichtenklasse spezifische Eigenschaften auf die Spalte festzulegen, unterstützen.</span><span class="sxs-lookup"><span data-stu-id="83b6c-214">Folder contents tables should support adding message class specific properties to the column set, if they support the creation of arbitrary messages in the folder.</span></span>
  
<span data-ttu-id="83b6c-215">Clients können die Standard-Sortierreihenfolge für einen Ordner Inhaltstabelle speichern, dessen [IMAPIFolder::SaveContentsSort](imapifolder-savecontentssort.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="83b6c-215">Clients can save the default sort order for a folder contents table by calling its [IMAPIFolder::SaveContentsSort](imapifolder-savecontentssort.md) method.</span></span> <span data-ttu-id="83b6c-216">Wenn das Flag RECURSIVE_SORT dem Gespräch angegeben wird, kann die Sortierreihenfolge vorgenommen werden, auf alle Unterordner innerhalb des Ordners anwenden.</span><span class="sxs-lookup"><span data-stu-id="83b6c-216">If the RECURSIVE_SORT flag is specified on the call, the sort order can be made to apply to all of the subfolders within the folder.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="83b6c-217">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="83b6c-217">See also</span></span>



[<span data-ttu-id="83b6c-218">MAPI-Tabellen</span><span class="sxs-lookup"><span data-stu-id="83b6c-218">MAPI Tables</span></span>](mapi-tables.md)
