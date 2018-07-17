---
title: Implementieren eine Anmeldung-Objekt
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 41e5c88c-d79d-4e9f-81f4-c4365cfaa15d
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: e23c73931c9051b61d30b7ea7e9c54d06a4d9c33
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792534"
---
# <a name="implementing-a-logon-object"></a><span data-ttu-id="ff3d3-103">Implementieren eine Anmeldung-Objekt</span><span class="sxs-lookup"><span data-stu-id="ff3d3-103">Implementing a Logon Object</span></span>

  
  
<span data-ttu-id="ff3d3-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ff3d3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ff3d3-105">Jedes Adressbuch, Nachrichtenspeicher und Transport-Provider instanziiert ein Anmeldeobjekt als Teil der Implementierung der [IABProvider::Logon](iabprovider-logon.md), [IMSProvider::Logon](imsprovider-logon.md)oder [IXPProvider::TransportLogon](ixpprovider-transportlogon.md).</span><span class="sxs-lookup"><span data-stu-id="ff3d3-105">Every address book, message store, and transport provider instantiates a logon object as part of its implementation of [IABProvider::Logon](iabprovider-logon.md), [IMSProvider::Logon](imsprovider-logon.md), or [IXPProvider::TransportLogon](ixpprovider-transportlogon.md).</span></span> <span data-ttu-id="ff3d3-106">Logon-Objekten Implementieren von Methoden, mit deren Hilfe MAPI-Client Serviceanfragen.</span><span class="sxs-lookup"><span data-stu-id="ff3d3-106">Logon objects implement methods that help MAPI service client requests.</span></span> <span data-ttu-id="ff3d3-107">Je nach Typ des Dienstanbieters wird Ihr Anmeldeobjekt eine der folgenden Schnittstellen unterstützen.</span><span class="sxs-lookup"><span data-stu-id="ff3d3-107">Depending on your type of service provider, your logon object will support one of the following interfaces.</span></span> 
  
|<span data-ttu-id="ff3d3-108">**Anmeldung-Objektschnittstelle**</span><span class="sxs-lookup"><span data-stu-id="ff3d3-108">**Logon object interface**</span></span>|<span data-ttu-id="ff3d3-109">**Dienstanbieter**</span><span class="sxs-lookup"><span data-stu-id="ff3d3-109">**Service provider**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ff3d3-110">IABLogon: IUnknown</span><span class="sxs-lookup"><span data-stu-id="ff3d3-110">IABLogon : IUnknown</span></span>](iablogoniunknown.md) <br/> |<span data-ttu-id="ff3d3-111">-Adressbuchanbieter</span><span class="sxs-lookup"><span data-stu-id="ff3d3-111">Address book provider</span></span>  <br/> |
|[<span data-ttu-id="ff3d3-112">IMSLogon: IUnknown</span><span class="sxs-lookup"><span data-stu-id="ff3d3-112">IMSLogon : IUnknown</span></span>](imslogoniunknown.md) <br/> |<span data-ttu-id="ff3d3-113">Nachricht Speicheranbieter</span><span class="sxs-lookup"><span data-stu-id="ff3d3-113">Message store provider</span></span>  <br/> |
|[<span data-ttu-id="ff3d3-114">IXPLogon: IUnknown</span><span class="sxs-lookup"><span data-stu-id="ff3d3-114">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md) <br/> |<span data-ttu-id="ff3d3-115">Transportdienst</span><span class="sxs-lookup"><span data-stu-id="ff3d3-115">Transport provider</span></span>  <br/> |
   
<span data-ttu-id="ff3d3-116">Adressbuch und Meldung von nachrichtenspeicheranbietern implementierte die folgenden Features in ihrer Anmeldung Objekte:</span><span class="sxs-lookup"><span data-stu-id="ff3d3-116">Address book and message store providers implement the following features in their logon objects:</span></span>
  
- <span data-ttu-id="ff3d3-117">Unterstützung für ereignisbenachrichtigung (**Advise** und **Unadvise** -Methoden).</span><span class="sxs-lookup"><span data-stu-id="ff3d3-117">Support for event notification (**Advise** and **Unadvise** methods).</span></span> <span data-ttu-id="ff3d3-118">Eine Übersicht über ereignisbenachrichtigung finden Sie unter [Event Notification in MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="ff3d3-118">For an overview of event notification, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> <span data-ttu-id="ff3d3-119">Weitere Informationen zur Unterstützung von Benachrichtigung in Ihrer Anmeldung-Objekt finden Sie unter [Ereignisbenachrichtigung unterstützen](supporting-event-notification.md).</span><span class="sxs-lookup"><span data-stu-id="ff3d3-119">For more information about supporting notification in your logon object, see [Supporting Event Notification](supporting-event-notification.md).</span></span> 
    
- <span data-ttu-id="ff3d3-120">Vergleich der Eintrag Bezeichner **(Eintragsbezeichner)** .</span><span class="sxs-lookup"><span data-stu-id="ff3d3-120">Entry identifier comparison (**CompareEntryIDs** method).</span></span> <span data-ttu-id="ff3d3-121">Allgemeine Informationen zu Eintragsbezeichner finden Sie unter [MAPI-Eintragsbezeichner](mapi-entry-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="ff3d3-121">For general information about entry identifiers, see [MAPI Entry Identifiers](mapi-entry-identifiers.md).</span></span> <span data-ttu-id="ff3d3-122">Weitere Informationen zum Vergleichen von Eintragsbezeichner in **Ihrer Anmeldung-Objekt-Eintragsbezeichner** finden Sie unter [Vergleich und unterstützende Objektzugriff](supporting-object-access-and-comparison.md).</span><span class="sxs-lookup"><span data-stu-id="ff3d3-122">For more information about comparing entry identifiers in your logon object's **CompareEntryIDs** method, see [Supporting Object Access and Comparison](supporting-object-access-and-comparison.md).</span></span>
    
- <span data-ttu-id="ff3d3-123">Zugriff auf zusätzliche Fehlerinformationen (**GetLastError** -Methode).</span><span class="sxs-lookup"><span data-stu-id="ff3d3-123">Access to additional error information (**GetLastError** method).</span></span> <span data-ttu-id="ff3d3-124">Weitere Informationen zur Behandlung von Fehlern in MAPI finden Sie unter [Fehlerbehandlung in MAPI](error-handling-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="ff3d3-124">For more information about handling errors in MAPI, see [Error Handling in MAPI](error-handling-in-mapi.md).</span></span> 
    
- <span data-ttu-id="ff3d3-125">Zugriff auf Objekte, die vom Dienstanbieter (**OpenEntry** -Methode) implementiert.</span><span class="sxs-lookup"><span data-stu-id="ff3d3-125">Access to objects implemented by the service provider (**OpenEntry** method).</span></span> <span data-ttu-id="ff3d3-126">Weitere Informationen finden Sie unter [Vergleich und unterstützende Object Access](supporting-object-access-and-comparison.md).</span><span class="sxs-lookup"><span data-stu-id="ff3d3-126">For more information, see [Supporting Object Access and Comparison](supporting-object-access-and-comparison.md).</span></span>
    
- <span data-ttu-id="ff3d3-127">Zugriff auf ein Statusobjekt (**OpenStatusEntry** -Methode).</span><span class="sxs-lookup"><span data-stu-id="ff3d3-127">Access to a status object (**OpenStatusEntry** method).</span></span> <span data-ttu-id="ff3d3-128">Allgemeine Informationen zu Status-Objekten finden Sie unter [MAPI-Status-Objekten](mapi-status-objects.md).</span><span class="sxs-lookup"><span data-stu-id="ff3d3-128">For general information about status objects, see [MAPI Status Objects](mapi-status-objects.md).</span></span> <span data-ttu-id="ff3d3-129">Bestimmte Informationen zum Implementieren der Statusobjekt finden Sie unter [Implementierung der Status-Objekts](status-object-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="ff3d3-129">For specific information about implementing a status object, see [Status Object Implementation](status-object-implementation.md).</span></span>
    
- <span data-ttu-id="ff3d3-130">Ein Prozess der Abmeldung (**Logoff (** Methode)).</span><span class="sxs-lookup"><span data-stu-id="ff3d3-130">A logoff process (**Logoff** method).</span></span> <span data-ttu-id="ff3d3-131">Weitere Informationen finden Sie unter [Herunterfahren nach unten a Service Provider](shutting-down-a-service-provider.md).</span><span class="sxs-lookup"><span data-stu-id="ff3d3-131">For more information, see [Shutting Down a Service Provider](shutting-down-a-service-provider.md).</span></span>
    
<span data-ttu-id="ff3d3-132">Wenn der Anbieter eine Adressbuchanbieter ist, implementieren Sie die auch die folgenden Methoden und die zugehörigen Features:</span><span class="sxs-lookup"><span data-stu-id="ff3d3-132">If your provider is an address book provider, you will also implement the following methods and associated features:</span></span>
  
- <span data-ttu-id="ff3d3-133">[GetOneOffTable](iablogon-getoneofftable.md) , um eine Liste der Vorlagen bereitzustellen, die für das Erstellen von neuen Empfänger unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ff3d3-133">[IABLogon::GetOneOffTable](iablogon-getoneofftable.md) to provide a listing of the templates that you support for creating new recipients.</span></span> <span data-ttu-id="ff3d3-134">Weitere Informationen finden Sie unter [Einmaligen Tabellen](one-off-tables.md) oder [Implementieren einer einmaligen Anbieter-Tabelle](implementing-a-provider-one-off-table.md).</span><span class="sxs-lookup"><span data-stu-id="ff3d3-134">For more information, see [One-Off Tables](one-off-tables.md) or [Implementing a Provider One-Off Table](implementing-a-provider-one-off-table.md).</span></span>
    
- <span data-ttu-id="ff3d3-135">[OpenTemplateID](iablogon-opentemplateid.md) für den Zugriff auf die Implementierung eines Empfängers, dessen Daten in einer Host-Adressbuchanbieter befindet.</span><span class="sxs-lookup"><span data-stu-id="ff3d3-135">[IABLogon::OpenTemplateID](iablogon-opentemplateid.md) to provide access to the implementation of a recipient whose data resides in a host address book provider.</span></span> <span data-ttu-id="ff3d3-136">Weitere Informationen finden Sie unter [als einen fremden Adressbuchanbieter fungiert](acting-as-a-foreign-address-book-provider.md).</span><span class="sxs-lookup"><span data-stu-id="ff3d3-136">For more information, see [Acting as a Foreign Address Book Provider](acting-as-a-foreign-address-book-provider.md).</span></span> 
    
- <span data-ttu-id="ff3d3-137">[IABLogon::PrepareRecips](iablogon-preparerecips.md) , um sicherzustellen, dass die entsprechenden Eigenschaften für alle Empfänger in einer Empfängerliste verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="ff3d3-137">[IABLogon::PrepareRecips](iablogon-preparerecips.md) to ensure that the appropriate properties are available for all of the recipients in a recipient list.</span></span> <span data-ttu-id="ff3d3-138">Weitere Informationen finden Sie unter [IABLogon::PrepareRecips](iablogon-preparerecips.md).</span><span class="sxs-lookup"><span data-stu-id="ff3d3-138">For more information, see [IABLogon::PrepareRecips](iablogon-preparerecips.md).</span></span> 
    
<span data-ttu-id="ff3d3-139">Eines Transportdienstes Anmeldung-Objekt, das implementiert [IXPLogon: IUnknown](ixplogoniunknown.md), unterscheidet sich von der Logon-Objekten, die von anderen Typen der Dienstanbieter implementiert.</span><span class="sxs-lookup"><span data-stu-id="ff3d3-139">A transport provider's logon object, which implements [IXPLogon : IUnknown](ixplogoniunknown.md), is quite different from the logon objects implemented by the other types of service providers.</span></span> <span data-ttu-id="ff3d3-140">Es wurde die Anmeldung Objekte nur zwei Features: Zugriff auf ein Statusobjekt über die [IXPLogon::OpenStatusEntry](ixplogon-openstatusentry.md) -Methode und eine Abmeldung über die [IXPLogon::TransportLogoff](ixplogon-transportlogoff.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="ff3d3-140">It has only two features in common with the other logon objects: access to a status object through the [IXPLogon::OpenStatusEntry](ixplogon-openstatusentry.md) method and a logoff operation through the [IXPLogon::TransportLogoff](ixplogon-transportlogoff.md) method.</span></span> <span data-ttu-id="ff3d3-141">Transportanbieter implementieren die folgenden eindeutigen Features in ihrer Anmeldung Objekte:</span><span class="sxs-lookup"><span data-stu-id="ff3d3-141">Transport providers implement the following unique features in their logon objects:</span></span> 
  
- <span data-ttu-id="ff3d3-142">Registrierung für Adresstypen ([IXPLogon::AddressTypes](ixplogon-addresstypes.md) -Methode).</span><span class="sxs-lookup"><span data-stu-id="ff3d3-142">Registration for address types ([IXPLogon::AddressTypes](ixplogon-addresstypes.md) method).</span></span> <span data-ttu-id="ff3d3-143">Weitere Informationen zum Registrieren eines Adresstyps finden Sie unter [Adressbuchhierarchie und MAPI-Warteschlange betriebliche Modell](transport-provider-and-mapi-spooler-operational-model.md).</span><span class="sxs-lookup"><span data-stu-id="ff3d3-143">For more information about registering an address type, see [Transport Provider and MAPI Spooler Operational Model](transport-provider-and-mapi-spooler-operational-model.md).</span></span>
    
- <span data-ttu-id="ff3d3-144">Steuerung der Nachrichtenübermittlung ([IXPLogon::StartMessage](ixplogon-startmessage.md), [IXPLogon::EndMessage](ixplogon-endmessage.md)und [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) -Methoden).</span><span class="sxs-lookup"><span data-stu-id="ff3d3-144">Control of message transmission ([IXPLogon::StartMessage](ixplogon-startmessage.md), [IXPLogon::EndMessage](ixplogon-endmessage.md), and [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) methods).</span></span> <span data-ttu-id="ff3d3-145">Weitere Informationen finden Sie unter [Nachricht Empfang Modell](message-reception-model.md) [interagieren mit der MAPI-Warteschlange](interacting-with-the-mapi-spooler.md)und [Nachricht Übermittlung Modell](message-submission-model.md).</span><span class="sxs-lookup"><span data-stu-id="ff3d3-145">For more information, see [Message Reception Model](message-reception-model.md), [Interacting with the MAPI Spooler](interacting-with-the-mapi-spooler.md), and [Message Submission Model](message-submission-model.md).</span></span>
    
- <span data-ttu-id="ff3d3-146">Überprüfung der internen Zustand ([IXPLogon::ValidateState](ixplogon-validatestate.md) -Methode).</span><span class="sxs-lookup"><span data-stu-id="ff3d3-146">Internal state validation ([IXPLogon::ValidateState](ixplogon-validatestate.md) method).</span></span> 
    
- <span data-ttu-id="ff3d3-147">Möglichkeit zum Herunterladen und Hochladen von Nachrichten bei Bedarf ([IXPLogon::FlushQueues](ixplogon-flushqueues.md) -Methode).</span><span class="sxs-lookup"><span data-stu-id="ff3d3-147">Ability to download or upload messages on demand ([IXPLogon::FlushQueues](ixplogon-flushqueues.md) method).</span></span> <span data-ttu-id="ff3d3-148">Weitere Informationen finden Sie unter [Implementieren der FlushQueues-Methode](implementing-the-flushqueues-method.md).</span><span class="sxs-lookup"><span data-stu-id="ff3d3-148">For more information, see [Implementing the FlushQueues Method](implementing-the-flushqueues-method.md).</span></span>
    
- <span data-ttu-id="ff3d3-149">Die Möglichkeit, die Abfrage für ausstehende Nachrichten ([IXPLogon::Poll](ixplogon-poll.md) -Methode).</span><span class="sxs-lookup"><span data-stu-id="ff3d3-149">Ability to query for pending messages ([IXPLogon::Poll](ixplogon-poll.md) method).</span></span> <span data-ttu-id="ff3d3-150">Weitere Informationen finden Sie unter [Message Empfang Model](message-reception-model.md).</span><span class="sxs-lookup"><span data-stu-id="ff3d3-150">For more information, see [Message Reception Model](message-reception-model.md).</span></span>
    
- <span data-ttu-id="ff3d3-151">Leerlauf Erkennung ([IXPLogon::Idle](ixplogon-idle.md) -Methode).</span><span class="sxs-lookup"><span data-stu-id="ff3d3-151">Idle state detection ([IXPLogon::Idle](ixplogon-idle.md) method).</span></span> 
    
- <span data-ttu-id="ff3d3-152">Interaktion mit der MAPI-Warteschlange ([IXPLogon::TransportNotify](ixplogon-transportnotify.md) -Methode).</span><span class="sxs-lookup"><span data-stu-id="ff3d3-152">Interaction with the MAPI spooler ([IXPLogon::TransportNotify](ixplogon-transportnotify.md) method).</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="ff3d3-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ff3d3-153">See also</span></span>



[<span data-ttu-id="ff3d3-154">Implementieren von Service Provider Anmeldung</span><span class="sxs-lookup"><span data-stu-id="ff3d3-154">Implementing Service Provider Logon</span></span>](implementing-service-provider-logon.md)
