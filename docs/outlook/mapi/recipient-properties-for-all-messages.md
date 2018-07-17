---
title: Empfängereigenschaften für alle Nachrichten
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 18c96796-f38d-4058-9c51-9c5a14990846
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: d92e9dbbf594dffc3dbf5bbf271fc80a0abed68e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795341"
---
# <a name="recipient-properties-for-all-messages"></a><span data-ttu-id="25a6e-103">Empfängereigenschaften für alle Nachrichten</span><span class="sxs-lookup"><span data-stu-id="25a6e-103">Recipient Properties for All Messages</span></span>

  
  
<span data-ttu-id="25a6e-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="25a6e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="25a6e-105">Die folgenden Eigenschaften sind in der Regel für alle Empfänger der Nachricht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="25a6e-105">The following properties are typically present for all message recipients.</span></span> <span data-ttu-id="25a6e-106">**PR_EMAIL_ADDRESS** und **PR_SEARCH_KEY** sind optional. Alle anderen Eigenschaften sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="25a6e-106">**PR_EMAIL_ADDRESS** and **PR_SEARCH_KEY** are optional; all of the other properties are required.</span></span> 
  
<span data-ttu-id="25a6e-107">**Titel der Tabelle**</span><span class="sxs-lookup"><span data-stu-id="25a6e-107">**Table Title**</span></span>

|<span data-ttu-id="25a6e-108">**Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="25a6e-108">**Property**</span></span>|<span data-ttu-id="25a6e-109">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="25a6e-109">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="25a6e-110">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="25a6e-110">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="25a6e-111">Enthält die messaging-Benutzer e-Mail-Adresstyp wie SMTP.</span><span class="sxs-lookup"><span data-stu-id="25a6e-111">Contains the messaging user's email address type, such as SMTP.</span></span>  <br/> |
|<span data-ttu-id="25a6e-112">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="25a6e-112">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="25a6e-113">Enthält den Anzeigenamen für ein bestimmtes MAPI-Objekt.</span><span class="sxs-lookup"><span data-stu-id="25a6e-113">Contains the display name for a given MAPI object.</span></span>  <br/> |
|<span data-ttu-id="25a6e-114">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="25a6e-114">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="25a6e-115">Enthält einen Wert zum Verknüpfen eines Symbols mit einer bestimmten Zeile einer Tabelle verwendet.</span><span class="sxs-lookup"><span data-stu-id="25a6e-115">Contains a value used to associate an icon with a particular row of a table.</span></span>  <br/> |
|<span data-ttu-id="25a6e-116">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="25a6e-116">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="25a6e-117">Messaging-Benutzer e-Mail-Adresse enthält.</span><span class="sxs-lookup"><span data-stu-id="25a6e-117">Contains the messaging user's email address.</span></span>  <br/> |
|<span data-ttu-id="25a6e-118">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="25a6e-118">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="25a6e-119">Enthält eine MAPI-Eintrags-ID, die zum Öffnen und Bearbeiten der Eigenschaften eines bestimmten MAPI-Objekts verwendet.</span><span class="sxs-lookup"><span data-stu-id="25a6e-119">Contains a MAPI entry identifier used to open and edit properties of a particular MAPI object.</span></span>  <br/> |
|<span data-ttu-id="25a6e-120">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="25a6e-120">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="25a6e-121">Enthält den Typ eines Objekts.</span><span class="sxs-lookup"><span data-stu-id="25a6e-121">Contains the type of an object.</span></span>  <br/> |
|<span data-ttu-id="25a6e-122">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="25a6e-122">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="25a6e-123">Enthält einen binären vergleichbaren Schlüssel, der für eine Suche korrelierte Objekte identifiziert.</span><span class="sxs-lookup"><span data-stu-id="25a6e-123">Contains a binary-comparable key that identifies correlated objects for a search.</span></span>  <br/> |
   
