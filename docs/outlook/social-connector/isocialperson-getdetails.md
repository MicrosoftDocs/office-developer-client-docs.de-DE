---
title: ISocialPersonGetDetails
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9ca3172a-82a3-4483-b0aa-4e848930f6ed
description: Ruft eine Zeichenfolge, die Details zu einem Profilbild der Person ein, beispielsweise den Vornamen, Nachnamen sowie eine URL darstellt.
ms.openlocfilehash: 158ce9b5c6a97ffff0325427ed07c74f518941d8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795962"
---
# <a name="isocialpersongetdetails"></a><span data-ttu-id="d964a-103">ISocialPerson::GetDetails</span><span class="sxs-lookup"><span data-stu-id="d964a-103">ISocialPerson::GetDetails</span></span>

<span data-ttu-id="d964a-104">Ruft eine Zeichenfolge, die Details zu einem Profilbild der Person ein, beispielsweise den Vornamen, Nachnamen sowie eine URL darstellt.</span><span class="sxs-lookup"><span data-stu-id="d964a-104">Gets a string that represents details for the person, such as the first name, last name, and a URL to a profile picture.</span></span> 
  
```cpp
HRESULT _stdcall GetDetails([out, retval] BSTR* details);
```

## <a name="parameters"></a><span data-ttu-id="d964a-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="d964a-105">Parameters</span></span>

<span data-ttu-id="d964a-106">_Details_</span><span class="sxs-lookup"><span data-stu-id="d964a-106">_details_</span></span>
  
> <span data-ttu-id="d964a-107">[out] Ein XML-String-Wert, der die Details für eine Person darstellt.</span><span class="sxs-lookup"><span data-stu-id="d964a-107">[out] An XML string value that represents the details for a person.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d964a-108">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d964a-108">Remarks</span></span>

<span data-ttu-id="d964a-109">Die zurückgegebene _Details_ XML-Zeichenfolge muss die Schemadefinition für die **Person**, gemäß Definition im Schema für Outlook Social Connector (OSC)-Erweiterbarkeit des Providers entsprechen.</span><span class="sxs-lookup"><span data-stu-id="d964a-109">The returned  _details_ XML string must comply with the schema definition for **person**, as defined in the schema for Outlook Social Connector (OSC) provider extensibility.</span></span>
  
<span data-ttu-id="d964a-110">Die OSC-Aufrufe **GetDetails** , wenn der OSC-Anbieter unterstützt zwischengespeichert oder Hybrid Synchronisierung von Freunde im sozialen Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="d964a-110">The OSC calls **GetDetails** if the OSC provider supports cached or hybrid synchronization of friends on the social network.</span></span> <span data-ttu-id="d964a-111">Wenn der OSC anfänglich Freunde Aktivitäten für den angemeldeten Benutzer erhält, ruft [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md), und speichert Freunde Informationen in einem Kontakteordner speziell für die sozialen Netzwerk, in der Outlook-Standardspeicher des angemeldeten Benutzers .</span><span class="sxs-lookup"><span data-stu-id="d964a-111">When the OSC initially gets friends' activities for the logged on user, it calls [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md), and stores friends' information in a contacts folder specific to the social network, in the logged on user's default Outlook store.</span></span> <span data-ttu-id="d964a-112">Anschließend wird die OSC nicht **GetFriendsAndColleagues** oder **GetDetails** aufgerufen, wenn das Aktualisierungsintervall für den Cache abgelaufen ist.</span><span class="sxs-lookup"><span data-stu-id="d964a-112">Subsequently the OSC does not call **GetFriendsAndColleagues** or **GetDetails** unless the refresh interval for the cache has expired.</span></span> <span data-ttu-id="d964a-113">Weitere Informationen dazu, wie die OSC Informationen in einem Kontakteordner Freunde zwischenspeichert finden Sie unter [Synchronisieren Freunde und Aktivitäten](synchronizing-friends-and-activities.md).</span><span class="sxs-lookup"><span data-stu-id="d964a-113">For more information about how the OSC caches friends' information in a contacts folder, see [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d964a-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d964a-114">See also</span></span>

- [<span data-ttu-id="d964a-115">ISocialPerson: IUnknown</span><span class="sxs-lookup"><span data-stu-id="d964a-115">ISocialPerson : IUnknown</span></span>](isocialpersoniunknown.md)
