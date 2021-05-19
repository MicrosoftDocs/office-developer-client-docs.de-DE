---
title: Struktur eines Nachrichtenspeicheranbieters
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 064b2fc1-e690-43e6-95d3-a61438115de5
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: eda62a4cd31e0de695d52391a6717e7a0f5ea581
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426422"
---
# <a name="structure-of-message-store-providers"></a><span data-ttu-id="dcbbd-103">Struktur eines Nachrichtenspeicheranbieters</span><span class="sxs-lookup"><span data-stu-id="dcbbd-103">Structure of message store providers</span></span>
  
<span data-ttu-id="dcbbd-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dcbbd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dcbbd-105">Ein Nachrichtenspeicheranbieter, wenn er im Arbeitsspeicher ausgeführt wird, ist eine [IMSProvider : IUnknown-Schnittstelle.](imsprovideriunknown.md)</span><span class="sxs-lookup"><span data-stu-id="dcbbd-105">A message store provider, when it is running in memory, is an [IMSProvider : IUnknown](imsprovideriunknown.md) interface.</span></span> <span data-ttu-id="dcbbd-106">Über **die IMSProvider-Schnittstelle** können sich Clientanwendungen und der MAPI-Spooler beim nachrichtenspeicher anmelden und abmelden.</span><span class="sxs-lookup"><span data-stu-id="dcbbd-106">The **IMSProvider** interface allows client applications and the MAPI spooler to log on to and off of the message store.</span></span> <span data-ttu-id="dcbbd-107">Die Schnittstellen, die Clientanwendungen und der MAPI-Spooler für den Zugriff auf Ordner und Nachrichten im Nachrichtenspeicher verwenden, sind [IMSLogon-](imslogoniunknown.md) und [IMsgStore-Schnittstellen.](imsgstoreimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="dcbbd-107">The interfaces that client applications and the MAPI spooler use to access folders and messages in the message store are [IMSLogon](imslogoniunknown.md) and [IMsgStore](imsgstoreimapiprop.md) interfaces.</span></span> <span data-ttu-id="dcbbd-108">Diese Schnittstellen werden in der Regel erstellt, wenn der Nachrichtenspeicher zum ersten Mal angemeldet ist, obwohl sie auch vom [MSProviderInit-Einstiegspunkt](msproviderinit.md) der Nachrichtenspeicher-DLL erstellt werden können.</span><span class="sxs-lookup"><span data-stu-id="dcbbd-108">These interfaces are typically created when the message store is first logged on to, although the [MSProviderInit](msproviderinit.md) entry point of the message store DLL could also create them.</span></span> 
  
<span data-ttu-id="dcbbd-109">Da die **IMSLogon-** und **IMsgStore-Schnittstellen** einige Methoden gemeinsam verwenden, ist es möglicherweise einfacher, ein Klassenobjekt zu erstellen, das von beiden Schnittstellen erbt.</span><span class="sxs-lookup"><span data-stu-id="dcbbd-109">Because the **IMSLogon** and **IMsgStore** interfaces share some methods, it may be easier to create one class object that inherits from both of these interfaces.</span></span> <span data-ttu-id="dcbbd-110">Sie können diese Schnittstellen auch in separaten Objekten implementieren und Hilfsfunktionen intern in Ihre DLL schreiben, die die gemeinsam genutzten Methoden implementieren, die dann von den Methoden in den **ImSLogon-** und **IMsgStore-Schnittstellen** aufgerufen werden können.</span><span class="sxs-lookup"><span data-stu-id="dcbbd-110">You can also implement these interfaces in separate objects, and write helper functions internal to your DLL that implement the shared methods that can then be called from the methods in the **IMSLogon** and **IMsgStore** interfaces.</span></span> 
  
<span data-ttu-id="dcbbd-111">Die folgende Abbildung zeigt eine übersichtsorientierte Gliederung der Objekthierarchie innerhalb eines ausgeführten Nachrichtenspeichers.</span><span class="sxs-lookup"><span data-stu-id="dcbbd-111">The following illustration shows a high-level outline of the object hierarchy within a running message store.</span></span>
  
<span data-ttu-id="dcbbd-112">**Objekthierarchie des Nachrichtenspeichers**</span><span class="sxs-lookup"><span data-stu-id="dcbbd-112">**Message store object hierarchy**</span></span>
  
<span data-ttu-id="dcbbd-113">![Objekthierarchie des Nachrichtenspeichers](media/storeobj.gif "Nachrichtenspeicherobjekthierarchie")</span><span class="sxs-lookup"><span data-stu-id="dcbbd-113">![Message store object hierarchy](media/storeobj.gif "Message store object hierarchy")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="dcbbd-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dcbbd-114">See also</span></span>

- [<span data-ttu-id="dcbbd-115">Entwickeln eines MAPI-Nachrichtenspeicheranbieters</span><span class="sxs-lookup"><span data-stu-id="dcbbd-115">Developing a MAPI Message Store Provider</span></span>](developing-a-mapi-message-store-provider.md)

