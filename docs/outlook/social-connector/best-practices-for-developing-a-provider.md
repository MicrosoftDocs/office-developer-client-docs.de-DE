---
title: Bewährte Methoden für die Entwicklung eines Anbieters
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 22e3de8a-c4f2-41a4-a5b1-c5b1bf06f724
description: 'Beachten Sie die folgenden Methoden, wenn Sie einen Outlook Social Connector 2013 (OSC) entwickeln:'
ms.openlocfilehash: 6a48a56d8065fb9a176ca6527340c99551cdb52a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425918"
---
# <a name="best-practices-for-developing-a-provider"></a><span data-ttu-id="2efca-103">Bewährte Methoden für die Entwicklung eines Anbieters</span><span class="sxs-lookup"><span data-stu-id="2efca-103">Best practices for developing a provider</span></span>

<span data-ttu-id="2efca-104">Beachten Sie die folgenden Methoden, wenn Sie einen Outlook Social Connector 2013 (OSC) entwickeln:</span><span class="sxs-lookup"><span data-stu-id="2efca-104">You should adhere to the following practices when you develop an Outlook Social Connector 2013 (OSC) provider:</span></span>
  
- <span data-ttu-id="2efca-105">Aus Sicherheitsgründen sollten Anbieter, die mit Servern über das Internet kommunizieren, das HTTPS -Protokoll (Hypertext Transfer Protocol, HTTP) mit SSL (Secure Socket Layer) verwenden.</span><span class="sxs-lookup"><span data-stu-id="2efca-105">For security reasons, providers that communicate with servers over the Internet should use the HTTPS (Hypertext Transfer Protocol (HTTP) with Secure Socket Layer (SSL)) protocol.</span></span> <span data-ttu-id="2efca-106">Andernfalls besteht das Risiko, dass E-Mail-Adressen, Aktivitäten in sozialen Netzwerken und andere Benutzerdaten während der Übertragung abgefangen oder verfügbar gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="2efca-106">Otherwise, there is a risk that email addresses, social network activities, and other user data could be intercepted or exposed while in transit.</span></span>
    
- <span data-ttu-id="2efca-107">Wenn Sie einen OSC-Anbieter für ein soziales Netzwerk eines Drittanbieters entwickeln, muss ihr Anbieter die Nutzungsbedingungen des sozialen Netzwerks einhalten.</span><span class="sxs-lookup"><span data-stu-id="2efca-107">If you are developing an OSC provider for a third-party social network, your provider must adhere to the social network's terms of service.</span></span>
    
- <span data-ttu-id="2efca-108">Um die Größe des Anbieterdownloadpakets zu minimieren, erstellen Sie den Anbieter mithilfe eines systemeigenen Compilers wie C++ oder eines anderen Tools, das eine #A0 erstellen kann.</span><span class="sxs-lookup"><span data-stu-id="2efca-108">To minimize the size of the provider download package, build the provider by using a native compiler such as C++ or any other tool that can build a COM component.</span></span>
    
- <span data-ttu-id="2efca-109">Erstellen Sie in Ihrem Anbieter einen eindeutigen Benutzer-Agent, der an das soziale Netzwerk gesendet wird, um Anrufe des Anbieters an das soziale Netzwerk zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="2efca-109">In your provider, create a unique user agent that is sent to the social network to track calls made by the provider to the social network.</span></span>
    
- <span data-ttu-id="2efca-110">Die [ISocialProvider::GetCapabilities-Methode](isocialprovider-getcapabilities.md) sollte nicht auf das Aufrufen des sozialen Netzwerks über das Internet angewiesen sein, um die Funktionen des Anbieters zu nutzen.</span><span class="sxs-lookup"><span data-stu-id="2efca-110">The [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method should not rely on calling the social network over the Internet to get the capabilities of the provider.</span></span> <span data-ttu-id="2efca-111">Benutzer können z. B. offline Outlook starten. Wenn das OSC **GetCapabilities** aufruft und keine Netzwerkverbindung besteht, gibt **der GetCapabilities-Aufruf** keinen gültigen **Funktionen-XML-Code** zurück.</span><span class="sxs-lookup"><span data-stu-id="2efca-111">For example, users can start Outlook offline; if the OSC calls **GetCapabilities** and there is no network connection, the **GetCapabilities** call will not return valid **capabilities** XML.</span></span> <span data-ttu-id="2efca-112">Die bewährte Methode besteht in der Speicherung von **Funktionen von** XML als Ressource in Ihrem Anbieter.</span><span class="sxs-lookup"><span data-stu-id="2efca-112">The best practice is to store **capabilities** XML as a resource in your provider.</span></span> 
    
- <span data-ttu-id="2efca-113">Ihr OSC-Anbieter kann eine große Anzahl von Anrufen an ein soziales Netzwerk generieren.</span><span class="sxs-lookup"><span data-stu-id="2efca-113">Your OSC provider can generate a significant volume of calls to a social network.</span></span> <span data-ttu-id="2efca-114">In Abhängigkeit von den Nutzungsbedingungen für Ihr soziales Netzwerk sollten Sie die Zwischenspeicherung von Freunden in einem Outlook-Ordner in Betracht ziehen, um die Anzahl der Anrufe vom OSC an Ihren Anbieter und wiederum von Ihrem Anbieter an das soziale Netzwerk zu reduzieren.</span><span class="sxs-lookup"><span data-stu-id="2efca-114">Depending on the terms of service for your social network, consider caching friends to an Outlook folder to reduce the number of calls from the OSC to your provider and, in turn, from your provider to the social network.</span></span>
    
- <span data-ttu-id="2efca-115">Office 2013 ist sowohl in 32-Bit- als auch in 64-Bit-Versionen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2efca-115">Office 2013 is available in both 32-bit and 64-bit versions.</span></span> <span data-ttu-id="2efca-116">Versionen von Office vor Office 2010 sind nur in einer 32-Bit-Version verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2efca-116">Versions of Office prior to Office 2010 are available only in a 32-bit version.</span></span> <span data-ttu-id="2efca-117">Die Standardinstallation von Office 2013 auf 64-Bit-Windows ist 32-Bit.</span><span class="sxs-lookup"><span data-stu-id="2efca-117">The default installation of Office 2013 on 64-bit Windows is 32-bit.</span></span> <span data-ttu-id="2efca-118">Wenn Sie die 64-Bit-Version des Betriebssystems unterstützen möchten, die mit 64-Bit Office 2013 installiert ist, müssen Sie auch eine 64-Bit-Version Ihres Anbieters veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="2efca-118">If you intend to support the 64-bit version of the OSC that is installed with 64-bit Office 2013, you must also release a 64-bit version of your provider.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="2efca-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2efca-119">See also</span></span>

- [<span data-ttu-id="2efca-120">OSC - Typische Aufrufsequenzen</span><span class="sxs-lookup"><span data-stu-id="2efca-120">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)  
- [<span data-ttu-id="2efca-121">Entwickeln eines Providers mit dem OSC-XML-Schema</span><span class="sxs-lookup"><span data-stu-id="2efca-121">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)  
- [<span data-ttu-id="2efca-122">Bereitstellen eines Providers</span><span class="sxs-lookup"><span data-stu-id="2efca-122">Deploying a Provider</span></span>](deploying-a-provider.md)  
- [<span data-ttu-id="2efca-123">Erste Schritte zum Entwickeln eines Outlook Connector Providers für soziale Netzwerke</span><span class="sxs-lookup"><span data-stu-id="2efca-123">Getting Started with Developing an Outlook Social Connector Provider</span></span>](getting-started-with-developing-an-outlook-social-connector-provider.md)

