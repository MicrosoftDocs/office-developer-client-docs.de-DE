---
title: IMAPISessionOpenMsgStore
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.OpenMsgStore
api_type:
- COM
ms.assetid: 7f73b5cf-7093-42e9-8acc-63d73df77cf5
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 19d3df004676a71e2bf6243d9288efd824d99c33
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418022"
---
# <a name="imapisessionopenmsgstore"></a><span data-ttu-id="c8bca-103">IMAPISession::OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="c8bca-103">IMAPISession::OpenMsgStore</span></span>

<span data-ttu-id="c8bca-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c8bca-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c8bca-105">Öffnet einen Nachrichtenspeicher und gibt einen [IMsgStore-Zeiger](imsgstoreimapiprop.md) für weiteren Zugriff zurück.</span><span class="sxs-lookup"><span data-stu-id="c8bca-105">Opens a message store and returns an [IMsgStore](imsgstoreimapiprop.md) pointer for further access.</span></span> 
  
```cpp
HRESULT OpenMsgStore(
  ULONG_PTR ulUIParam,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPMDB FAR * lppMDB
);
```

## <a name="parameters"></a><span data-ttu-id="c8bca-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c8bca-106">Parameters</span></span>

<span data-ttu-id="c8bca-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="c8bca-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="c8bca-108">[in] Ein Handle zum übergeordneten Fenster des Dialogfelds allgemeine Adresse und andere zugehörige Displays.</span><span class="sxs-lookup"><span data-stu-id="c8bca-108">[in] A handle to the parent window of the common address dialog box and other related displays.</span></span>
    
<span data-ttu-id="c8bca-109">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="c8bca-109">_cbEntryID_</span></span>
  
> <span data-ttu-id="c8bca-110">[in] Die Byteanzahl im Eintragsbezeichner, auf den der  _lpEntryID-Parameter_ verweist.</span><span class="sxs-lookup"><span data-stu-id="c8bca-110">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
<span data-ttu-id="c8bca-111">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="c8bca-111">_lpEntryID_</span></span>
  
> <span data-ttu-id="c8bca-112">[in] Ein Zeiger auf die Eintrags-ID des zu öffnende Nachrichtenspeichers.</span><span class="sxs-lookup"><span data-stu-id="c8bca-112">[in] A pointer to the entry identifier of the message store to be opened.</span></span> <span data-ttu-id="c8bca-113">Der  _lpEntryID-Parameter_ darf nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="c8bca-113">The  _lpEntryID_ parameter must not be NULL.</span></span> 
    
<span data-ttu-id="c8bca-114">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="c8bca-114">_lpInterface_</span></span>
  
> <span data-ttu-id="c8bca-115">[in] Ein Zeiger auf die Schnittstellen-ID (Interface Identifier, IID), die die Schnittstelle darstellt, die für den Zugriff auf den Nachrichtenspeicher verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c8bca-115">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the message store.</span></span> <span data-ttu-id="c8bca-116">Durch Übergeben von NULL gibt  _der lppMDB-Parameter_ einen Zeiger auf die Standardschnittstelle für einen Nachrichtenspeicher zurück (**IMsgStore**).</span><span class="sxs-lookup"><span data-stu-id="c8bca-116">Passing NULL causes the  _lppMDB_ parameter to return a pointer to the standard interface for a message store (**IMsgStore**).</span></span>
    
<span data-ttu-id="c8bca-117">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c8bca-117">_ulFlags_</span></span>
  
> <span data-ttu-id="c8bca-118">[in] Eine Bitmaske mit Flags, die steuert, wie das Objekt geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="c8bca-118">[in] A bitmask of flags that controls how the object is opened.</span></span> <span data-ttu-id="c8bca-119">Die folgenden Kennzeichen können verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="c8bca-119">The following flags can be used:</span></span>
    
  - <span data-ttu-id="c8bca-120">MAPI_BEST_ACCESS: Fordert an, dass der Nachrichtenspeicher mit den maximal zulässigen Netzwerkberechtigungen für den Benutzer und den maximalen Clientanwendungsberechtigungen geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="c8bca-120">MAPI_BEST_ACCESS: Requests that the message store be opened with the maximum network permissions allowed for the user and the maximum client application permissions.</span></span> <span data-ttu-id="c8bca-121">Wenn der Client beispielsweise über Lese-/Schreibberechtigungen verfügt, sollte der Nachrichtenspeicher mit Lese-/Schreibberechtigung geöffnet werden. Wenn der Client über schreibgeschützte Berechtigungen verfügt, sollte der Nachrichtenspeicher mit schreibgeschützter Berechtigung geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="c8bca-121">For example, if the client has read/write permission, the message store should be opened with read/write permission; if the client has read-only permission, the message store should be opened with read-only permission.</span></span> 
      
  - <span data-ttu-id="c8bca-122">MAPI_DEFERRED_ERRORS: Ermöglicht **es OpenMsgStore,** erfolgreich zurückzukehren, möglicherweise bevor der Nachrichtenspeicher vollständig für den aufrufenden Client verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="c8bca-122">MAPI_DEFERRED_ERRORS: Allows **OpenMsgStore** to return successfully, possibly before the message store is fully available to the calling client.</span></span> <span data-ttu-id="c8bca-123">Wenn der Nachrichtenspeicher nicht verfügbar ist, kann durch einen nachfolgenden Objektaufruf ein Fehler verursacht werden.</span><span class="sxs-lookup"><span data-stu-id="c8bca-123">If the message store is not available, making a subsequent object call can raise an error.</span></span> 
      
  - <span data-ttu-id="c8bca-124">MDB \_ NO_DIALOG: Verhindert die Anzeige von Anmeldedialogfeldern.</span><span class="sxs-lookup"><span data-stu-id="c8bca-124">MDB\_NO_DIALOG: Prevents the display of logon dialog boxes.</span></span> <span data-ttu-id="c8bca-125">Wenn dieses Kennzeichen festgelegt ist und **OpenMsgStore** nicht über ausreichende Konfigurationsinformationen verfügt, um den Nachrichtenspeicher ohne Hilfe des Benutzers zu öffnen, wird MAPI_E_LOGON_FAILED.</span><span class="sxs-lookup"><span data-stu-id="c8bca-125">If this flag is set, and **OpenMsgStore** has insufficient configuration information to open the message store without the user's help, it returns MAPI_E_LOGON_FAILED.</span></span> <span data-ttu-id="c8bca-126">Wenn dieses Kennzeichen nicht festgelegt ist, kann der Nachrichtenspeicheranbieter den Benutzer zum Korrigieren eines Namens oder Kennworts oder zum Ausführen anderer Aktionen zum Herstellen einer Verbindung mit dem Nachrichtenspeicher aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="c8bca-126">If this flag is not set, the message store provider can prompt the user to correct a name or password or to perform other actions that are needed to establish a connection to the message store.</span></span> 
      
  - <span data-ttu-id="c8bca-127">MDB NO_MAIL: Der Nachrichtenspeicher sollte nicht zum Senden oder Empfangen \_ von E-Mails verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c8bca-127">MDB\_NO_MAIL: The message store should not be used for sending or receiving mail.</span></span> <span data-ttu-id="c8bca-128">Wenn dieses Flag festgelegt ist, benachrichtigt MAPI den MAPI-Spooler nicht darüber, dass dieser Nachrichtenspeicher geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="c8bca-128">When this flag is set, MAPI does not notify the MAPI spooler that this message store is being opened.</span></span>
      
  - <span data-ttu-id="c8bca-129">MDB ONLINE: Im Cache-Exchange-Modus kann ein Client oder Dienstanbieter diese Methode mit MDB_ONLINE aufrufen, um die Verbindung zum lokalen Nachrichtenspeicher zu überschreiben und den Speicher auf dem Remoteserver \_ zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="c8bca-129">MDB\_ONLINE: In Cached Exchange Mode, a client or service provider can call this method with MDB_ONLINE to override the connection to the local message store and open the store on the remote server.</span></span> <span data-ttu-id="c8bca-130">Sie können einen Exchange im Cachemodus und im nicht zwischengespeicherten Modus nicht gleichzeitig in derselben MAPI-Sitzung öffnen.</span><span class="sxs-lookup"><span data-stu-id="c8bca-130">You cannot open an Exchange store in cached mode and in non-cached mode at the same time in the same MAPI session.</span></span> <span data-ttu-id="c8bca-131">Wenn Sie den zwischengespeicherten Nachrichtenspeicher bereits geöffnet haben, müssen Sie entweder den Speicher schließen, bevor Sie ihn mit dieser Kennzeichnung öffnen, oder eine neue MAPI-Sitzung öffnen, in der Sie den Exchange-Speicher auf dem Remoteserver mit dieser Kennzeichnung öffnen können.</span><span class="sxs-lookup"><span data-stu-id="c8bca-131">If you have already opened the cached message store, you must either close the store before you open it with this flag, or open a new MAPI session where you can open the Exchange store on the remote server by using this flag.</span></span>
      
  - <span data-ttu-id="c8bca-132">MDB_TEMPORARY: Die MAPI wird angewiesen, dass der Nachrichtenspeicher nicht dauerhaft ist und nicht der Nachrichtenspeichertabelle hinzugefügt werden sollte.</span><span class="sxs-lookup"><span data-stu-id="c8bca-132">MDB_TEMPORARY: Instructs MAPI that the message store is not permanent and should not be added to the message store table.</span></span> <span data-ttu-id="c8bca-133">Dieses Flag wird zum Anmelden am Nachrichtenspeicher verwendet, damit Informationen programmgesteuert aus dem Profilabschnitt abgerufen werden können.</span><span class="sxs-lookup"><span data-stu-id="c8bca-133">This flag is used to log on to the message store so information can be retrieved programmatically from the profile section.</span></span> 
      
  - <span data-ttu-id="c8bca-134">MDB_WRITE: Fordert Lese-/Schreibberechtigungen für den Nachrichtenspeicher an.</span><span class="sxs-lookup"><span data-stu-id="c8bca-134">MDB_WRITE: Requests read/write permission to the message store.</span></span>
    
<span data-ttu-id="c8bca-135">_lppMDB_</span><span class="sxs-lookup"><span data-stu-id="c8bca-135">_lppMDB_</span></span>
  
> <span data-ttu-id="c8bca-136">[out] Zeiger auf einen Zeiger des Nachrichtenspeichers.</span><span class="sxs-lookup"><span data-stu-id="c8bca-136">[out] Pointer to a pointer of the message store.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c8bca-137">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c8bca-137">Return value</span></span>

<span data-ttu-id="c8bca-138">S_OK</span><span class="sxs-lookup"><span data-stu-id="c8bca-138">S_OK</span></span> 
  
> <span data-ttu-id="c8bca-139">Der Nachrichtenspeicher wurde erfolgreich geöffnet.</span><span class="sxs-lookup"><span data-stu-id="c8bca-139">The message store was successfully opened.</span></span>
    
<span data-ttu-id="c8bca-140">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="c8bca-140">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="c8bca-141">Es wurde versucht, auf einen Nachrichtenspeicher zu zugreifen, für den der Benutzer nicht über ausreichende Berechtigungen verfügt.</span><span class="sxs-lookup"><span data-stu-id="c8bca-141">An attempt was made to access a message store for which the user has insufficient permissions.</span></span>
    
<span data-ttu-id="c8bca-142">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="c8bca-142">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="c8bca-143">Der durch  _lpEntryID_ angegebene Nachrichtenspeicher ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="c8bca-143">The message store indicated by  _lpEntryID_ does not exist.</span></span> 
    
<span data-ttu-id="c8bca-144">MAPI_E_UNKNOWN_CPID</span><span class="sxs-lookup"><span data-stu-id="c8bca-144">MAPI_E_UNKNOWN_CPID</span></span> 
  
> <span data-ttu-id="c8bca-145">Der Server ist nicht für die Unterstützung der Codeseite des Clients konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="c8bca-145">The server is not configured to support the client's code page.</span></span>
    
<span data-ttu-id="c8bca-146">MAPI_E_UNKNOWN_LCID</span><span class="sxs-lookup"><span data-stu-id="c8bca-146">MAPI_E_UNKNOWN_LCID</span></span> 
  
> <span data-ttu-id="c8bca-147">Der Server ist nicht für die Unterstützung der Locale-Informationen des Clients konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="c8bca-147">The server is not configured to support the client's locale information.</span></span>
    
<span data-ttu-id="c8bca-148">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="c8bca-148">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="c8bca-149">Der Aufruf ist erfolgreich, der Nachrichtenspeicheranbieter verfügt jedoch über Fehlerinformationen.</span><span class="sxs-lookup"><span data-stu-id="c8bca-149">The call succeeded, but the message store provider has error information available.</span></span> <span data-ttu-id="c8bca-150">Wenn diese Warnung zurückgegeben wird, sollte der Anruf als erfolgreich behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="c8bca-150">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="c8bca-151">Rufen Sie die [IMAPISession::GetLastError-Methode](imapisession-getlasterror.md) auf, um die Fehlerinformationen vom Anbieter zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="c8bca-151">To get the error information from the provider, call the [IMAPISession::GetLastError](imapisession-getlasterror.md) method.</span></span> <span data-ttu-id="c8bca-152">Verwenden Sie zum Testen dieser Warnung das **HR_FAILED** Makro.</span><span class="sxs-lookup"><span data-stu-id="c8bca-152">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="c8bca-153">Weitere Informationen finden Sie unter [Using Macros for Error Handling](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="c8bca-153">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c8bca-154">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c8bca-154">Remarks</span></span>

<span data-ttu-id="c8bca-155">Die **IMAPISession::OpenMsgStore-Methode** öffnet einen bestimmten Nachrichtenspeicher.</span><span class="sxs-lookup"><span data-stu-id="c8bca-155">The **IMAPISession::OpenMsgStore** method opens a particular message store.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="c8bca-156">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="c8bca-156">Notes to callers</span></span>

<span data-ttu-id="c8bca-157">Die Standardberechtigungsstufe für Nachrichtenspeicher ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="c8bca-157">The default permission level for message stores is read-only.</span></span> <span data-ttu-id="c8bca-158">Wenn Sie das MDB_WRITE festlegen, erhalten Sie möglicherweise keine Lese-/Schreibberechtigung.</span><span class="sxs-lookup"><span data-stu-id="c8bca-158">If you set the MDB_WRITE flag, you still might not be granted read/write permission.</span></span> <span data-ttu-id="c8bca-159">Die letzte Zugriffsebene, die MAPI dem Nachrichtenspeicher zuteil wird, hängt von Ihrer Berechtigungsstufe, dem Nachrichtenspeicher selbst und dem Nachrichtenspeicheranbieter ab.</span><span class="sxs-lookup"><span data-stu-id="c8bca-159">The final level of access that MAPI assigns to the message store depends on your permission level, the message store itself, and the message store provider.</span></span> 
  
<span data-ttu-id="c8bca-160">Wenn Sie **OpenMsgStore aufrufen,** um einen Nachrichtenspeicher mit schreibgeschützter Berechtigung zu öffnen, tritt Folgendes auf:</span><span class="sxs-lookup"><span data-stu-id="c8bca-160">If you call **OpenMsgStore** to open a message store with read-only permission, the following will occur:</span></span> 
  
- <span data-ttu-id="c8bca-161">Die **\_ PR-STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))-Eigenschaft des Speichers verfügt nicht über die \_ STORE-MODIFY_OK und store \_ CREATE_OK Bits.</span><span class="sxs-lookup"><span data-stu-id="c8bca-161">The store's **PR\_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property will not have its STORE\_MODIFY_OK and STORE\_CREATE_OK bits set.</span></span> 
    
- <span data-ttu-id="c8bca-162">Aufrufe zum Öffnen einer der Nachrichten oder Ordner des Nachrichtenspeichers mithilfe von [IMAPISession::OpenEntry](imapisession-openentry.md) mit dem MAPI_MODIFY werden fehlschlagen.</span><span class="sxs-lookup"><span data-stu-id="c8bca-162">Calls to open one of the message store's messages or folders by using [IMAPISession::OpenEntry](imapisession-openentry.md) with the MAPI_MODIFY flag set will fail.</span></span> 
    
- <span data-ttu-id="c8bca-163">Aufrufe zum Öffnen einer der Eigenschaften der Nachrichten oder Ordner des Nachrichtenspeichers mithilfe von [IMAPIProp::OpenProperty](imapiprop-openproperty.md) mit dem MAPI_MODIFY werden fehlschlagen.</span><span class="sxs-lookup"><span data-stu-id="c8bca-163">Calls to open one of the properties of the message store's messages or folders by using [IMAPIProp::OpenProperty](imapiprop-openproperty.md) with the MAPI_MODIFY flag will fail.</span></span> 
    
- <span data-ttu-id="c8bca-164">Aufrufe einer der folgenden Methoden führen zu einem Fehler:</span><span class="sxs-lookup"><span data-stu-id="c8bca-164">Calls to any of the following methods will fail:</span></span> 
    
  - [<span data-ttu-id="c8bca-165">IMAPIFolder::CreateMessage</span><span class="sxs-lookup"><span data-stu-id="c8bca-165">IMAPIFolder::CreateMessage</span></span>](imapifolder-createmessage.md)
    
  - [<span data-ttu-id="c8bca-166">IMAPIFolder::DeleteMessages</span><span class="sxs-lookup"><span data-stu-id="c8bca-166">IMAPIFolder::DeleteMessages</span></span>](imapifolder-deletemessages.md)
    
  - [<span data-ttu-id="c8bca-167">IMAPIFolder::CreateFolder</span><span class="sxs-lookup"><span data-stu-id="c8bca-167">IMAPIFolder::CreateFolder</span></span>](imapifolder-createfolder.md)
    
  - [<span data-ttu-id="c8bca-168">IMAPIFolder::DeleteFolder</span><span class="sxs-lookup"><span data-stu-id="c8bca-168">IMAPIFolder::DeleteFolder</span></span>](imapifolder-deletefolder.md)
    
  - [<span data-ttu-id="c8bca-169">IMAPIFolder::SetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="c8bca-169">IMAPIFolder::SetMessageStatus</span></span>](imapifolder-setmessagestatus.md)
    
  - [<span data-ttu-id="c8bca-170">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="c8bca-170">IMAPIProp::SetProps</span></span>](imapiprop-setprops.md)
    
  - [<span data-ttu-id="c8bca-171">IMAPIProp::DeleteProps</span><span class="sxs-lookup"><span data-stu-id="c8bca-171">IMAPIProp::DeleteProps</span></span>](imapiprop-deleteprops.md)
  
- <span data-ttu-id="c8bca-172">Aufrufe der folgenden Methoden führen zu einem Fehler, wenn das Ziel für die kopierte Nachricht schreibgeschützt ist, ob das Ziel mit dem Quellnachrichtenspeicher identisch ist oder ein anderer schreibgeschützter Speicher ist.</span><span class="sxs-lookup"><span data-stu-id="c8bca-172">Calls to the following methods will fail if the destination for the copied message is read-only, whether the destination is the same as the source message store or is another read-only store.</span></span>
    
  - [<span data-ttu-id="c8bca-173">IMAPIFolder::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="c8bca-173">IMAPIFolder::CopyMessages</span></span>](imapifolder-copymessages.md)
    
  - [<span data-ttu-id="c8bca-174">IMAPIFolder::CopyFolder</span><span class="sxs-lookup"><span data-stu-id="c8bca-174">IMAPIFolder::CopyFolder</span></span>](imapifolder-copyfolder.md)
    
  - [<span data-ttu-id="c8bca-175">IMAPIProp::CopyTo</span><span class="sxs-lookup"><span data-stu-id="c8bca-175">IMAPIProp::CopyTo</span></span>](imapiprop-copyto.md)
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="c8bca-176">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="c8bca-176">MFCMAPI reference</span></span>

<span data-ttu-id="c8bca-177">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="c8bca-177">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="c8bca-178">**Datei**</span><span class="sxs-lookup"><span data-stu-id="c8bca-178">**File**</span></span>|<span data-ttu-id="c8bca-179">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="c8bca-179">**Function**</span></span>|<span data-ttu-id="c8bca-180">**Comment**</span><span class="sxs-lookup"><span data-stu-id="c8bca-180">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c8bca-181">MAPIStoreFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="c8bca-181">MAPIStoreFunctions.cpp</span></span>  <br/> |<span data-ttu-id="c8bca-182">CallOpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="c8bca-182">CallOpenMsgStore</span></span>  <br/> |<span data-ttu-id="c8bca-183">MFCMAPI verwendet die **IMAPISession::OpenMsgStore-Methode,** um einen Nachrichtenspeicher zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="c8bca-183">MFCMAPI uses the **IMAPISession::OpenMsgStore** method to open a message store.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c8bca-184">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c8bca-184">See also</span></span>

- [<span data-ttu-id="c8bca-185">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="c8bca-185">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)
- [<span data-ttu-id="c8bca-186">IMAPISession::GetLastError</span><span class="sxs-lookup"><span data-stu-id="c8bca-186">IMAPISession::GetLastError</span></span>](imapisession-getlasterror.md)
- [<span data-ttu-id="c8bca-187">IMAPISession::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="c8bca-187">IMAPISession::OpenEntry</span></span>](imapisession-openentry.md)
- [<span data-ttu-id="c8bca-188">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="c8bca-188">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
- [<span data-ttu-id="c8bca-189">IMAPISession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c8bca-189">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)
- [<span data-ttu-id="c8bca-190">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="c8bca-190">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
- [<span data-ttu-id="c8bca-191">Verwenden von Makros für die Fehlerbehandlung</span><span class="sxs-lookup"><span data-stu-id="c8bca-191">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

