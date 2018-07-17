---
title: IABProviderLogon
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABProvider.Logon
api_type:
- COM
ms.assetid: f9468715-1674-4d14-81c8-2f24dbaa0453
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 21a6907f7511779d7e8ec6825ac68d109d2f48eb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791983"
---
# <a name="iabproviderlogon"></a><span data-ttu-id="99192-103">IABProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="99192-103">IABProvider::Logon</span></span>

  
  
<span data-ttu-id="99192-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="99192-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="99192-105">Stellt eine Verbindung mit einer aktiven Sitzung her.</span><span class="sxs-lookup"><span data-stu-id="99192-105">Establishes a connection to an active session.</span></span>
  
```cpp
HRESULT Logon(
  LPMAPISUP lpMAPISup,
  ULONG_PTR ulUIParam,
  LPSTR lpszProfileName,
  ULONG ulFlags,
  ULONG FAR * lpulcbSecurity,
  LPBYTE FAR * lppbSecurity,
  LPMAPIERROR FAR * lppMAPIError,
  LPABLOGON FAR * lppABLogon
);
```

## <a name="parameters"></a><span data-ttu-id="99192-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="99192-106">Parameters</span></span>

 <span data-ttu-id="99192-107">_lpMAPISup_</span><span class="sxs-lookup"><span data-stu-id="99192-107">_lpMAPISup_</span></span>
  
> <span data-ttu-id="99192-108">[in] Ein Zeiger auf die Adressbuchanbieter DSO-Objekt.</span><span class="sxs-lookup"><span data-stu-id="99192-108">[in] A pointer to the address book provider's support object.</span></span>
    
 <span data-ttu-id="99192-109">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="99192-109">_ulUIParam_</span></span>
  
> <span data-ttu-id="99192-110">[in] Ein Handle für das übergeordnete Fenster für das Dialogfeld anmelden, die die **Logon** -Methode angezeigt, wenn zulässig.</span><span class="sxs-lookup"><span data-stu-id="99192-110">[in] A handle to the parent window for the logon dialog box that the **Logon** method displays, if permitted.</span></span> <span data-ttu-id="99192-111">Der Parameter _UlUIParam_ enthält den Wert des Parameters mit demselben Namen in der vorherigen Aufruf der Funktion [MAPILogonEx](mapilogonex.md) MAPI übergeben.</span><span class="sxs-lookup"><span data-stu-id="99192-111">The  _ulUIParam_ parameter contains the value of the parameter of the same name passed to MAPI in the previous call to the [MAPILogonEx](mapilogonex.md) function.</span></span> 
    
 <span data-ttu-id="99192-112">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="99192-112">_lpszProfileName_</span></span>
  
> <span data-ttu-id="99192-113">[in] Ein Zeiger auf den Namen des Profils Sitzung.</span><span class="sxs-lookup"><span data-stu-id="99192-113">[in] A pointer to the name of the session profile.</span></span>
    
 <span data-ttu-id="99192-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="99192-114">_ulFlags_</span></span>
  
> <span data-ttu-id="99192-115">[in] Eine Bitmaske aus Flags, die steuert, wie die Anmeldung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="99192-115">[in] A bitmask of flags that controls how the logon is performed.</span></span> <span data-ttu-id="99192-116">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="99192-116">The following flags can be set:</span></span>
    
<span data-ttu-id="99192-117">AB_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="99192-117">AB_NO_DIALOG</span></span> 
  
> <span data-ttu-id="99192-118">Der Anbieter sollte kein Dialogfeld während der Anmeldung angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="99192-118">The provider should not display a dialog box during logon.</span></span> <span data-ttu-id="99192-119">Wenn dieses Flag nicht festgelegt ist, kann der Anbieter ein Dialogfeld, um den Benutzer aufzufordern, nach fehlenden Konfigurationsinformationen anzeigen.</span><span class="sxs-lookup"><span data-stu-id="99192-119">If this flag is not set, the provider can display a dialog box to prompt the user for missing configuration information.</span></span>
    
<span data-ttu-id="99192-120">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="99192-120">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="99192-121">**Anmeldung** erfolgreich, möglicherweise vor Abschluss des Anmeldevorgangs zurückgeben können.</span><span class="sxs-lookup"><span data-stu-id="99192-121">Enables **Logon** to return successfully, possibly before the logon process is finished.</span></span> 
    
<span data-ttu-id="99192-122">PARAMETER MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="99192-122">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="99192-123">Alle Zeichenfolgen sollte im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="99192-123">All strings should be in Unicode format.</span></span> <span data-ttu-id="99192-124">Wenn die Option MAPI_UNICODE nicht festgelegt ist, sollte die Zeichenfolgen in ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="99192-124">If the MAPI_UNICODE flag is not set, the strings should be in ANSI format.</span></span>
    
 <span data-ttu-id="99192-125">_lpulcbSecurity_</span><span class="sxs-lookup"><span data-stu-id="99192-125">_lpulcbSecurity_</span></span>
  
> <span data-ttu-id="99192-126">[in, out] Ein Zeiger auf die Größe der Struktur der Sicherheits-Anmeldeinformationen auf das durch den Parameter _LppbSecurity_ in Bytes.</span><span class="sxs-lookup"><span data-stu-id="99192-126">[in, out] A pointer to the size, in bytes, of the security credentials structure pointed to by the  _lppbSecurity_ parameter.</span></span> <span data-ttu-id="99192-127">Bei der Eingabe muss der Wert ungleich NULL sein. Bei der Ausgabe muss der Wert 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="99192-127">On input, the value must be nonzero; on output, the value must be zero.</span></span> <span data-ttu-id="99192-128">In beiden Fällen müssen die Zeiger gültig sein.</span><span class="sxs-lookup"><span data-stu-id="99192-128">In both cases, the pointers must be valid.</span></span> 
    
 <span data-ttu-id="99192-129">_lppbSecurity_</span><span class="sxs-lookup"><span data-stu-id="99192-129">_lppbSecurity_</span></span>
  
> <span data-ttu-id="99192-130">[in, out] Ein Zeiger auf einen Zeiger auf Sicherheitsanmeldeinformationen.</span><span class="sxs-lookup"><span data-stu-id="99192-130">[in, out] A pointer to a pointer to security credentials.</span></span> <span data-ttu-id="99192-131">Bei der Eingabe muss der Wert ungleich NULL sein. Bei der Ausgabe muss der Wert 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="99192-131">On input, the value must be nonzero; on output, the value must be zero.</span></span> <span data-ttu-id="99192-132">In beiden Fällen muss der Zeiger gültig sein.</span><span class="sxs-lookup"><span data-stu-id="99192-132">In both cases the pointer must be valid.</span></span>
    
 <span data-ttu-id="99192-133">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="99192-133">_lppMAPIError_</span></span>
  
> <span data-ttu-id="99192-134">[out] Ein Zeiger auf einen Zeiger auf eine [MAPIERROR](mapierror.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="99192-134">[out] A pointer to a pointer to a [MAPIERROR](mapierror.md) structure.</span></span> <span data-ttu-id="99192-135">Der Parameter _LppMAPIError_ kann auf NULL festgelegt werden, wenn es keine **MAPIERROR** -Struktur ist zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="99192-135">The  _lppMAPIError_ parameter can be set to NULL if there is no **MAPIERROR** structure to return.</span></span> 
    
 <span data-ttu-id="99192-136">_lppABLogon_</span><span class="sxs-lookup"><span data-stu-id="99192-136">_lppABLogon_</span></span>
  
> <span data-ttu-id="99192-137">[out] Ein Zeiger auf einen Zeiger auf das Objekt für den Anbieter anmelden.</span><span class="sxs-lookup"><span data-stu-id="99192-137">[out] A pointer to a pointer to the provider's logon object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="99192-138">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="99192-138">Return value</span></span>

<span data-ttu-id="99192-139">S_OK</span><span class="sxs-lookup"><span data-stu-id="99192-139">S_OK</span></span> 
  
> <span data-ttu-id="99192-140">Eine Verbindung mit einer aktiven Sitzung wurde erfolgreich hergestellt.</span><span class="sxs-lookup"><span data-stu-id="99192-140">A connection to an active session was successfully established.</span></span>
    
<span data-ttu-id="99192-141">MAPI_E_FAILONEPROVIDER</span><span class="sxs-lookup"><span data-stu-id="99192-141">MAPI_E_FAILONEPROVIDER</span></span> 
  
> <span data-ttu-id="99192-142">Der Anbieter nicht anmelden kann, MAPI jedoch weiterhin die anderen Anbieter in der Nachrichtendienst anmelden zu der der Anbieter gehört.</span><span class="sxs-lookup"><span data-stu-id="99192-142">The provider cannot log on, but MAPI can continue to log on the other providers in the message service to which the provider belongs.</span></span> 
    
<span data-ttu-id="99192-143">MAPI_E_UNCONFIGURED</span><span class="sxs-lookup"><span data-stu-id="99192-143">MAPI_E_UNCONFIGURED</span></span> 
  
> <span data-ttu-id="99192-144">Der Anbieter verfügt über nicht genügend Informationen für die Durchführung die Anmeldung.</span><span class="sxs-lookup"><span data-stu-id="99192-144">The provider has insufficient information to complete the logon.</span></span> <span data-ttu-id="99192-145">MAPI-Aufrufen des Anbieters Nachricht Service Eintrag-Funktion.</span><span class="sxs-lookup"><span data-stu-id="99192-145">MAPI calls the provider's message service entry function.</span></span>
    
<span data-ttu-id="99192-146">MAPI_E_UNKNOWN_CPID</span><span class="sxs-lookup"><span data-stu-id="99192-146">MAPI_E_UNKNOWN_CPID</span></span> 
  
> <span data-ttu-id="99192-147">Der Server ist nicht zur Unterstützung der Codeseite für den Client konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="99192-147">The server is not configured to support the client's code page.</span></span>
    
<span data-ttu-id="99192-148">MAPI_E_UNKNOWN_LCID</span><span class="sxs-lookup"><span data-stu-id="99192-148">MAPI_E_UNKNOWN_LCID</span></span> 
  
> <span data-ttu-id="99192-149">Der Server ist nicht konfiguriert, um Gebietsschemainformationen des Clients zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="99192-149">The server is not configured to support the client's locale information.</span></span>
    
<span data-ttu-id="99192-150">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="99192-150">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="99192-151">Der Benutzer hat den Vorgang in der Regel durch Klicken auf die Schaltfläche **Abbrechen** im Dialogfeld Anmeldung abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="99192-151">The user canceled the operation, typically by clicking the **Cancel** button in the logon dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="99192-152">Hinweise</span><span class="sxs-lookup"><span data-stu-id="99192-152">Remarks</span></span>

<span data-ttu-id="99192-153">Verbindungen sind mit jedem Adressbuchanbieter im Profil der Sitzung eingerichtet, wenn ein Client die [IMAPISession::OpenAddressBook](imapisession-openaddressbook.md) -Methode aufruft.</span><span class="sxs-lookup"><span data-stu-id="99192-153">Connections are established with each address book provider in the session profile when a client calls the [IMAPISession::OpenAddressBook](imapisession-openaddressbook.md) method.</span></span> <span data-ttu-id="99192-154">**OpenAddressBook** ruft dann des Anbieters **Logon** (Methode).</span><span class="sxs-lookup"><span data-stu-id="99192-154">**OpenAddressBook** then calls each provider's **Logon** method.</span></span> 
  
<span data-ttu-id="99192-155">Der Name der Benutzerprofildienst auf das durch den Parameter _LpszProfileName_ wird in den Zeichensatz des Client des Benutzers, wie durch die Anwesenheit oder Abwesenheit die Option MAPI_UNICODE im _UlFlags_ -Parameter angegeben angezeigt.</span><span class="sxs-lookup"><span data-stu-id="99192-155">The profile name pointed to by the  _lpszProfileName_ parameter is displayed in the character set of the user's client as indicated by the presence or absence of the MAPI_UNICODE flag in the  _ulFlags_ parameter.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="99192-156">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="99192-156">Notes to implementers</span></span>

<span data-ttu-id="99192-157">Rufen Sie in der Implementierung der die **Logon** -Methode die [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) -Methode, um eine eindeutige ID oder [MAPIUID](mapiuid.md) -Struktur zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="99192-157">In your implementation of the **Logon** method, call the [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) method to register a unique identifier, or [MAPIUID](mapiuid.md) structure.</span></span> <span data-ttu-id="99192-158">Jedes Ihrer Objekte haben eine Eintrags-ID, die diese **MAPIUID**enthält.</span><span class="sxs-lookup"><span data-stu-id="99192-158">Each of your objects will have an entry identifier that includes this **MAPIUID**.</span></span> <span data-ttu-id="99192-159">MAPI verwendet die **MAPIUID** , um ein Objekt mit seinen Provider übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="99192-159">MAPI uses the **MAPIUID** to match an object with its provider.</span></span> <span data-ttu-id="99192-160">Wenn ein Client die [IMAPISession::OpenEntry](imapisession-openentry.md) -Methode, um ein messaging-Benutzer öffnen aufruft, untersucht **OpenEntry** beispielsweise den **MAPIUID** Teil der Eintrags-ID, die übergeben wurde, und ordnet ihn einem **MAPIUID** registriert, indem ein Adressbuchanbieter.</span><span class="sxs-lookup"><span data-stu-id="99192-160">For example, when a client calls the [IMAPISession::OpenEntry](imapisession-openentry.md) method to open a messaging user, **OpenEntry** examines the **MAPIUID** portion of the entry identifier that was passed in and matches it with a **MAPIUID** registered by an address book provider.</span></span> 
  
<span data-ttu-id="99192-161">Wenn ein Client an Ihren Anbieter nur einmal anmeldet, möchten Sie möglicherweise eine unterschiedliche **MAPIUID** für jede Anmeldung registrieren.</span><span class="sxs-lookup"><span data-stu-id="99192-161">If a client logs on to your provider more than once, you may want to register a different **MAPIUID** for each logon.</span></span> <span data-ttu-id="99192-162">Registrieren eindeutige **MAPIUID** Strukturen ermöglicht MAPI ordnungsgemäß Anforderungen an die entsprechende authentifizierungsanbieterinstanz weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="99192-162">Registering unique **MAPIUID** structures enables MAPI to correctly route requests to the appropriate provider instance.</span></span> <span data-ttu-id="99192-163">Sie möchten jedoch jeder Anmeldung-Objekt eine **MAPIUID**freigeben.</span><span class="sxs-lookup"><span data-stu-id="99192-163">However, you may want to have every logon object share one **MAPIUID**.</span></span> <span data-ttu-id="99192-164">In diesem Fall müssen Sie das routing verarbeiten werden selbst auf MAPI angewiesen.</span><span class="sxs-lookup"><span data-stu-id="99192-164">In this case, you must be able to handle the routing yourself instead of relying on MAPI.</span></span> <span data-ttu-id="99192-165">Weitere Informationen zum Erstellen einer **MAPIUID**finden Sie unter [Registrieren Service Provider eindeutige Bezeichner](registering-service-provider-unique-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="99192-165">For more information about how to create a **MAPIUID**, see [Registering Service Provider Unique Identifiers](registering-service-provider-unique-identifiers.md).</span></span>
  
<span data-ttu-id="99192-166">Das Support-Objekt, das MAPI an Ihre **Logon** -Methode im Parameter _LpMAPISup_ übergibt ermöglicht den Zugriff auf viele der Methoden in enthalten die [IMAPISupport: IUnknown](imapisupportiunknown.md) Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="99192-166">The support object that MAPI passes to your **Logon** method in the  _lpMAPISup_ parameter provides access to many of the methods included in the [IMAPISupport : IUnknown](imapisupportiunknown.md) interface.</span></span> <span data-ttu-id="99192-167">MAPI erstellt ein Support-Objekt, das in den Typ des Anbieters angepasst ist.</span><span class="sxs-lookup"><span data-stu-id="99192-167">MAPI creates a support object that is customized to your type of provider.</span></span> <span data-ttu-id="99192-168">Wenn Sie müssen zur Anmeldung an einer zugrunde liegenden messaging-System oder Verzeichnisdienst, wenn Sie die Verbindung hergestellt wird, können Sie beispielsweise die [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) -Methode zum Abrufen von Anmeldeinformationen für diese Sitzung bestimmte Anmeldung anrufen.</span><span class="sxs-lookup"><span data-stu-id="99192-168">For example, if you need to log on to an underlying messaging system or directory service when you establish your connection, you can call the [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) method to retrieve security credentials for this particular logon session.</span></span> 
  
<span data-ttu-id="99192-169">Wenn die **Anmeldung** erfolgreich ist, müssen Sie unbedingt, dass Sie die des Unterstützungsobjekts [IUnknown:: AddRef](http://msdn.microsoft.com/de-de/library/ms691379%28VS.85%29.aspx) -Methode, um erhöht den Referenzzähler aufrufen.</span><span class="sxs-lookup"><span data-stu-id="99192-169">If **Logon** is successful, be sure that you call the support object's [IUnknown::AddRef](http://msdn.microsoft.com/de-de/library/ms691379%28VS.85%29.aspx) method to increment its reference count.</span></span> <span data-ttu-id="99192-170">Auf diese Weise können vom Dienstanbieter, die auf den Support-Objektzeiger für den Rest der Sitzung enthalten soll.</span><span class="sxs-lookup"><span data-stu-id="99192-170">This enables your provider to hold onto the support object pointer for the rest of the session.</span></span> <span data-ttu-id="99192-171">Wenn Sie diese **AddRef** -Methode nicht aufrufen, wird MAPI vom Dienstanbieter entfernen.</span><span class="sxs-lookup"><span data-stu-id="99192-171">If you do not call this **AddRef** method, MAPI will unload your provider.</span></span> 
  
<span data-ttu-id="99192-172">Sie können den Namen des Profils im Parameter _LpszProfileName_ Fehlerdialogfelder, Anmeldefenster oder andere Elemente der Benutzeroberfläche übergeben einschließen.</span><span class="sxs-lookup"><span data-stu-id="99192-172">You can include the profile name passed in the  _lpszProfileName_ parameter in error dialog boxes, logon screens, or other user interfaces.</span></span> <span data-ttu-id="99192-173">Um den Profilnamen zu verwenden, kopieren Sie sie in einen Speicher, die Sie bereitgestellt haben.</span><span class="sxs-lookup"><span data-stu-id="99192-173">To use the profile name, copy it to storage that you have allocated.</span></span> 
  
<span data-ttu-id="99192-174">Erstellen Sie ein Objekt Anmeldung und zurückkehren Sie einen Zeiger in der _LppABLogon_ -Parameter zu ihm.</span><span class="sxs-lookup"><span data-stu-id="99192-174">Create a logon object and return a pointer to it in the  _lppABLogon_ parameter.</span></span> <span data-ttu-id="99192-175">MAPI verwendet dieses Anmeldeobjekt tätigen von Anrufen an die Methoden in der Implementierung [IABLogon](iablogoniunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="99192-175">MAPI uses this logon object to make calls to the methods in your [IABLogon](iablogoniunknown.md) implementation.</span></span> 
  
<span data-ttu-id="99192-176">Wenn Sie ein Kennwort bei der Anmeldung benötigen, ein Anmeldedialogfeld nur angezeigt, wenn das Flag AB_NO_DIALOG nicht festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="99192-176">If you require a password during logon, display a logon dialog box only if the AB_NO_DIALOG flag is not set.</span></span> <span data-ttu-id="99192-177">Wenn der Benutzer des Anmeldevorgangs abbricht, in der Regel durch Klicken auf die Schaltfläche **Abbrechen** klicken Sie im Dialogfeld zurückgeben Sie MAPI_E_USER_CANCEL aus **Anmelden**.</span><span class="sxs-lookup"><span data-stu-id="99192-177">If the user cancels the logon process, typically by clicking the **Cancel** button in the dialog box, return MAPI_E_USER_CANCEL from **Logon**.</span></span>
  
<span data-ttu-id="99192-178">In der Regel bei der Adressbuch-Dienstanbieter nicht anmelden kann, MAPI wird deaktiviert den Dienst, der der fehlerhaften Anbieter angehört – d. h., MAPI versucht nicht, Verbindungen für andere Anbieter herzustellen, die mit dem Dienst für den Rest der der Sitzung gehören Lebensdauer.</span><span class="sxs-lookup"><span data-stu-id="99192-178">Typically, when an address book provider cannot log on, MAPI disables the message service to which the failing provider belongs—that is, MAPI will not try to establish connections for any of the other providers that belong to the service for the rest of the session's lifetime.</span></span> <span data-ttu-id="99192-179">Wenn vom Dienstanbieter kann keine Verbindung herstellen, und Sie nicht den gesamten Dienst deaktivieren möchten, zurückgeben Sie MAPI_E_FAILONEPROVIDER oder MAPI_E_UNCONFIGURED aus.</span><span class="sxs-lookup"><span data-stu-id="99192-179">However, if your provider cannot establish a connection and you want not to disable the entire service, return either MAPI_E_FAILONEPROVIDER or MAPI_E_UNCONFIGURED.</span></span> <span data-ttu-id="99192-180">MAPI wird nicht den Dienst deaktivieren, zu dem der Anbieter gehört.</span><span class="sxs-lookup"><span data-stu-id="99192-180">MAPI will not disable the message service to which the provider belongs.</span></span> 
  
<span data-ttu-id="99192-181">Rückgabe MAPI_E_FAILONEPROVIDER, wenn ein Fehler auftritt, kann nicht schwerwiegend genug ist, um zu verhindern, dass die anderen Anbieter in der Nachrichtendienst Herstellen einer Verbindung.</span><span class="sxs-lookup"><span data-stu-id="99192-181">Return MAPI_E_FAILONEPROVIDER if an error occurs that is not serious enough to prevent the other providers in the message service from establishing connections.</span></span> <span data-ttu-id="99192-182">MAPI_E_UNCONFIGURED zurück, wenn die erforderlichen Konfigurationsdaten aus dem Profil nicht vorhanden ist und Sie ein Dialogfeld, um den Benutzer aufzufordern können nicht angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="99192-182">Return MAPI_E_UNCONFIGURED if the necessary configuration information is missing from the profile and you cannot display a dialog box to prompt the user.</span></span> <span data-ttu-id="99192-183">MAPI wird durch Aufrufen des Anbieters Nachricht Service Entry Point-Funktion mit MSG_SERVICE_CONFIGURE als Parameter _UlContext_ für dem Dienst selbst, entweder programmgesteuert konfigurieren kann oder Verwenden des Eigenschaftenfensters Antworten.</span><span class="sxs-lookup"><span data-stu-id="99192-183">MAPI will respond by calling your provider's message service entry point function with MSG_SERVICE_CONFIGURE set as the  _ulContext_ parameter to give the service a chance to configure itself, either programmatically or using a property sheet.</span></span> <span data-ttu-id="99192-184">Wenn die Nachricht Service Einstiegspunkt Funktion beendet wurde, MAPI, ein Wiederholungsversuch der Anmeldung.</span><span class="sxs-lookup"><span data-stu-id="99192-184">When the message service entry point function has finished, MAPI retries the logon.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="99192-185">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="99192-185">See also</span></span>



[<span data-ttu-id="99192-186">IABLogon::Logoff</span><span class="sxs-lookup"><span data-stu-id="99192-186">IABLogon::Logoff</span></span>](iablogon-logoff.md)
  
[<span data-ttu-id="99192-187">IABLogon::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="99192-187">IABLogon::OpenEntry</span></span>](iablogon-openentry.md)
  
[<span data-ttu-id="99192-188">IMAPISupport::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="99192-188">IMAPISupport::OpenProfileSection</span></span>](imapisupport-openprofilesection.md)
  
[<span data-ttu-id="99192-189">IMAPISupport::SetProviderUID</span><span class="sxs-lookup"><span data-stu-id="99192-189">IMAPISupport::SetProviderUID</span></span>](imapisupport-setprovideruid.md)
  
[<span data-ttu-id="99192-190">MSGSERVICEENTRY</span><span class="sxs-lookup"><span data-stu-id="99192-190">MSGSERVICEENTRY</span></span>](msgserviceentry.md)
  
[<span data-ttu-id="99192-191">IABProvider: IUnknown</span><span class="sxs-lookup"><span data-stu-id="99192-191">IABProvider : IUnknown</span></span>](iabprovideriunknown.md)
