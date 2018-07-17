---
title: Typen der Transportanbieter
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 772ecab1-7e91-415b-bae8-af8ffb7b7ed9
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 4a0ab660b8df2fb32f21f9bc93932a9187c37b7b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795767"
---
# <a name="types-of-transport-providers"></a><span data-ttu-id="10c82-103">Typen der Transportanbieter</span><span class="sxs-lookup"><span data-stu-id="10c82-103">Types of Transport Providers</span></span>

  
  
<span data-ttu-id="10c82-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="10c82-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="10c82-105">Alle Transportanbieter für unterstützen einen Bereich von Standardfeatures, z. B.:</span><span class="sxs-lookup"><span data-stu-id="10c82-105">All transport providers support a range of standard features, such as:</span></span>
  
- <span data-ttu-id="10c82-106">Bereitstellen von ordnungsgemäße Sicherheit für die zugrunde liegenden messaging-System.</span><span class="sxs-lookup"><span data-stu-id="10c82-106">Providing proper security for the underlying messaging system.</span></span>
    
- <span data-ttu-id="10c82-107">Senden und Empfangen von Nachrichten aus dem zugrunde liegenden messaging-System.</span><span class="sxs-lookup"><span data-stu-id="10c82-107">Sending and receiving messages from the underlying messaging system.</span></span>
    
- <span data-ttu-id="10c82-108">Verfügbarmachen der Adresstypen unterstützen die Transportanbieter, damit der MAPI-Warteschlange und Clientanwendungen entsprechend verwendet können.</span><span class="sxs-lookup"><span data-stu-id="10c82-108">Exposing the address types the transport providers support so the MAPI spooler and client applications can use them appropriately.</span></span>
    
- <span data-ttu-id="10c82-109">Akzeptieren von Übermittlung für bestimmte Empfänger.</span><span class="sxs-lookup"><span data-stu-id="10c82-109">Accepting delivery for specific recipients.</span></span>
    
<span data-ttu-id="10c82-110">MAPI unterstützt darüber hinaus zwei spezielle Arten von Anbietern für bestimmte messaging-Systeme.</span><span class="sxs-lookup"><span data-stu-id="10c82-110">In addition, MAPI supports two specialized types of providers for specific messaging systems.</span></span>
  
|<span data-ttu-id="10c82-111">**Transporttyp**</span><span class="sxs-lookup"><span data-stu-id="10c82-111">**Transport type**</span></span>|<span data-ttu-id="10c82-112">**Zusätzliche Funktionalität**</span><span class="sxs-lookup"><span data-stu-id="10c82-112">**Added functionality**</span></span>|
|:-----|:-----|
|<span data-ttu-id="10c82-113">Remote-Transport</span><span class="sxs-lookup"><span data-stu-id="10c82-113">Remote Transport</span></span>  <br/> |<span data-ttu-id="10c82-114">Ermöglicht die Interoperabilität mit Clients Remote verbunden.</span><span class="sxs-lookup"><span data-stu-id="10c82-114">Enables interoperability with clients connected remotely.</span></span>  <br/> |
|<span data-ttu-id="10c82-115">TNEF-Transport</span><span class="sxs-lookup"><span data-stu-id="10c82-115">TNEF Transport</span></span>  <br/> |<span data-ttu-id="10c82-116">MAPI-Eigenschaften auf die messaging-Systeme, die diese nicht unterstützen beibehalten werden können.</span><span class="sxs-lookup"><span data-stu-id="10c82-116">Allows MAPI properties to be preserved on messaging systems that do not support them.</span></span>  <br/> |
   
<span data-ttu-id="10c82-117">TNEF Transporten dienen zum Übersetzen von Nachrichten zwischen messaging-Systemen, die verschiedene Sätze von MAPI-Eigenschaften zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="10c82-117">TNEF transports are used for translating messages between messaging systems that support different sets of MAPI properties.</span></span> <span data-ttu-id="10c82-118">TNEF Transporten verwenden Sie die MAPI [ITnef: IUnknown](itnefiunknown.md) -Schnittstelle für alle Eigenschaften, die das Zielsystem darstellen kann nicht direkt in einem binären Datenstrom zu konvertieren, die an die Nachricht angefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="10c82-118">TNEF transports use the MAPI [ITnef : IUnknown](itnefiunknown.md) interface to convert any properties that the destination system cannot represent directly into a binary data stream that can be attached to the message.</span></span> <span data-ttu-id="10c82-119">Eine andere TNEF Transport kann später **ITnef** verwenden, um den Datenstrom decodieren und die ursprünglichen MAPI-Eigenschaften-Clientanwendungen zur Verfügung stellen.</span><span class="sxs-lookup"><span data-stu-id="10c82-119">Later, another TNEF transport can use **ITnef** to decode the data stream and make the original MAPI properties available to client applications.</span></span> <span data-ttu-id="10c82-120">Darüber hinaus ist die TNEF-Unterstützung erforderlich, wenn Ihre Transport benutzerdefinierte Nachrichtenklassen unterstützen muss.</span><span class="sxs-lookup"><span data-stu-id="10c82-120">Additionally, TNEF support is required if your transport needs to support custom message classes.</span></span> <span data-ttu-id="10c82-121">Informationen zum Implementieren von TNEF Transporten finden Sie unter [Developing eines Transportdienstes TNEF-Enabled](developing-a-tnef-enabled-transport-provider.md).</span><span class="sxs-lookup"><span data-stu-id="10c82-121">For information about implementing TNEF transports, see [Developing a TNEF-Enabled Transport Provider](developing-a-tnef-enabled-transport-provider.md).</span></span>
  
<span data-ttu-id="10c82-122">Wenn Ihre Adressbuchhierarchie nicht dieser Typen ist, müssen Sie mit den grundlegenden MAPI-Funktionen und Netzwerkfunktionen der Zielplattform verfügbar zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="10c82-122">If your transport provider is not one of these types, you will have to implement it with the basic MAPI functions and networking functions available on your target platform.</span></span>
  
