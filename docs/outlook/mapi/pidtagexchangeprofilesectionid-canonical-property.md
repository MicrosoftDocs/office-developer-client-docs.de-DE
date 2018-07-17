---
title: Kanonische PidTagExchangeProfileSectionId-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagExchangeProfileSectionId
api_type:
- HeaderDef
ms.assetid: 4ad2f417-be8f-4fc8-9321-82097289074b
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 37a318df01101487fe0e8970251201c2515d1e8a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794345"
---
# <a name="pidtagexchangeprofilesectionid-canonical-property"></a><span data-ttu-id="6e247-103">Kanonische PidTagExchangeProfileSectionId-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="6e247-103">PidTagExchangeProfileSectionId Canonical Property</span></span>

  
  
<span data-ttu-id="6e247-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6e247-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6e247-105">Enthält eine dynamisch generierte GUID verwendet, um ein Konto zu bestimmen, wann Sie mehrere Microsoft Exchange Server-Konten verwenden.</span><span class="sxs-lookup"><span data-stu-id="6e247-105">Contains a dynamically generated GUID used to determine an account when you are using multiple Microsoft Exchange Server accounts.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6e247-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="6e247-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6e247-107">PR_EMSMDB_SECTION_UID</span><span class="sxs-lookup"><span data-stu-id="6e247-107">PR_EMSMDB_SECTION_UID</span></span>  <br/> |
|<span data-ttu-id="6e247-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="6e247-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6e247-109">0x3d150102</span><span class="sxs-lookup"><span data-stu-id="6e247-109">0x3d150102</span></span>  <br/> |
|<span data-ttu-id="6e247-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="6e247-110">Data type:</span></span>  <br/> |<span data-ttu-id="6e247-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="6e247-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="6e247-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="6e247-112">Area:</span></span>  <br/> |<span data-ttu-id="6e247-113">Mehrere Exchange-Konten</span><span class="sxs-lookup"><span data-stu-id="6e247-113">Multiple Exchange Accounts</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6e247-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6e247-114">Remarks</span></span>

<span data-ttu-id="6e247-115">Microsoft Outlook 2010 und Microsoft Outlook 2013 unterstützen mehrerer Exchange-Konten anstelle von einem einzelnen Exchange-Konto.</span><span class="sxs-lookup"><span data-stu-id="6e247-115">Microsoft Outlook 2010 and Microsoft Outlook 2013 support multiple Exchange accounts instead of one single Exchange account.</span></span> <span data-ttu-id="6e247-116">Um mehrere Exchange-Konten zu unterstützen, wurde das MAPI-Profil Layout geändert.</span><span class="sxs-lookup"><span data-stu-id="6e247-116">To accommodate multiple Exchange accounts, the MAPI profile layout was changed.</span></span> <span data-ttu-id="6e247-117">In Microsoft Office Outlook 2007 und früheren Versionen enthalten Profile feste Profile-Abschnitt für Exchange-Einstellungen wie Servernamen, Benutzernamen und Offlineordnerdatei (OST).</span><span class="sxs-lookup"><span data-stu-id="6e247-117">In Microsoft Office Outlook 2007 and earlier, profiles contained a fixed profile section dedicated to Exchange settings such as server name, user name, and Offline Folder file (.ost).</span></span> <span data-ttu-id="6e247-118">Speicherort.</span><span class="sxs-lookup"><span data-stu-id="6e247-118">location.</span></span> <span data-ttu-id="6e247-119">Diese Einstellungen wurden über einen eindeutigen Bezeichner, der **PbGlobalProfileSectionGuid** -Eigenschaft identifiziert.</span><span class="sxs-lookup"><span data-stu-id="6e247-119">These settings were identified by using a unique identifier, the **pbGlobalProfileSectionGuid** property.</span></span> <span data-ttu-id="6e247-120">Im Abschnitt für die Exchange-Einstellungen verwendet wird Abschnitts Profile globale Exchange aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="6e247-120">The section used for Exchange settings is called the Exchange Global Profile Section.</span></span> <span data-ttu-id="6e247-121">Weitere Informationen über die globale Exchange-Profil in Outlook 2007 finden Sie unter [globale Abschnitt Profile zu öffnen](http://support.microsoft.com/kb/188482).</span><span class="sxs-lookup"><span data-stu-id="6e247-121">For more information about the Exchange Global Profile in Outlook 2007, see [How To Open the Global Profile Section](http://support.microsoft.com/kb/188482).</span></span>
  
<span data-ttu-id="6e247-122">Ein festen Profil im Abschnitt Speicherort ist nicht mehr ausreichend, um mehrere Exchange-Konten aufzunehmen.</span><span class="sxs-lookup"><span data-stu-id="6e247-122">A fixed profile section location is no longer sufficient to accommodate multiple Exchange accounts.</span></span> <span data-ttu-id="6e247-123">Stattdessen vorhanden ist für jede Exchange-Konto in Ihrem Benutzerprofil ein Abschnitt, der auf die Einstellungen für dieses Konto vorgesehen ist.</span><span class="sxs-lookup"><span data-stu-id="6e247-123">Instead, for each Exchange account in your profile, a section exists that is dedicated to settings for that account.</span></span> <span data-ttu-id="6e247-124">Der neue Abschnitt für die Exchange-Einstellungen verwendet wird durch die eindeutige ID **EmsmdbUID**identifiziert.</span><span class="sxs-lookup"><span data-stu-id="6e247-124">The new section used for Exchange settings is identified by the unique identifier **emsmdbUID**.</span></span>
  
<span data-ttu-id="6e247-125">In der Nachricht Profilabschnitt für die Exchange-Konto finden Sie eine Eigenschaft, die eine GUID enthält, die dynamisch zu dem Zeitpunkt generiert wird, die das Konto erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="6e247-125">In the message service profile section for the Exchange account, you can find a property that contains a GUID that is dynamically generated at the time that the account is created.</span></span> <span data-ttu-id="6e247-126">Diese GUID wird in der **PidTagExchangeProfileSectionId** -Eigenschaft gespeichert.</span><span class="sxs-lookup"><span data-stu-id="6e247-126">This GUID is stored in the **PidTagExchangeProfileSectionId** property.</span></span> <span data-ttu-id="6e247-127">Nachrichtenspeicher und Address Book Container verfügbar machen, eine Eigenschaft, um die Exchange-Konto zu bestimmen, zu dem sie gehören.</span><span class="sxs-lookup"><span data-stu-id="6e247-127">Message stores and address book containers expose a property to determine which Exchange account they belong to.</span></span> <span data-ttu-id="6e247-128">In der Tabelle der Dienste zugänglich, jeden Exchange-Dienst macht diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="6e247-128">Accessible in the message services table, each Exchange service exposes this property.</span></span> 
  
<span data-ttu-id="6e247-129">Sie können diese Eigenschaft durch einen Aufruf von [IMAPIProp::GetProps](imapiprop-getprops.md) auf **PidTagExchangeProfileSectionId** abrufen, nachdem Sie Abfragen aus einem der folgenden Schnittstellen:</span><span class="sxs-lookup"><span data-stu-id="6e247-129">You can retrieve this property through a call to [IMAPIProp::GetProps](imapiprop-getprops.md) on **PidTagExchangeProfileSectionId** after querying for any of the following interfaces:</span></span> 
  
- [<span data-ttu-id="6e247-130">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="6e247-130">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)
    
- [<span data-ttu-id="6e247-131">IMAPIFolder: IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="6e247-131">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)
    
- [<span data-ttu-id="6e247-132">IABContainer: IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="6e247-132">IABContainer : IMAPIContainer</span></span>](iabcontainerimapicontainer.md)
    
<span data-ttu-id="6e247-133">Wenn das Objekt nicht mit Exchange angegliedert ist, gibt der Aufruf **MAPI_E_NOT_FOUND**zurück.</span><span class="sxs-lookup"><span data-stu-id="6e247-133">If the object is not affiliated with Exchange, the call returns **MAPI_E_NOT_FOUND**.</span></span>
  
<span data-ttu-id="6e247-134">Beim Anzeigen des Adressbuchs können Sie Container in einer **PidTagExchangeProfileSectionId** einschränken.</span><span class="sxs-lookup"><span data-stu-id="6e247-134">You can restrict containers on a **PidTagExchangeProfileSectionId** when displaying the address book.</span></span> <span data-ttu-id="6e247-135">Nachdem Sie einen Container geöffneten haben, können Sie die **EmsmdbUID** daraus Abfragen.</span><span class="sxs-lookup"><span data-stu-id="6e247-135">Once you have an opened container, you can query the **emsmdbUID** from it.</span></span> <span data-ttu-id="6e247-136">Es ist außerdem zu beachten, dass wenn ein Empfänger aus einem Exchange-Adressbuch ausgewählt wurde, der Empfänger auch die **PidTagExchangeProfileSectionId** in der Liste der Eigenschaften verfügt.</span><span class="sxs-lookup"><span data-stu-id="6e247-136">It is also worth noting that if a recipient was selected from an Exchange address book, the recipient also has the **PidTagExchangeProfileSectionId** in its list of properties.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="6e247-137">Diese GUID wird in der Codebeispiele und Funktion Kopfzeilen als **EmsmdbUID**bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="6e247-137">Throughout the code samples and function headers, this GUID is known as **emsmdbUID**.</span></span> 
  
<span data-ttu-id="6e247-138">Eines der Exchange-Konten ist mit der Exchange-Vorversionskonten gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="6e247-138">One of the Exchange accounts is marked as the legacy Exchange account.</span></span> <span data-ttu-id="6e247-139">Normalerweise ist es das erste Konto dem Profil hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="6e247-139">Usually, it is the first account added to the profile.</span></span> <span data-ttu-id="6e247-140">Alle Anrufe **PbGlobalProfileSectionGuid** geöffnet wird an die globale Exchange-Abschnitt des legacy-Kontos umgeleitet.</span><span class="sxs-lookup"><span data-stu-id="6e247-140">Every call to open **pbGlobalProfileSectionGuid** is redirected to the Exchange global section of the legacy account.</span></span> <span data-ttu-id="6e247-141">Die Objektmodellaufrufe, die Interaktion mit nicht-Legacy-Exchange-Konto interagieren Sie auch mit der legacy-Exchange-Konto.</span><span class="sxs-lookup"><span data-stu-id="6e247-141">The object model calls that interact with the non-legacy Exchange account also interact with the legacy Exchange account.</span></span> 
  
<span data-ttu-id="6e247-142">Ältere Exchange-Dienst hat die Eigenschaft **PR_EMSMDB_LEGACY** (0x3D18000B), die auf **"true"** in der Tabelle der Dienste festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="6e247-142">The legacy Exchange service has the property **PR_EMSMDB_LEGACY** (0x3D18000B), which is set to **true** in the message services table.</span></span> 
  
<span data-ttu-id="6e247-143">Der Vorversion **EmsmdbUID** wird auch als **PidTagExchangeProfileSectionId**in der globalen Profil im Abschnitt Outlook des Profils versehen.</span><span class="sxs-lookup"><span data-stu-id="6e247-143">The legacy **emsmdbUID** is also stamped in the Outlook Global Profile Section of the profile as **PidTagExchangeProfileSectionId**.</span></span> <span data-ttu-id="6e247-144">Zur Unterstützung mehrerer Exchange-Konten geschriebene Code sollte keinen der Vorversion **EmsmdbUID** abgerufen werden, da es die richtige **EmsmdbUID**, je nach dem Konto abrufen soll, Ihr Code interagiert.</span><span class="sxs-lookup"><span data-stu-id="6e247-144">Code written to support multiple Exchange accounts should not have to retrieve the legacy **emsmdbUID** because it should get the correct **emsmdbUID**, depending on the account your code is interacting with.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6e247-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6e247-145">See also</span></span>



[<span data-ttu-id="6e247-146">Verwenden mehrerer Exchange-Konten</span><span class="sxs-lookup"><span data-stu-id="6e247-146">Using Multiple Exchange Accounts</span></span>](using-multiple-exchange-accounts.md)


[<span data-ttu-id="6e247-147">How To Open the Global Profile Section</span><span class="sxs-lookup"><span data-stu-id="6e247-147">How To Open the Global Profile Section</span></span>](http://support.microsoft.com/kb/188482)
