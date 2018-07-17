---
title: Ordner von Formularbibliotheken
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 62b7480e-b3eb-45fb-b74d-62f1dc918a53
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: f5ce900fee3d40a46e66ac8f74f111db33d7522e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791699"
---
# <a name="folder-form-libraries"></a><span data-ttu-id="a39fa-103">Ordner von Formularbibliotheken</span><span class="sxs-lookup"><span data-stu-id="a39fa-103">Folder Form Libraries</span></span>

  
  
<span data-ttu-id="a39fa-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a39fa-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a39fa-105">In einigen Fällen können Sie ein oder mehrere Formulare mit einem bestimmten Ordner zuordnen möchten.</span><span class="sxs-lookup"><span data-stu-id="a39fa-105">In some cases, you might want to associate one or more forms with a specific folder.</span></span> <span data-ttu-id="a39fa-106">Beispielsweise können Mitarbeiter in Ihrer Organisation alle einen Fortschrittsbericht Ordner in ihren persönlichen Nachrichtenspeicher für das Erstellen und Speichern von Fortschrittsberichte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="a39fa-106">For example, employees in your organization could all have a Progress Report folder in their personal message store for creating and storing progress reports.</span></span> <span data-ttu-id="a39fa-107">Da der Fortschrittsbericht Benutzerordner Fortschrittsbericht spezifisch sind, kann es nicht zum Speichern des Fortschritt Formulars in der Breite Formularbibliothek System geeignet sein.</span><span class="sxs-lookup"><span data-stu-id="a39fa-107">Because the progress report is specific to each user's Progress Report folder, it might not be appropriate to store the progress report form in the system wide form library.</span></span> <span data-ttu-id="a39fa-108">Eine Kopie des Formulars Bericht Aufgabenstatus kann jedoch in der Tabelle verknüpfte Inhalt des Ordners für jeden Benutzer Fortschrittsbericht aufbewahrt werden.</span><span class="sxs-lookup"><span data-stu-id="a39fa-108">However, a copy of the progress report form can be kept in the associated-contents table of each user's Progress Report folder.</span></span> <span data-ttu-id="a39fa-109">Dies verhindert den Benutzer Formulare für Fortschritt außerhalb des festgelegten Ordners.</span><span class="sxs-lookup"><span data-stu-id="a39fa-109">This restricts the user from using progress report forms outside of the designated folder.</span></span>
  
<span data-ttu-id="a39fa-110">Es ist im Prinzip eine Ordner-Formularbibliothek für jeden Ordner in einem Nachrichtenspeicher, auch wenn keine Formular Server darin installiert werden.</span><span class="sxs-lookup"><span data-stu-id="a39fa-110">Conceptually, there is one folder form library for every folder in a message store, even if no form servers are installed in it.</span></span> <span data-ttu-id="a39fa-111">Ordner Formularbibliotheken wie andere Formularbibliotheken implementiert werden – diese als verknüpften Inhalt Tabellen in der alternativen Teil des Ordners gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="a39fa-111">Folder form libraries are implemented like other form libraries — they are stored as associated-contents tables in the alternate part of the folder.</span></span> <span data-ttu-id="a39fa-112">Da Formularbibliotheken Ordner im Ordner enthalten sind, werden sie zusammen mit den übergeordneten Ordner in von Vorgängen kopiert.</span><span class="sxs-lookup"><span data-stu-id="a39fa-112">Because folder form libraries are contained in the folder, they are copied along with their parent folder in copy operations.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a39fa-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a39fa-113">See also</span></span>



[<span data-ttu-id="a39fa-114">MAPI-Formulare</span><span class="sxs-lookup"><span data-stu-id="a39fa-114">MAPI Forms</span></span>](mapi-forms.md)
