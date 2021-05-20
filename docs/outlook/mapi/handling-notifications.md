---
title: Behandeln von Benachrichtigungen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 451b71da-a888-4d8f-9814-12f9f846de05
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: e261b71a8e94d9db3b1b17168d84798dfe18955d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429159"
---
# <a name="handling-notifications"></a><span data-ttu-id="397d6-103">Behandeln von Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="397d6-103">Handling notifications</span></span>

<span data-ttu-id="397d6-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="397d6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="397d6-105">Benachrichtigungen ermöglichen es einem Objekt, ein anderes Objekt darüber zu informieren, dass es einer Änderung unterzogen wurde.</span><span class="sxs-lookup"><span data-stu-id="397d6-105">Notifications enable one object to inform another object that it has undergone a change.</span></span> <span data-ttu-id="397d6-106">Der Änderungstyp wird als Ereignis bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="397d6-106">The type of change is referred to as an event.</span></span> <span data-ttu-id="397d6-107">MAPI definiert mehrere Ereignisse, für die Benachrichtigungen generiert werden.</span><span class="sxs-lookup"><span data-stu-id="397d6-107">MAPI defines several events for which notifications are generated.</span></span> 
  
<span data-ttu-id="397d6-108">Clients registrieren sich in der Regel für ein oder mehrere Ereignisse mit einem oder mehreren Objekten.</span><span class="sxs-lookup"><span data-stu-id="397d6-108">Clients typically register for one or more events with one or more objects.</span></span> <span data-ttu-id="397d6-109">Diese Objekte werden als Ratenquellen bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="397d6-109">These objects are referred to as advise sources.</span></span> <span data-ttu-id="397d6-110">Zu den Objekten, die als Ratgeberquellen fungieren können, gehören das Sitzungsobjekt unter mapI-Steuerelement oder ein von einem Dienstanbieter erstelltes Objekt, z. B. eine Nachricht.</span><span class="sxs-lookup"><span data-stu-id="397d6-110">Objects that can act as advise sources include the session object, under MAPI's control, or an object created by a service provider, such as a message.</span></span> <span data-ttu-id="397d6-111">Das informierte Objekt, das als "Advise Sink" bezeichnet wird, enthält entweder eine Implementierung der [IMAPIAdviseSink : IUnknown-Schnittstelle](imapiadvisesinkiunknown.md) oder die [IMAPIViewAdviseSink : IUnknown-Schnittstelle](imapiviewadvisesinkiunknown.md) und befindet sich innerhalb einer Clientanwendung.</span><span class="sxs-lookup"><span data-stu-id="397d6-111">The informed object, referred to as the advise sink, contains either an implementation of the [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md) interface or the [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md) interface and is within a client application.</span></span> 
  
<span data-ttu-id="397d6-112">Advise-Quellobjekte implementieren eine **Advise-Methode,** die von Clients aufgerufen wird, um sich für Benachrichtigungen zu registrieren, und eine **Unadvise-Methode,** die aufgerufen wird, um eine Registrierung abbricht.</span><span class="sxs-lookup"><span data-stu-id="397d6-112">Advise source objects implement an **Advise** method, which is called by clients to register for notifications, and an **Unadvise** method, which is called to cancel a registration.</span></span> <span data-ttu-id="397d6-113">Einer der zu empfehlenden Parameter **ist** ein Zeiger auf eine Implementierung von **IMAPIAdviseSink** oder \*\* IMAPIViewAdviseSink \*\*.</span><span class="sxs-lookup"><span data-stu-id="397d6-113">One of the parameters to **Advise** is a pointer to an implementation of **IMAPIAdviseSink** or \*\* IMAPIViewAdviseSink \*\*.</span></span> <span data-ttu-id="397d6-114">Die Advise-Quelle speichert diesen Zeiger zwischen, sodass er [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) oder eine der Methoden in **IMAPIViewAdviseSink** aufrufen kann, wenn eine Änderung auftritt.</span><span class="sxs-lookup"><span data-stu-id="397d6-114">The advise source caches this pointer so that it can call [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) or one of the methods in **IMAPIViewAdviseSink** when a change occurs.</span></span> 
  
<span data-ttu-id="397d6-115">Da benutzer beim Empfangen von Benachrichtigungen die neuesten Informationen anzeigen können, wird empfohlen, dass sich alle Clients für Benachrichtigungen registrieren und diese behandeln.</span><span class="sxs-lookup"><span data-stu-id="397d6-115">Because receiving notifications enables users to view the most up-to-date information, it is recommended that all clients register for and handle notifications.</span></span> <span data-ttu-id="397d6-116">Sie ist jedoch optional.</span><span class="sxs-lookup"><span data-stu-id="397d6-116">However, it is optional.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="397d6-117">Inhalt dieses Abschnitts</span><span class="sxs-lookup"><span data-stu-id="397d6-117">In this section</span></span>

- <span data-ttu-id="397d6-118">[Registrieren für eine Benachrichtigung](registering-for-a-notification.md): Beschreibt, wie ein Client für Benachrichtigungen als Teil des Initialisierungsprozesses registriert wird.</span><span class="sxs-lookup"><span data-stu-id="397d6-118">[Registering for a Notification](registering-for-a-notification.md): Describes how to register a client for notifications as a part of its initialization process.</span></span>
    
- <span data-ttu-id="397d6-119">[Abbrechen einer Benachrichtigung](canceling-a-notification.md): Beschreibt, wie Sie ein Abonnement für eine Benachrichtigung kündigen.</span><span class="sxs-lookup"><span data-stu-id="397d6-119">[Canceling a Notification](canceling-a-notification.md): Describes how to cancel a subscription to a notification.</span></span>
    
- <span data-ttu-id="397d6-120">[Handling Message Store Notification](handling-message-store-notification.md): Beschreibt, wie Sie sich für Nachrichtenspeicherbenachrichtigungen registrieren.</span><span class="sxs-lookup"><span data-stu-id="397d6-120">[Handling Message Store Notification](handling-message-store-notification.md): Describes how to register for message store notifications.</span></span>
    
- <span data-ttu-id="397d6-121">[Benachrichtigung über das Handhandbuch:](handing-address-book-notification.md)Beschreibt, wie Adressbuchbenachrichtigungen registriert und behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="397d6-121">[Handing Address Book Notification](handing-address-book-notification.md): Describes how to register for and handle address book notifications.</span></span>
    
- <span data-ttu-id="397d6-122">[Behandeln von Tabellenbenachrichtigungen](handling-table-notification.md): Beschreibt, wie Sie sich für Benachrichtigungen aus der Hierarchietabelle registrieren.</span><span class="sxs-lookup"><span data-stu-id="397d6-122">[Handling Table Notification](handling-table-notification.md): Describes how to register for notifications from the hierarchy table.</span></span>
    
- <span data-ttu-id="397d6-123">[Implementieren eines Advise Sink-Objekts:](implementing-an-advise-sink-object.md)Beschreibt die Implementierung eines Advise Sink-Objekts.</span><span class="sxs-lookup"><span data-stu-id="397d6-123">[Implementing an Advise Sink Object](implementing-an-advise-sink-object.md): Describes how to implement an advise sink object.</span></span>
    
- <span data-ttu-id="397d6-124">[Timing a Notification](timing-a-notification.md): Beschreibt den Zeitpunkt der Clientbenachrichtigung durch Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="397d6-124">[Timing a Notification](timing-a-notification.md): Describes the timing of client notification by service providers.</span></span>
    
- <span data-ttu-id="397d6-125">[Sicherstellen einer Thread-Safe Benachrichtigung](ensuring-a-thread-safe-notification.md): Beschreibt, wie Sie threadsichere Benachrichtigungen mit MAPI sicherstellen.</span><span class="sxs-lookup"><span data-stu-id="397d6-125">[Ensuring a Thread-Safe Notification](ensuring-a-thread-safe-notification.md): Describes how to ensure thread-safe notification with MAPI.</span></span>
    
- <span data-ttu-id="397d6-126">[Erzwingen einer Benachrichtigung](forcing-a-notification.md): Beschreibt, wie Sie eine Benachrichtigung in MAPI erzwingen.</span><span class="sxs-lookup"><span data-stu-id="397d6-126">[Forcing a Notification](forcing-a-notification.md): Describes how to force a notification in MAPI.</span></span>
    

