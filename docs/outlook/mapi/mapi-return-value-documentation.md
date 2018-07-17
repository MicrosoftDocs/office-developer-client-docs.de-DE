---
title: MAPI-Rückgabewert Dokumentation
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c32ee53c-b063-4a00-a6bf-75ce5e07f56a
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: f2b8f87987f93ec152d4986131a6b7990273c28d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793072"
---
# <a name="mapi-return-value-documentation"></a><span data-ttu-id="a71da-103">MAPI-Rückgabewert Dokumentation</span><span class="sxs-lookup"><span data-stu-id="a71da-103">MAPI Return Value Documentation</span></span>

  
  
<span data-ttu-id="a71da-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a71da-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a71da-105">Der Verweis Einträge in dieser Referenz des Dokuments nur diese Werte zurückgeben, die einige Behandlung von Clientanwendungen erfordern.</span><span class="sxs-lookup"><span data-stu-id="a71da-105">The reference entries in this Reference document only those return values that require some handling by client applications.</span></span> <span data-ttu-id="a71da-106">Rückgabewerte, die allgemeine fehlerbedingungen anzugeben und Mobilgeräts auf eventuelle Fehler abgeleitet werden können, sind nicht in der Dokumentation enthalten.</span><span class="sxs-lookup"><span data-stu-id="a71da-106">Return values that indicate common error conditions and can be deduced by checking for failure are not included in the documentation.</span></span> <span data-ttu-id="a71da-107">Beispielsweise können viele Schnittstellenmethoden MAPI_E_INVALID_PARAMETER zurück, wenn ein Anrufer gibt den falschen Wert für einen Eingabeparameter an.</span><span class="sxs-lookup"><span data-stu-id="a71da-107">For example, many interface methods can return MAPI_E_INVALID_PARAMETER if a caller specifies the wrong value for an input parameter.</span></span> <span data-ttu-id="a71da-108">Dieser Wert wird in der Regel nicht in den erwarteten Rückgabewerte aufgeführt, weil es muss speziell für MAPI_E_INVALID_PARAMETER und müssen nicht anders aus einem anderen Fehler die Verarbeitung.</span><span class="sxs-lookup"><span data-stu-id="a71da-108">This value is typically not listed in the set of expected return values because there is no need to look specifically for MAPI_E_INVALID_PARAMETER and no need to process it differently from any other error.</span></span> <span data-ttu-id="a71da-109">Andererseits, einige Dienstanbieter unterstützen keine Benachrichtigung und MAPI_E_NO_SUPPORT an die Clients über **IMAPISession**vorgenommene **Advise** -Methode zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="a71da-109">On the other hand, some service providers do not support event notification and will return MAPI_E_NO_SUPPORT to the **Advise** method made by clients through **IMAPISession**.</span></span> <span data-ttu-id="a71da-110">Da Clients müssen explizit für diesen Wert überprüfen und bereitstellen, sollten Code für die Behandlung der Bedingung, die es darstellt es tritt auf, MAPI_E_NO_SUPPORT ist in der Liste der Rückgabewerte für [IMAPISession::Advise](imapisession-advise.md)enthalten.</span><span class="sxs-lookup"><span data-stu-id="a71da-110">Because clients need to explicitly check for this value and provide code for handling the condition that it represents should it occur, MAPI_E_NO_SUPPORT is included in the list of return values for [IMAPISession::Advise](imapisession-advise.md).</span></span>
  
<span data-ttu-id="a71da-111">In der folgenden Tabelle werden die Fehlerwerte, die häufig von Methoden und Funktionen zurückgegeben werden und erfordern explizite Behandlung durch einen Client oder Dienstanbieter beschrieben.</span><span class="sxs-lookup"><span data-stu-id="a71da-111">The following table describes error values that are commonly returned from methods and functions and require explicit handling on the part of a client or service provider.</span></span> <span data-ttu-id="a71da-112">Diese Werte werden in vier Kategorien unterteilt: Werte, die ungültige Eingabedaten angeben, Werte, die Ressourcenprobleme hinweisen, Werte, die angeben, Zeichensatz Inkompatibilität und Werte, die Ausfall eines unbekannten Ursprungs angeben.</span><span class="sxs-lookup"><span data-stu-id="a71da-112">These values fall into four categories: values that indicate invalid input data, values that indicate resource problems, values that indicate character set incompatibility, and values that indicate failure of an unknown origin.</span></span>
  
|<span data-ttu-id="a71da-113">**Rückgabewert**</span><span class="sxs-lookup"><span data-stu-id="a71da-113">**Return value**</span></span>|<span data-ttu-id="a71da-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a71da-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a71da-115">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="a71da-115">MAPI_E_INVALID_PARAMETER</span></span>  <br/> |<span data-ttu-id="a71da-116">Eine oder mehrere der Parameter an die Methode übergebenen oder Funktionen sind nicht gültig.</span><span class="sxs-lookup"><span data-stu-id="a71da-116">One or more of the parameters passed into the method or functions were not valid.</span></span>  <br/> |
|<span data-ttu-id="a71da-117">MAPI_E_UNKNOWN_FLAGS</span><span class="sxs-lookup"><span data-stu-id="a71da-117">MAPI_E_UNKNOWN_FLAGS</span></span>  <br/> |<span data-ttu-id="a71da-118">Eine oder mehrere Werte für Flags-Parameter sind ungültig.</span><span class="sxs-lookup"><span data-stu-id="a71da-118">One or more values for a flags parameter were not valid.</span></span>  <br/> |
|<span data-ttu-id="a71da-119">MAPI_E_DISK_ERROR</span><span class="sxs-lookup"><span data-stu-id="a71da-119">MAPI_E_DISK_ERROR</span></span>  <br/> |<span data-ttu-id="a71da-120">Es wurde ein Problem beim Schreiben in oder Lesen vom Datenträger.</span><span class="sxs-lookup"><span data-stu-id="a71da-120">There was a problem writing to or reading from disk.</span></span>  <br/> |
|<span data-ttu-id="a71da-121">MAPI_E_NOT_ENOUGH_DISK</span><span class="sxs-lookup"><span data-stu-id="a71da-121">MAPI_E_NOT_ENOUGH_DISK</span></span>  <br/> |<span data-ttu-id="a71da-122">Es war nicht genügend Speicherplatz zum Abschließen des Vorgangs verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a71da-122">Not enough disk space was available to complete the operation.</span></span>  <br/> |
|<span data-ttu-id="a71da-123">MAPI_E_NOT_ENOUGH_MEMORY</span><span class="sxs-lookup"><span data-stu-id="a71da-123">MAPI_E_NOT_ENOUGH_MEMORY</span></span>  <br/> |<span data-ttu-id="a71da-124">Es ist nicht genügend Arbeitsspeicher verfügbar, um den Vorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="a71da-124">Not enough memory was available to complete the operation.</span></span>  <br/> |
|<span data-ttu-id="a71da-125">MAPI_E_NOT_ENOUGH_RESOURCES</span><span class="sxs-lookup"><span data-stu-id="a71da-125">MAPI_E_NOT_ENOUGH_RESOURCES</span></span>  <br/> |<span data-ttu-id="a71da-126">Nicht genügend Systemressourcen waren zum Abschließen des Vorgangs verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a71da-126">Not enough system resources were available to complete the operation.</span></span>  <br/> |
|<span data-ttu-id="a71da-127">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="a71da-127">MAPI_E_BAD_CHARWIDTH</span></span>  <br/> |<span data-ttu-id="a71da-128">Eine Inkompatibilität vorhanden ist, in die Zeichensätze, die von dem Anrufer und der Implementierung unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="a71da-128">An incompatibility exists in the character sets supported by the caller and the implementation.</span></span>  <br/> |
|<span data-ttu-id="a71da-129">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="a71da-129">MAPI_E_CALL_FAILED</span></span>  <br/> |<span data-ttu-id="a71da-130">Unerwarteter oder unbekannten Ursprungs ein Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="a71da-130">An error of unexpected or unknown origin occurred.</span></span>  <br/> |
   
<span data-ttu-id="a71da-131">Die Konstanten, die MAPI-Rückgabewerte darstellen, sind in der MAPICODE aufgeführt. H-Headerdatei.</span><span class="sxs-lookup"><span data-stu-id="a71da-131">The constants that represent MAPI return values are listed in the MAPICODE.H header file.</span></span> <span data-ttu-id="a71da-132">Einige der Konstanten zuordnen zu Win32-Fehler; die Zuordnung der folgenden Konstanten für numerische Werte kann in der Win32-Headerdatei WINERROR gefunden werden. H.</span><span class="sxs-lookup"><span data-stu-id="a71da-132">Some of the constants map to Win32 errors; the mapping of these constants to numeric values can be found in the Win32 header file, WINERROR.H.</span></span>
  
<span data-ttu-id="a71da-133">Fehler bezüglich ungültige Daten vom Anrufer übergebene können über entweder den Parameter Validierung API bereitgestellten Funktionen MAPI oder eine Gruppe von Makros ermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="a71da-133">Errors regarding invalid data passed in by a caller can be determined through either the parameter validation API functions provided by MAPI or a set of macros.</span></span> 
  
<span data-ttu-id="a71da-134">Character Set Inkompatibilität tritt auf, wenn eine der folgenden Situationen auftritt:</span><span class="sxs-lookup"><span data-stu-id="a71da-134">Character set incompatibility arises when either of the following situations occurs:</span></span>
  
- <span data-ttu-id="a71da-135">Ein Client oder Dienstanbieter legt die Option MAPI_UNICODE bei einem Aufruf-Methode oder die Funktion, und die Implementierung Unicode nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a71da-135">A client or service provider sets the MAPI_UNICODE flag on a method or function call and the implementation does not support Unicode.</span></span> <span data-ttu-id="a71da-136">Festlegen von Parameter MAPI_UNICODE gibt an, dass Zeichenfolgen, die als Eingabe übergebenen Unicode-Zeichenfolgen und Zeichenfolgen übergeben wieder als Ausgabe erwartet werden Unicode-Zeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="a71da-136">Setting MAPI_UNICODE indicates that character strings passed in as input are Unicode strings and that character strings passed back as output are expected to be Unicode strings.</span></span>
    
- <span data-ttu-id="a71da-137">Ein Client oder Dienstanbieter wird die Option MAPI_UNICODE ein Gespräch über eine Methode oder Funktion nicht festgelegt, und die Implementierung unterstützt nur Unicode.</span><span class="sxs-lookup"><span data-stu-id="a71da-137">A client or service provider does not set the MAPI_UNICODE flag on a method or function call and the implementation only supports Unicode.</span></span>
    
