---
title: Standardauthentifizierung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 89349d1e-365a-442e-9ba3-2df601d9323c
description: Der Outlook Social Connector (OSC) ruft die ISocialProvider::GetCapabilities-Methode auf, um die Funktionen des OSC-Anbieters für ein soziales Netzwerk zu ermitteln.
ms.openlocfilehash: 7f716df3ef2e82712374ce3d775cdf66eb07e8b3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439926"
---
# <a name="basic-authentication"></a><span data-ttu-id="0b0ee-103">Standardauthentifizierung</span><span class="sxs-lookup"><span data-stu-id="0b0ee-103">Basic authentication</span></span>

<span data-ttu-id="0b0ee-104">Das Outlook Social Connector (OSC) ruft die [ISocialProvider::GetCapabilities-Methode](isocialprovider-getcapabilities.md) auf, um die Funktionen des OSC-Anbieters für ein soziales Netzwerk zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="0b0ee-104">The Outlook Social Connector (OSC) calls the [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method to determine the capabilities of the OSC provider for a social network.</span></span> <span data-ttu-id="0b0ee-105">Das OSC verwendet die zurückgegebenen Funktionen, um zu bestimmen, wie ein benutzer Office, der sich bei diesem sozialen Netzwerk anmeldet.</span><span class="sxs-lookup"><span data-stu-id="0b0ee-105">The OSC uses the returned capabilities to determine how to support an Office user who is logging on to this social network.</span></span> <span data-ttu-id="0b0ee-106">Wenn das **useLogonWebAuth-Element**  im zurückgegebenen Funktionen-XML angibt, dass der OSC-Anbieter die Standardauthentifizierung unterstützt, kann das OSC die folgende Aufrufsequenz erstellen, damit sich ein Benutzer bei diesem sozialen Netzwerk anmelden kann:</span><span class="sxs-lookup"><span data-stu-id="0b0ee-106">If the **useLogonWebAuth** element in the returned **capabilities** XML indicates that the OSC provider supports basic authentication, the OSC can make the following calling sequence to allow a user to log on to that social network:</span></span> 
  
1. <span data-ttu-id="0b0ee-107">[ISocialProvider::Load](isocialprovider-load.md) – Das Betriebssystem lädt den Anbieter.</span><span class="sxs-lookup"><span data-stu-id="0b0ee-107">[ISocialProvider::Load](isocialprovider-load.md) —The OSC loads the provider.</span></span> 
    
2. <span data-ttu-id="0b0ee-108">[ISocialProvider::Version](isocialprovider-version.md) – Das OSC ruft eine Zeichenfolge ab, die die Versionsnummer des OSC-Anbieters darstellt.</span><span class="sxs-lookup"><span data-stu-id="0b0ee-108">[ISocialProvider::Version](isocialprovider-version.md) —The OSC gets a string that represents the version number of the OSC provider.</span></span> 
    
3. <span data-ttu-id="0b0ee-109">[ISocialProvider::SocialNetworkName](isocialprovider-socialnetworkname.md) – Das OSC ruft eine Zeichenfolge ab, die den Namen des sozialen Netzwerks darstellt.</span><span class="sxs-lookup"><span data-stu-id="0b0ee-109">[ISocialProvider::SocialNetworkName](isocialprovider-socialnetworkname.md) —The OSC gets a string that represents the social network name.</span></span> 
    
4. <span data-ttu-id="0b0ee-110">[ISocialProvider::SocialNetworkGuid](isocialprovider-socialnetworkguid.md) – Das OSC ruft eine unveränderliche GUID ab, die das soziale Netzwerk darstellt.</span><span class="sxs-lookup"><span data-stu-id="0b0ee-110">[ISocialProvider::SocialNetworkGuid](isocialprovider-socialnetworkguid.md) —The OSC gets an immutable GUID that represents the social network.</span></span> 
    
5. <span data-ttu-id="0b0ee-111">[ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) – Das OSC ruft eine Zeichenfolge ab, die die Funktionen des Anbieters darstellt und die der Schemadefinition für das **Capabilities-Element** entspricht.</span><span class="sxs-lookup"><span data-stu-id="0b0ee-111">[ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) —The OSC gets a string that represents the provider's capabilities and that complies with the schema definition for the **capabilities** element.</span></span> 
    
6. <span data-ttu-id="0b0ee-112">[ISocialProvider::SocialNetworkIcon](isocialprovider-socialnetworkicon.md) – Das OSC ruft ein Bytearray ab, das das Symbol für die Website des sozialen Netzwerks darstellt.</span><span class="sxs-lookup"><span data-stu-id="0b0ee-112">[ISocialProvider::SocialNetworkIcon](isocialprovider-socialnetworkicon.md) —The OSC gets a byte array that represents the icon for the social network site.</span></span> 
    
7. <span data-ttu-id="0b0ee-113">[ISocialProvider::GetSession](isocialprovider-getsession.md) – Das OSC ruft eine [ISocialSession-Schnittstelle](isocialsessioniunknown.md) ab.</span><span class="sxs-lookup"><span data-stu-id="0b0ee-113">[ISocialProvider::GetSession](isocialprovider-getsession.md) —The OSC gets an [ISocialSession](isocialsessioniunknown.md) interface.</span></span> 
    
8. <span data-ttu-id="0b0ee-114">[ISocialSession::Logon](isocialsession-logon.md) – Das Betriebssystem meldet den Benutzer mithilfe des angegebenen Benutzernamens und Kennworts am Standort des sozialen Netzwerks an.</span><span class="sxs-lookup"><span data-stu-id="0b0ee-114">[ISocialSession::Logon](isocialsession-logon.md) —The OSC logs the user on to the social network site by using the specified user name and password.</span></span> 
    
9. <span data-ttu-id="0b0ee-115">[ISocialSession::GetLoggedOnUser](isocialsession-getloggedonuser.md) – Das OSC ruft eine [ISocialProfile-Schnittstelle](isocialprovideriunknown.md) ab, die den angemeldeten Benutzer darstellt.</span><span class="sxs-lookup"><span data-stu-id="0b0ee-115">[ISocialSession::GetLoggedOnUser](isocialsession-getloggedonuser.md) —The OSC gets an [ISocialProfile](isocialprovideriunknown.md) interface that represents the logged-on user.</span></span> 
    
10. <span data-ttu-id="0b0ee-116">[ISocialSession::GetNetworkIdentifier](isocialsession-getnetworkidentifier.md) – Das OSC ruft eine Zeichenfolge ab, die einen eindeutigen Bezeichner für einen Standort im sozialen Netzwerk darstellt.</span><span class="sxs-lookup"><span data-stu-id="0b0ee-116">[ISocialSession::GetNetworkIdentifier](isocialsession-getnetworkidentifier.md) —The OSC gets a string that represents a unique identifier for a social network site.</span></span> <span data-ttu-id="0b0ee-117">Der Netzwerkbezeichner kann dem Netzwerknamen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="0b0ee-117">The network identifier can be equivalent to the network name.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="0b0ee-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0b0ee-118">See also</span></span>

- [<span data-ttu-id="0b0ee-119">XML für Funktionen</span><span class="sxs-lookup"><span data-stu-id="0b0ee-119">XML for Capabilities</span></span>](xml-for-capabilities.md)
- [<span data-ttu-id="0b0ee-120">OSC - Typische Aufrufsequenzen</span><span class="sxs-lookup"><span data-stu-id="0b0ee-120">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)

