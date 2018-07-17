---
title: Richtlinien für das Aktivitäten ordnungsgemäß anzeigen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 55268188-8432-4145-9527-f5888949fc24
description: Outlook Social Connector (OSC)-Anbieter lassen sich die GetActivities und DynamicActivitiesLookupEx Elemente, die die OSC-Aktivitätselemente im Arbeitsspeicher gespeichert haben.
ms.openlocfilehash: f8cb5850c8920f09f784343db18372bb75ca17a4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795954"
---
# <a name="guidelines-for-properly-displaying-activities"></a><span data-ttu-id="76675-103">Richtlinien für das Aktivitäten ordnungsgemäß anzeigen</span><span class="sxs-lookup"><span data-stu-id="76675-103">Guidelines for properly displaying activities</span></span>

<span data-ttu-id="76675-104">Outlook Social Connector (OSC)-Anbieter können die **GetActivities** und **DynamicActivitiesLookupEx** Elemente haben die OSC Aktivitätselemente im Arbeitsspeicher gespeichert.</span><span class="sxs-lookup"><span data-stu-id="76675-104">Outlook Social Connector (OSC) providers can set the **getActivities** and **dynamicActivitiesLookupEx** elements to have the OSC store activity items in memory.</span></span> <span data-ttu-id="76675-105">In diesem Thema werden die OSC-anbietererweiterung, die aus dem sozialen Netzwerk-APIs, die die OSC zum Abrufen oder Aktualisieren von Aktivitäten und Aktivität Besitzer Details, aufruft Wenn der OSC-Anbieter synchronisieren Aktivität unterstützt feeds.</span><span class="sxs-lookup"><span data-stu-id="76675-105">This topic describes the OSC provider extensibility APIs that the OSC calls to get or refresh activities and activity owner details, if the OSC provider supports synchronizing activity feeds from the social network.</span></span> <span data-ttu-id="76675-106">Das Thema enthält auch ein paar untergeordnete Elemente des **ActivityFeed** -Elements, dass der OSC-Anbieter für das osc bilden zum Anzeigen von Aktivitäten ordnungsgemäß in der Office-Visitenkarte oder Outlook Personenbereich festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="76675-106">The topic also lists a few child elements of the **activityFeed** element that the OSC provider should set for the OSC to display activities properly in the Office Contact Card or Outlook People Pane.</span></span> 
  
- <span data-ttu-id="76675-107">Die OSC Ruft die [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) -Methode zum Abrufen und Speichern von Aktivitäten im Newsfeed Ordner des angemeldeten Benutzers.</span><span class="sxs-lookup"><span data-stu-id="76675-107">The OSC calls the [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) method to get and store activities in the News Feed folder for the logged-on user.</span></span> <span data-ttu-id="76675-108">Der OSC-Anbieter muss **GetActivitiesEx** um _Aktivitäten_ XML-Zeichenfolge zurückzugeben, die mit dem OSC-Anbieter XML-Schemadefinition des **ActivityFeed** -Elements entspricht implementieren.</span><span class="sxs-lookup"><span data-stu-id="76675-108">The OSC provider must implement **GetActivitiesEx** to return an  _activities_ XML string that complies with the OSC provider XML schema definition of the **activityFeed** element.</span></span> 
    
- <span data-ttu-id="76675-109">Der OSC-Anbieter muss das **OwnerID** -Element ein untergeordnetes Element des Elements **ActivityDetails ist** festlegen.</span><span class="sxs-lookup"><span data-stu-id="76675-109">The OSC provider must set the **ownerID** element, which is a child element of the **activityDetails** element.</span></span> <span data-ttu-id="76675-110">**OwnerID** ist eine opake Zeichenfolge, die den Besitzer der Aktivität im sozialen Netzwerk identifiziert.</span><span class="sxs-lookup"><span data-stu-id="76675-110">**ownerID** is an opaque string that identifies the owner of the activity on the social network.</span></span> 
    
- <span data-ttu-id="76675-111">Der OSC-Anbieter sollte die **NameHint** und **EmailAddress** -Elemente im Knoten **PublisherVariable** des **TemplateVariables** -Elements festgelegt.</span><span class="sxs-lookup"><span data-stu-id="76675-111">The OSC provider should set the **nameHint** and **emailAddress** elements in the **publisherVariable** node of the **templateVariables** element.</span></span> 
    
   <span data-ttu-id="76675-112">Beachten Sie, dass pro das OSC-Anbieter-XML-Schema, das **NameHint** -Element ein optionales Element ist.</span><span class="sxs-lookup"><span data-stu-id="76675-112">Note that per the OSC provider XML schema, the **nameHint** element is an optional element.</span></span> <span data-ttu-id="76675-113">Die OSC wird verwendet, um den Anzeigenamen des Benutzers in der Visitenkarte oder Personenbereich ausgewählt übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="76675-113">The OSC uses it to match the display name of the user selected in the Contact Card or People Pane.</span></span> <span data-ttu-id="76675-114">In ähnlicher Weise ist das **EmailAddress** -Element ein optionales Element im XML-Schema.</span><span class="sxs-lookup"><span data-stu-id="76675-114">Similarly, the **emailAddress** element is an optional element in the XML schema.</span></span> <span data-ttu-id="76675-115">Die OSC wird verwendet, um die SMTP-Adresse des Benutzers in der Visitenkarte oder Personenbereich ausgewählt übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="76675-115">The OSC uses it to match the SMTP address of the user selected in the Contact Card or People Pane.</span></span> 
    
   <span data-ttu-id="76675-116">Wenn nur das **OwnerID** -Element angegeben ist, aber eine oder beide der **NameHint** und **EmailAddress** nicht angegeben werden, ruft das osc bilden die [ISocialSession2::GetPeopleDetails](isocialsession2-getpeopledetails.md) -Methode, und klicken Sie dann die [ISocialPerson::GetDetails](isocialperson-getdetails.md) Methode, um weitere Informationen über die Person, die vom **OwnerID**abzurufen.</span><span class="sxs-lookup"><span data-stu-id="76675-116">If only the **ownerID** element is specified, but one or both of **nameHint** and **emailAddress** are not specified, the OSC calls the [ISocialSession2::GetPeopleDetails](isocialsession2-getpeopledetails.md) method and then the [ISocialPerson::GetDetails](isocialperson-getdetails.md) method to get more information about the person identified by the **ownerID**.</span></span> <span data-ttu-id="76675-117">Wenn die OSC **ISocialPerson::GetDetails**aufruft, muss der Anbieter **Person** XML zurück, der die **FullName** und **EmailAddress** -Elemente angibt.</span><span class="sxs-lookup"><span data-stu-id="76675-117">When the OSC calls **ISocialPerson::GetDetails**, the provider must return **person** XML that specifies the **fullName** and **emailAddress** elements.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="76675-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="76675-118">See also</span></span>

- [<span data-ttu-id="76675-119">XML-Code für Aktivitäten</span><span class="sxs-lookup"><span data-stu-id="76675-119">XML for Activities</span></span>](xml-for-activities.md)  
- [<span data-ttu-id="76675-120">XML-Code für Freunde</span><span class="sxs-lookup"><span data-stu-id="76675-120">XML for Friends</span></span>](xml-for-friends.md)  
- [<span data-ttu-id="76675-121">XML-Code für Funktionen</span><span class="sxs-lookup"><span data-stu-id="76675-121">XML for Capabilities</span></span>](xml-for-capabilities.md)
