---
title: Speichern von MAPI-Eigenschaften
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ed0c14f9-3dcf-49ad-928e-ba872d4d6b5a
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 6135dfae915a1e70743f9224352390c4b56ea02e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795418"
---
# <a name="saving-mapi-properties"></a><span data-ttu-id="a40d9-103">Speichern von MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a40d9-103">Saving MAPI Properties</span></span>

  
  
<span data-ttu-id="a40d9-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a40d9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a40d9-105">Viele Objekte unterstützen eine Transaktionsmodell der Verarbeitung bei dem Eigenschaften nicht permanent geändert werden, bis sie zu einem späteren Zeitpunkt übernommen werden.</span><span class="sxs-lookup"><span data-stu-id="a40d9-105">Many objects support a transaction model of processing whereby changes to properties are not made permanent until they are committed at a later time.</span></span> <span data-ttu-id="a40d9-106">Während die Änderungen an Eigenschaften von den Methoden [IMAPIProp::SetProps](imapiprop-setprops.md) und [IMAPIProp::DeleteProps](imapiprop-deleteprops.md) behandelt werden, wird der Schritt Commit von [IMAPIProp::SaveChanges](imapiprop-savechanges.md)behandelt.</span><span class="sxs-lookup"><span data-stu-id="a40d9-106">Whereas changes to properties are handled by the [IMAPIProp::SetProps](imapiprop-setprops.md) and [IMAPIProp::DeleteProps](imapiprop-deleteprops.md) methods, the commit step is handled by [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span></span> <span data-ttu-id="a40d9-107">Es ist nicht erst nach einem erfolgreichen Aufruf von **SaveChanges** , dass die aktuellste Version von Eigenschaften eines Objekts zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="a40d9-107">It isn't until after a successful call to **SaveChanges** that the most recent version of an object's properties can be accessed.</span></span> 
  
<span data-ttu-id="a40d9-108">Wenn **SaveChanges** den Fehlerwert MAPI_E_OBJECT_CHANGED zurückgegeben wird, ist dies eine Warnung, dass ein anderer Client gleichzeitig Änderungen auf das Objekt übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="a40d9-108">When **SaveChanges** returns the error value MAPI_E_OBJECT_CHANGED, this is a warning that another client is simultaneously committing changes to the object.</span></span> <span data-ttu-id="a40d9-109">Es ist möglich, und öffnen je nach der Anbieter das Objekt erfolgreich für mehrere Clients zum Implementieren eines Objekts durch Aufrufen seiner **OpenEntry** -Methode mit der MAPI_MODIFY-Flag, Gewähren von Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="a40d9-109">It is possible, depending on the provider implementing the object, for multiple clients to successfully open an object by calling its **OpenEntry** method with the MAPI_MODIFY flag set, giving them read/write access.</span></span> <span data-ttu-id="a40d9-110">Das Objekt, das solcher zurückgegeben wird, dass ein Anruf **OpenEntry** eine Momentaufnahme der Speicherdaten ist.</span><span class="sxs-lookup"><span data-stu-id="a40d9-110">The object that is returned from such an **OpenEntry** call is a snapshot of the storage data.</span></span> <span data-ttu-id="a40d9-111">Jedem nachfolgenden Versuch, diese Daten ändern kann vorherige Versuch zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="a40d9-111">Each subsequent attempt to change this data can overwrite the previous attempt.</span></span> 
  
<span data-ttu-id="a40d9-112">Beimkontakt MAPI_E_OBJECT_CHANGED aus **SaveChanges**, muss der Client die Option aus, um:</span><span class="sxs-lookup"><span data-stu-id="a40d9-112">Upon receiving MAPI_E_OBJECT_CHANGED from **SaveChanges**, a client has the option to:</span></span> 
  
- <span data-ttu-id="a40d9-113">Erstellen Sie eine Kopie des Objekts, um die Änderungen zu halten.</span><span class="sxs-lookup"><span data-stu-id="a40d9-113">Make a copy of the object to hold the changes.</span></span>
    
- <span data-ttu-id="a40d9-114">Stellen Sie einen weiteren Anruf zu **SaveChanges**, FORCE_SAVE angeben.</span><span class="sxs-lookup"><span data-stu-id="a40d9-114">Make another call to **SaveChanges**, specifying FORCE_SAVE.</span></span> 
    
<span data-ttu-id="a40d9-115">Durch den Aufruf von **SaveChanges** das Flag FORCE_SAVE überschreibt das vorherige speichern ein und ändert ein Client dauerhaft entfernt.</span><span class="sxs-lookup"><span data-stu-id="a40d9-115">Calling **SaveChanges** with the FORCE_SAVE flag overwrites the previous save and makes a client's changes permanent.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a40d9-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a40d9-116">See also</span></span>



[<span data-ttu-id="a40d9-117">�bersicht �ber die MAPI-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="a40d9-117">MAPI Property Overview</span></span>](mapi-property-overview.md)
