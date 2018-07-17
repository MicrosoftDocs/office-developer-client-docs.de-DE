---
title: Provider-Tabellen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 99709a4c-cb52-436e-a322-02ded5d65ce5
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: a613bd744a113b4378c5bef94fb51f6ae3aa4041
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795330"
---
# <a name="provider-tables"></a><span data-ttu-id="ed2de-103">Provider-Tabellen</span><span class="sxs-lookup"><span data-stu-id="ed2de-103">Provider Tables</span></span>

  
  
<span data-ttu-id="ed2de-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ed2de-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ed2de-105">Eine Anbieter-Tabelle enthält Informationen zu Dienstanbietern.</span><span class="sxs-lookup"><span data-stu-id="ed2de-105">A provider table contains information about service providers.</span></span> <span data-ttu-id="ed2de-106">Es gibt zwei verschiedene Anbieter Tabellen, beide MAPI implementiert und von Clients verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ed2de-106">There are two different provider tables, both implemented by MAPI and used by clients.</span></span> <span data-ttu-id="ed2de-107">Die erste Tabelle, die durch Aufrufen der Methode [IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md) zugegriffen enthält Informationen über alle Anbieter für das aktuelle Profil.</span><span class="sxs-lookup"><span data-stu-id="ed2de-107">The first table, accessed by calling the [IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md) method, holds information about all of the providers for the current profile.</span></span> <span data-ttu-id="ed2de-108">Die zweite Tabelle, auf die Sie über [IProviderAdmin::GetProviderTable](iprovideradmin-getprovidertable.md), erstellt eine Tabelle, die Informationen zu allen-Dienstanbieter für einen Nachrichtendienst gespeichert.</span><span class="sxs-lookup"><span data-stu-id="ed2de-108">The second table, accessed through [IProviderAdmin::GetProviderTable](iprovideradmin-getprovidertable.md), creates a table that stores information about all of the service providers for a message service.</span></span>
  
<span data-ttu-id="ed2de-109">Diese beiden Tabellen haben ein weiterer Unterschied.</span><span class="sxs-lookup"><span data-stu-id="ed2de-109">These two tables have another difference.</span></span> <span data-ttu-id="ed2de-110">Tabelle der Dienstanbieter über **IMsgServiceAdmin::GetProviderTable** verfügbar enthält nur die Zeilen, die Dienstanbieter darstellen, während die Tabelle über **IProviderAdmin::GetProviderTable** Zeilen hinzugefügt werden, die darstellen Weitere Informationen im Zusammenhang mit einem Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="ed2de-110">The provider table available through **IMsgServiceAdmin::GetProviderTable** contains only rows that represent service providers while the table available through **IProviderAdmin::GetProviderTable** may include rows that represent additional information associated with a service provider.</span></span> <span data-ttu-id="ed2de-111">Diese zusätzlichen Informationen wird das Profil mit dem Schlüsselwort "Abschnitte" der MAPISVC.INF hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="ed2de-111">This extra information is added to the profile with the "Sections" keyword of MAPISVC.INF.</span></span> <span data-ttu-id="ed2de-112">Wenn ein Anbieter zusätzliche Profil hat, werden die **MAPIUID** Werte für diese Abschnitte in der Eigenschaft **PR_SERVICE_EXTRA_UIDS** ([PidTagServiceExtraUids](pidtagserviceextrauids-canonical-property.md)) gespeichert.</span><span class="sxs-lookup"><span data-stu-id="ed2de-112">When a provider has extra profile sections, it stores the **MAPIUID** values for these sections in the **PR_SERVICE_EXTRA_UIDS** ([PidTagServiceExtraUids](pidtagserviceextrauids-canonical-property.md)) property.</span></span> <span data-ttu-id="ed2de-113">**PR_SERVICE_EXTRA_UIDS** wird im Abschnitt Profile Service Nachricht gespeichert.</span><span class="sxs-lookup"><span data-stu-id="ed2de-113">**PR_SERVICE_EXTRA_UIDS** is saved in the message service profile section.</span></span> 
  
<span data-ttu-id="ed2de-114">Die folgenden Eigenschaften bilden die erforderliche Spalte in beide Arten von Anbieter für Tabellen festzulegen:</span><span class="sxs-lookup"><span data-stu-id="ed2de-114">The following properties make up the required column set in both types of provider tables:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ed2de-115">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ed2de-115">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="ed2de-116">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ed2de-116">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="ed2de-117">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ed2de-117">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="ed2de-118">**PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ed2de-118">**PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="ed2de-119">**PR_PROVIDER_ORDINAL** ([PidTagProviderOrdinal](pidtagproviderordinal-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ed2de-119">**PR_PROVIDER_ORDINAL** ([PidTagProviderOrdinal](pidtagproviderordinal-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="ed2de-120">**PR_PROVIDER_UID** ([PidTagProviderUid](pidtagprovideruid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ed2de-120">**PR_PROVIDER_UID** ([PidTagProviderUid](pidtagprovideruid-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="ed2de-121">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ed2de-121">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="ed2de-122">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ed2de-122">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="ed2de-123">**PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ed2de-123">**PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="ed2de-124">**PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ed2de-124">**PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md))</span></span>  <br/> |
   
<span data-ttu-id="ed2de-125">Tabelle der Dienstanbieter kann verwendet werden, um die aktuelle Transport Reihenfolge anzuzeigen oder zu ändern.</span><span class="sxs-lookup"><span data-stu-id="ed2de-125">The provider table can be used to display the current transport order or to change it.</span></span> <span data-ttu-id="ed2de-126">Um die aktuelle Reihenfolge anzuzeigen, erstellen Sie eine Einschränkung, um nur die Zeilen mit der **PR_RESOURCE_TYPE** -Eigenschaft, um MAPI_TRANSPORT_PROVIDER abzurufen.</span><span class="sxs-lookup"><span data-stu-id="ed2de-126">To display the current order, build a restriction to retrieve only those rows with the **PR_RESOURCE_TYPE** property set to MAPI_TRANSPORT_PROVIDER.</span></span> <span data-ttu-id="ed2de-127">Klicken Sie dann verwenden Sie **PR_PROVIDER_ORDINAL** als Sortierschlüssel zum Sortieren der Tabelle und alle Zeilen mit [der QueryRows](imapitable-queryrows.md) oder die Funktion [HrQueryAllRows](hrqueryallrows.md) abrufen.</span><span class="sxs-lookup"><span data-stu-id="ed2de-127">Then use **PR_PROVIDER_ORDINAL** as a sort key to sort the table and retrieve all the rows with either the [IMAPITable::QueryRows](imapitable-queryrows.md) method or the [HrQueryAllRows](hrqueryallrows.md) function.</span></span> 
  
<span data-ttu-id="ed2de-128">Ändern der Reihenfolge Transport, gelten diese Beschränkung und die Zeilen abrufen.</span><span class="sxs-lookup"><span data-stu-id="ed2de-128">To change the transport order, apply the same restriction and retrieve the rows.</span></span> <span data-ttu-id="ed2de-129">Klicken Sie dann erstellen Sie ein Array von Werten aus der **PR_PROVIDER_UID** -Eigenschaft, die die eindeutigen Bezeichner für den Transport Anbietern darstellt.</span><span class="sxs-lookup"><span data-stu-id="ed2de-129">Then create an array of values from the **PR_PROVIDER_UID** property that represents the unique identifiers for the transport providers.</span></span> <span data-ttu-id="ed2de-130">Wenn der Bezeichner in der gewünschten Reihenfolge befinden, an die [IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md) -Methode übergeben.</span><span class="sxs-lookup"><span data-stu-id="ed2de-130">When the identifiers are in the desired order, pass them to the [IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md) method.</span></span> 
  
<span data-ttu-id="ed2de-131">Nachdem eine Tabelle Anbieter verfügbar gemacht wurde, wird es nicht nachfolgende Änderungen, wie die Hinzufügung oder Löschung eines Anbieters wider.</span><span class="sxs-lookup"><span data-stu-id="ed2de-131">After a provider table has been made available, it will not reflect subsequent changes, such as the addition or deletion of a provider.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ed2de-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ed2de-132">See also</span></span>



[<span data-ttu-id="ed2de-133">MAPI-Tabellen</span><span class="sxs-lookup"><span data-stu-id="ed2de-133">MAPI Tables</span></span>](mapi-tables.md)
