---
title: Übersicht über das MAPI-Objekt und die Schnittstelle
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d4ece3af-cb54-4727-8072-0c055381ec11
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: fcd85bf518f4e6466bf15a09e417767bc34df78d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345787"
---
# <a name="mapi-object-and-interface-overview"></a><span data-ttu-id="8c382-103">Übersicht über das MAPI-Objekt und die Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="8c382-103">MAPI Object and Interface Overview</span></span>

  
  
<span data-ttu-id="8c382-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8c382-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8c382-105">Ein MAPI-Objekt ist eine C++-Objektklasse oder C-Datenstruktur, die von einer oder mehreren #A0 oder Auflistungen verwandter Funktionen geerbt wird.</span><span class="sxs-lookup"><span data-stu-id="8c382-105">A MAPI object is a C++ object class or C data structure inherited from one or more MAPI interfaces, or collections of related functions.</span></span> <span data-ttu-id="8c382-106">Diese Auflistungen verwandter Funktionen werden C++-Entwicklern als reine virtuelle Funktionen bekannt.</span><span class="sxs-lookup"><span data-stu-id="8c382-106">These collections of related functions are known to C++ developers as pure virtual functions.</span></span> <span data-ttu-id="8c382-107">Für eine reine virtuelle Funktion liefert MAPI nur den Funktionsprototyp, keine Implementierung.</span><span class="sxs-lookup"><span data-stu-id="8c382-107">For a pure virtual function, MAPI supplies only the function prototype, not an implementation.</span></span> <span data-ttu-id="8c382-108">Es wird erwartet, dass eine Clientanwendung, ein Dienstanbieter oder mapI diese Implementierung bereitstellen, indem eine Objektklasse erstellt wird, die von der Schnittstelle erbt und den Funktionsbeschreibungen der Messaging-API entspricht.</span><span class="sxs-lookup"><span data-stu-id="8c382-108">It is expected that a client application, a service provider, or MAPI will provide this implementation by creating an object class that inherits from the interface and conforms to the function descriptions of the Messaging API.</span></span> <span data-ttu-id="8c382-109">Eine MAPI-Schnittstelle kann nur über eine geerbte Klasse instanziiert werden.</span><span class="sxs-lookup"><span data-stu-id="8c382-109">A MAPI interface can be instantiated only through an inherited class.</span></span>
  
<span data-ttu-id="8c382-110">Es gibt viele verschiedene MAPI-Objekte, von der jedes Objekt von einer Schnittstelle erbt, die letztendlich von der [IUnknown-Schnittstelle geerbt](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) wird.</span><span class="sxs-lookup"><span data-stu-id="8c382-110">There are many different MAPI objects, each object inheriting from an interface that is ultimately inherited from the [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) interface.</span></span> <span data-ttu-id="8c382-111">**IUnknown** ist die BASISschnittstelle (OLE Component Object Model, COM).</span><span class="sxs-lookup"><span data-stu-id="8c382-111">**IUnknown** is the OLE Component Object Model (COM) base interface.</span></span> <span data-ttu-id="8c382-112">Es bietet MAPI-Objekten einen Standardmechanismus für Kommunikation und Kontrolle.</span><span class="sxs-lookup"><span data-stu-id="8c382-112">It provides MAPI objects with a standard mechanism for communication and control.</span></span> <span data-ttu-id="8c382-113">COM bestimmt, wie Objekt implementierer Probleme wie Speicherverwaltung, Parameterverwaltung und Multithreading behandeln.</span><span class="sxs-lookup"><span data-stu-id="8c382-113">COM dictates how object implementers handle issues such as memory management, parameter management, and multithreading.</span></span> <span data-ttu-id="8c382-114">Durch Die Konformität mit diesem Modell hält ein Objekt implementier einen Vertrag gemäß den Schnittstellen im Objekt angegeben.</span><span class="sxs-lookup"><span data-stu-id="8c382-114">By conforming to this model, an object implementer adheres to a contract as specified by the interfaces included in the object.</span></span> 
  
<span data-ttu-id="8c382-115">Viele MAPI-Schnittstellen werden direkt von **IUnknown** geerbt, während andere indirekt über eine von zwei anderen Basisschnittstellen geerbt werden: [IMAPIProp : IUnknown](imapipropiunknown.md) für die Eigenschaftenverwaltung und [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md) für den Ordner- und Adressbuchzugriff.</span><span class="sxs-lookup"><span data-stu-id="8c382-115">Many MAPI interfaces are inherited directly from **IUnknown**, while others are inherited indirectly through one of two other base interfaces: [IMAPIProp : IUnknown](imapipropiunknown.md) for property management and [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md) for folder and address book access.</span></span> <span data-ttu-id="8c382-116">Basisschnittstellen werden nie als separate, eigenständige Objekte implementiert. Sie werden immer als Teil anderer Objekte implementiert, objekte, die abgeleitete Schnittstellen implementieren.</span><span class="sxs-lookup"><span data-stu-id="8c382-116">Base interfaces are never implemented as separate, standalone objects; they are always implemented as part of other objects, objects that implement derived interfaces.</span></span> 
  
<span data-ttu-id="8c382-117">MAPI definiert viele Objekttypen, die jeweils von einer oder mehreren MAPI-Komponenten implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="8c382-117">MAPI defines many types of objects, each implemented by one or more MAPI components.</span></span> <span data-ttu-id="8c382-118">Von Clients implementierte Objekte werden von MAPI, von Dienstanbietern und von benutzerdefinierten Formularkomponenten verwendet.</span><span class="sxs-lookup"><span data-stu-id="8c382-118">Objects implemented by clients are used by MAPI, by service providers, and by custom form components.</span></span> <span data-ttu-id="8c382-119">Von Dienstanbietern implementierte Objekte werden in der Regel von MAPI und von Clients verwendet.</span><span class="sxs-lookup"><span data-stu-id="8c382-119">Objects implemented by service providers are typically used by MAPI and by clients.</span></span> <span data-ttu-id="8c382-120">Von Formularbibliotheksanbietern und Formularservern implementierte Objekte werden von anderen Formularkomponenten und von Clients verwendet.</span><span class="sxs-lookup"><span data-stu-id="8c382-120">Objects implemented by form library providers and form servers are used by other form components and by clients.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8c382-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8c382-121">See also</span></span>



[<span data-ttu-id="8c382-122">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8c382-122">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)
  
[<span data-ttu-id="8c382-123">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="8c382-123">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)


[<span data-ttu-id="8c382-124">MAPI-Konzepte (engl.)</span><span class="sxs-lookup"><span data-stu-id="8c382-124">MAPI Concepts</span></span>](mapi-concepts.md)

