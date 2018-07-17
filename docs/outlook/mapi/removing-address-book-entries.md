---
title: Entfernen von Adressbucheinträgen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 107ebcd7-b612-4139-b676-c3851f15bc74
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 1fb7224e110bbee6844cf2820782aac8be213ba3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795356"
---
# <a name="removing-address-book-entries"></a><span data-ttu-id="2b8a1-103">Entfernen von Adressbucheinträgen</span><span class="sxs-lookup"><span data-stu-id="2b8a1-103">Removing address book entries</span></span>
  
<span data-ttu-id="2b8a1-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2b8a1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2b8a1-105">Des Containers [IABContainer::DeleteEntries](iabcontainer-deleteentries.md) -Methode aufgerufen, um einen oder mehrere Empfänger zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="2b8a1-105">Your container's [IABContainer::DeleteEntries](iabcontainer-deleteentries.md) method is called to remove one or more recipients.</span></span> <span data-ttu-id="2b8a1-106">**DeleteEntries** hat zwei Parameter: ein Array von Eintragsbezeichner, die die Empfänger zu löschenden darstellt und ein Flagwert reserviert.</span><span class="sxs-lookup"><span data-stu-id="2b8a1-106">**DeleteEntries** has two parameters: an array of entry identifiers representing the recipients to be deleted and a reserved flags value.</span></span> <span data-ttu-id="2b8a1-107">Löschen eines Empfängers wirkt sich aus die Inhaltstabelle des Containers. Zusätzlich zu den Empfänger löschen, muss der Container für die Tabellenzeile Inhalt löschen, die den Empfänger darstellt.</span><span class="sxs-lookup"><span data-stu-id="2b8a1-107">Deleting a recipient affects the contents table of your container; in addition to deleting the recipient, your container must delete the contents table row that represents the recipient.</span></span> <span data-ttu-id="2b8a1-108">Wenn die Zeile aus der Tabelle entfernt wurde, muss der Container für eine Benachrichtigung über eine Tabelle auf allen registrierten Clients ausstellen.</span><span class="sxs-lookup"><span data-stu-id="2b8a1-108">When the row has been removed from the table, your container must issue a table notification to each registered client.</span></span> 
  
### <a name="to-implement-iabcontainerdeleteentries"></a><span data-ttu-id="2b8a1-109">Implementieren von IABContainer::DeleteEntries</span><span class="sxs-lookup"><span data-stu-id="2b8a1-109">To implement IABContainer::DeleteEntries</span></span>
  
1. <span data-ttu-id="2b8a1-110">Löschen Sie jeden Empfänger, dargestellt durch die Eintrags-ID aus dem Container.</span><span class="sxs-lookup"><span data-stu-id="2b8a1-110">Delete each recipient represented by the entry identifier from your container.</span></span>
    
2. <span data-ttu-id="2b8a1-111">Wenn Inhaltstabelle des Containers geöffnet ist:</span><span class="sxs-lookup"><span data-stu-id="2b8a1-111">If your container's contents table is open:</span></span>
    
   - <span data-ttu-id="2b8a1-112">Senden Sie eine Benachrichtigung _FnevTableModified_ mit dem **UlTableEvent** -Element festlegen, um den registrierten Clients für jede Tabellenzeile gelöschten Inhalt TABLE_ROW_DELETED.</span><span class="sxs-lookup"><span data-stu-id="2b8a1-112">Send an  _fnevTableModified_ notification with the **ulTableEvent** member set to TABLE_ROW_DELETED to registered clients for each deleted contents table row.</span></span> <span data-ttu-id="2b8a1-113">Wenn der Anbieter das Dienstprogramm Benachrichtigung verwendet wird, rufen Sie [IMAPISupport::Notify](imapisupport-notify.md) , um diese Benachrichtigungen zu senden.</span><span class="sxs-lookup"><span data-stu-id="2b8a1-113">If your provider uses the notification utility, call [IMAPISupport::Notify](imapisupport-notify.md) to send these notifications.</span></span> 
    
   - <span data-ttu-id="2b8a1-114">Wenn der Anbieter Objekt Benachrichtigungen unterstützt, auch senden Sie eine _FnevObjectDeleted_ -Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="2b8a1-114">If your provider supports object notifications, also send an  _fnevObjectDeleted_ notification.</span></span> 
    
