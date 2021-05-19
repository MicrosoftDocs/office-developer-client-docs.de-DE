---
title: Übersicht über den MAPI-Adressbuchanbieter
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ead51434-ae19-4c34-aa7a-bdeeccca5bd9
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: ee628f4b11cb174c05a16ca60c9ec830a0e9abbe
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426541"
---
# <a name="mapi-address-book-provider-overview"></a><span data-ttu-id="1338d-103">Übersicht über den MAPI-Adressbuchanbieter</span><span class="sxs-lookup"><span data-stu-id="1338d-103">MAPI address book provider overview</span></span>
  
<span data-ttu-id="1338d-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1338d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1338d-105">Adressbuchanbieter verarbeiten den Zugriff auf Verzeichnisinformationen.</span><span class="sxs-lookup"><span data-stu-id="1338d-105">Address book providers handle access to directory information.</span></span> <span data-ttu-id="1338d-106">Verzeichnisinformationen bestehen aus Daten für zwei Arten von Nachrichtenempfängern: einzelne Messagingbenutzer und Gruppen von Messagingbenutzern, die häufig gemeinsam in Verteilerlisten adressiert werden.</span><span class="sxs-lookup"><span data-stu-id="1338d-106">Directory information consists of data for two types of message recipients: individual messaging users and groups of messaging users who are commonly addressed together in distribution lists.</span></span> <span data-ttu-id="1338d-107">Je nach Empfängertyp und Adressbuchanbieter gibt es eine vielzahl von Informationen, die zur Verfügung stehen können.</span><span class="sxs-lookup"><span data-stu-id="1338d-107">Depending on the type of recipient and the address book provider, there is a wide range of information that can be made available.</span></span> <span data-ttu-id="1338d-108">Beispielsweise speichern alle Adressbuchanbieter den Namen, die Adresse und den Adresstyp eines Empfängers.</span><span class="sxs-lookup"><span data-stu-id="1338d-108">For example, all address book providers store a recipient's name, address, and address type.</span></span>
  
<span data-ttu-id="1338d-109">Jeder Adressbuchanbieter organisiert diese Daten mithilfe eines oder mehreren Containern.</span><span class="sxs-lookup"><span data-stu-id="1338d-109">Each address book provider organizes this data by using one or more containers.</span></span> <span data-ttu-id="1338d-110">Die Anzahl und Struktur der Container hängt von der Implementierung des Adressbuchanbieters ab.</span><span class="sxs-lookup"><span data-stu-id="1338d-110">The number and structure of the containers depends on the address book provider's implementation.</span></span> <span data-ttu-id="1338d-111">Ein Adressbuchanbieter kann z. B. einen einzelnen Container verwenden, um alle Informationen zu enthalten, ein anderer kann einen Container auf oberster Ebene verwenden, der Untercontainer enthält, und ein dritter kann mehrere Container auf oberster Ebene verwenden, die jeweils Untercontainer enthalten.</span><span class="sxs-lookup"><span data-stu-id="1338d-111">For example, one address book provider might use a single container to hold all of the information, another might use one top-level container that holds subcontainers, and a third might use several top-level containers, each holding subcontainers.</span></span> <span data-ttu-id="1338d-112">Eine Adressbuchcontainerhierarchie kann recht tief sein. Es gibt keine Beschränkung der Anzahl von Untercontainern, die verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="1338d-112">An address book container hierarchy can be quite deep; there is no limit to the number of subcontainers that can be used.</span></span>
  
<span data-ttu-id="1338d-113">Die folgende Abbildung zeigt eine typische MAPI-Adressbuchorganisation.</span><span class="sxs-lookup"><span data-stu-id="1338d-113">The following illustration shows a typical MAPI address book organization.</span></span>
  
<span data-ttu-id="1338d-114">**Adressbuchorganisation**</span><span class="sxs-lookup"><span data-stu-id="1338d-114">**Address book organization**</span></span>
  
<span data-ttu-id="1338d-115">![Adressbuchorganisation](media/amapi_04.gif "Adressbuchorganisation")</span><span class="sxs-lookup"><span data-stu-id="1338d-115">![Address book organization](media/amapi_04.gif "Address book organization")</span></span>
  
<span data-ttu-id="1338d-116">MAPI integriert alle Informationen, die von den installierten Adressbuchanbietern bereitgestellt werden, in ein einzelnes Adressbuch und stellt eine einheitliche Ansicht für die Clientanwendung zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="1338d-116">MAPI integrates all the information supplied by the installed address book providers into a single address book, presenting a unified view to the client application.</span></span> <span data-ttu-id="1338d-117">Die integrierte Liste zeigt die Container auf oberster Ebene an, die von jedem der installierten Adressbuchanbieter angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="1338d-117">The integrated list shows the top-level containers displayed by each of the installed address book providers.</span></span> <span data-ttu-id="1338d-118">Die meisten Adressbuchanbieter machen nur wenige Container (in der Regel 1 bis 3) auf oberster Ebene verfügbar, um in die oberste Ebene des integrierten Adressbuchs mapI zu integrieren.</span><span class="sxs-lookup"><span data-stu-id="1338d-118">Most address book providers expose only a few containers (typically one to three) at the top level for inclusion in the top level of the MAPI integrated address book.</span></span> <span data-ttu-id="1338d-119">Ein Adressbuchanbieter kann beispielsweise "Alle Benutzer" und "Lokale Benutzer" als zwei Container auf oberster Ebene zur Verfügung stellen.</span><span class="sxs-lookup"><span data-stu-id="1338d-119">For example, an address book provider might make available "All Users" and "Local Users" as two containers at the top level.</span></span>
  
<span data-ttu-id="1338d-120">Die Benutzer von Clientanwendungen können den Inhalt von Adressbuchcontainern anzeigen und in einigen Fällen den Inhalt ändern.</span><span class="sxs-lookup"><span data-stu-id="1338d-120">The users of client applications can view the contents of address book containers and, in some cases, modify the contents.</span></span> <span data-ttu-id="1338d-121">Adressbuchcontainer können je nach Adressbuchanbieter mit unterschiedlichen Zugriffsebenen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="1338d-121">Address book containers can be created with different access levels, depending on the address book provider.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1338d-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1338d-122">See also</span></span>

- [<span data-ttu-id="1338d-123">MAPI-Features und -Architektur</span><span class="sxs-lookup"><span data-stu-id="1338d-123">MAPI Features and Architecture</span></span>](mapi-features-and-architecture.md)

