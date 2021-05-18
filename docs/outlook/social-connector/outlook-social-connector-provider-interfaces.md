---
title: Outlook Schnittstellen für Anbieter für soziale Netzwerke
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8f92b2c7-9f47-4c84-874b-fec1a2a5b555
description: Der Outlook Social Connector (OSC) ist ein Office-Feature, das von Office-Clientanwendungen gemeinsam genutzt wird und verbindungen mit sozialen und geschäftlichen Netzwerken herstellt, sodass Benutzer mit den Personen in ihren Netzwerken in Kontakt bleiben können, ohne Office.
ms.openlocfilehash: 77759db34f63239473e0682cfaca720860e96768
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422810"
---
# <a name="outlook-social-connector-provider-interfaces"></a><span data-ttu-id="78082-103">Outlook Schnittstellen für Anbieter für soziale Netzwerke</span><span class="sxs-lookup"><span data-stu-id="78082-103">Outlook Social Connector provider interfaces</span></span>

<span data-ttu-id="78082-104">Der Outlook Social Connector (OSC) ist ein Office-Feature, das von Office-Clientanwendungen gemeinsam genutzt wird und verbindungen mit sozialen und geschäftlichen Netzwerken herstellt, sodass Benutzer mit den Personen in ihren Netzwerken in Kontakt bleiben können, ohne Office.</span><span class="sxs-lookup"><span data-stu-id="78082-104">The Outlook Social Connector (OSC) is an Office feature shared by Office client applications that connects to social and business networks so users can stay in touch with the people in their networks without leaving Office.</span></span> 
  
<span data-ttu-id="78082-105">Ein OSC-Anbieter ist eine COM-DLL (Component Object Model), mit der das OSC unabhängig von den APIs der einzelnen sozialen Netzwerke auf Daten in sozialen Netzwerken zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="78082-105">An OSC provider is a Component Object Model (COM) DLL that allows the OSC to access social network data in a way that is independent of the APIs of each social network.</span></span> <span data-ttu-id="78082-106">In der folgenden Tabelle sind die Schnittstellen in der Erweiterbarkeit des OSC-Anbieters aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="78082-106">The following table lists the interfaces in OSC provider extensibility.</span></span> <span data-ttu-id="78082-107">Ein OSC-Anbieter muss vier der fünf Schnittstellen implementieren, um mit dem OSC zu kommunizieren: [ISocialPerson](isocialpersoniunknown.md), [ISocialProfile](isocialprofileisocialperson.md), [ISocialProvider](isocialprovideriunknown.md)und [ISocialSession](isocialsessioniunknown.md).</span><span class="sxs-lookup"><span data-stu-id="78082-107">An OSC provider must implement four of the five interfaces to communicate with the OSC: [ISocialPerson](isocialpersoniunknown.md), [ISocialProfile](isocialprofileisocialperson.md), [ISocialProvider](isocialprovideriunknown.md), and [ISocialSession](isocialsessioniunknown.md).</span></span> <span data-ttu-id="78082-108">Wenn der OSC-Anbieter die Synchronisierung von Aktivitäten, die On-Demand- oder Hybridsynchronisierung von Freunden, das Zwischenspeichern von Anmeldeinformationen und die Anmeldung mithilfe zwischengespeicherter Anmeldeinformationen oder die Möglichkeit unterstützt, einer Person zu folgen, sollte der Anbieter [auch ISocialSession2](isocialsession2iunknown.md)implementieren.</span><span class="sxs-lookup"><span data-stu-id="78082-108">If the OSC provider supports synchronizing activities, on-demand or hybrid synchronization of friends, caching logon credentials and logging on using cached credentials, or the ability to follow a person, the provider should implement [ISocialSession2](isocialsession2iunknown.md), as well.</span></span>
  
|<span data-ttu-id="78082-109">**Name**</span><span class="sxs-lookup"><span data-stu-id="78082-109">**Name**</span></span>|<span data-ttu-id="78082-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="78082-110">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="78082-111">ISocialPerson</span><span class="sxs-lookup"><span data-stu-id="78082-111">ISocialPerson</span></span>](isocialpersoniunknown.md) <br/> |<span data-ttu-id="78082-112">Stellt eine Person im sozialen Netzwerk dar.</span><span class="sxs-lookup"><span data-stu-id="78082-112">Represents a person on the social network.</span></span>  <br/> |
|[<span data-ttu-id="78082-113">ISocialProfile</span><span class="sxs-lookup"><span data-stu-id="78082-113">ISocialProfile</span></span>](isocialprofileisocialperson.md) <br/> |<span data-ttu-id="78082-114">Stellt den angemeldeten Benutzer dar.</span><span class="sxs-lookup"><span data-stu-id="78082-114">Represents the logged-on user.</span></span>  <br/> |
|[<span data-ttu-id="78082-115">ISocialProvider</span><span class="sxs-lookup"><span data-stu-id="78082-115">ISocialProvider</span></span>](isocialprovideriunknown.md) <br/> |<span data-ttu-id="78082-116">Stellt eine Instanz eines OSC-Anbieters dar.</span><span class="sxs-lookup"><span data-stu-id="78082-116">Represents an instance of an OSC provider.</span></span>  <br/> |
|[<span data-ttu-id="78082-117">ISocialSession</span><span class="sxs-lookup"><span data-stu-id="78082-117">ISocialSession</span></span>](isocialsessioniunknown.md) <br/> |<span data-ttu-id="78082-118">Stellt eine Verbindung mit einem Standort für soziale Netzwerke dar.</span><span class="sxs-lookup"><span data-stu-id="78082-118">Represents a connection to a social network site.</span></span>  <br/> |
|[<span data-ttu-id="78082-119">ISocialSession2</span><span class="sxs-lookup"><span data-stu-id="78082-119">ISocialSession2</span></span>](isocialsession2iunknown.md) <br/> |<span data-ttu-id="78082-120">Unterstützt das Synchronisieren von Aktivitäten, das Hinzufügen von Freunden, die On-Demand- oder Hybridsynchronisierung von Freunden oder die Anmeldung beim sozialen Netzwerk mithilfe zwischengespeicherter Anmeldeinformationen.</span><span class="sxs-lookup"><span data-stu-id="78082-120">Supports synchronizing activities, adding friends, on-demand or hybrid synchronization of friends, or logging on to the social network by using cached credentials.</span></span>  <br/> |
   

