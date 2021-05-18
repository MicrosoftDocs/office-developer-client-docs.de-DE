---
title: DateAdd-Funktion (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7174c585-86e1-42a3-bb7f-d6641001b0f2
description: Addiert zu dem angegebenen Datum die angegebene Anzahl von Intervallen (positive oder negative ganze Zahl) der angegebenen Datumskomponente und gibt das zugehörige Ergebnis zurück.
ms.openlocfilehash: 7cfd68c4983eee22a5e542facd72ea083deb3184
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423202"
---
# <a name="dateadd-function-access-custom-web-app"></a><span data-ttu-id="d2bde-103">DateAdd-Funktion (benutzerdefinierte Access-Web-App)</span><span class="sxs-lookup"><span data-stu-id="d2bde-103">DateAdd function (Access custom web app)</span></span>

<span data-ttu-id="d2bde-104">Addiert zu dem angegebenen Datum die angegebene Anzahl von Intervallen (positive oder negative ganze Zahl) der angegebenen Datumskomponente und gibt das zugehörige Ergebnis zurück.</span><span class="sxs-lookup"><span data-stu-id="d2bde-104">Returns a specified date with the specified number interval (positive or negative integer) added to a specified date part of that date.</span></span>
  
> [!NOTE]
> <span data-ttu-id="d2bde-p101">Die in diesem Artikel beschriebene Cloudspeicherfunktion wird in Office 2013 und Office 2016 nicht mehr unterstützt und kann dazu führen, dass die folgende Fehlermeldung angezeigt wird: >  *Leider bestehen Serverprobleme, sodass wir \<Dienst\> zurzeit nicht hinzufügen können. Bitte versuchen Sie es später erneut.* > Informationen zum Cloudspeicher für Office Online, Office für iOS und Office für Android finden Sie in unserem [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="d2bde-p101">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.* > For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="d2bde-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d2bde-107">Syntax</span></span>

<span data-ttu-id="d2bde-108">**DateAdd** (*DatePart*, *Number*, *Date*)</span><span class="sxs-lookup"><span data-stu-id="d2bde-108">**DateAdd** (*DatePart*, *Number*, *Date*)</span></span> 
  
<span data-ttu-id="d2bde-109">Die **DateAdd**-Funktion enthält die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="d2bde-109">The **DateAdd** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="d2bde-110">**Argumentname**</span><span class="sxs-lookup"><span data-stu-id="d2bde-110">**Argument name**</span></span>|<span data-ttu-id="d2bde-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d2bde-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="d2bde-112">*DatePart*</span><span class="sxs-lookup"><span data-stu-id="d2bde-112">*DatePart*</span></span>  <br/> |<span data-ttu-id="d2bde-p102">Die  *Date*  -Komponente, zu der eine ganze Zahl addiert wird. Eine Liste der zulässigen Einstellungen finden Sie im Abschnitt „Hinweise".  </span><span class="sxs-lookup"><span data-stu-id="d2bde-p102">The part of  *Date*  to which an integer number is added. Refer to the Remarks section for the list of valid settings.  </span></span><br/> |
| <span data-ttu-id="d2bde-115">*Number*</span><span class="sxs-lookup"><span data-stu-id="d2bde-115">*Number*</span></span>  <br/> |<span data-ttu-id="d2bde-p103">Ist ein Ausdruck, der in eine ganze Zahl aufgelöst werden kann, die zu der  *DatePart*  -Komponente von  *Date*  addiert wird. Wenn Sie einen Wert mit einem Dezimalbruch angeben, wird der Bruch gekürzt.  </span><span class="sxs-lookup"><span data-stu-id="d2bde-p103">Is an expression that can be resolved to an integer that is added to a  *DatePart*  of  *Date*  . If you specify a value with a decimal fraction, the fraction is truncated.  </span></span><br/> |
| <span data-ttu-id="d2bde-118">*Date*</span><span class="sxs-lookup"><span data-stu-id="d2bde-118">*Date*</span></span>  <br/> |<span data-ttu-id="d2bde-p104">Ein Ausdruck, der in einen Datums-/Uhrzeitwert aufgelöst werden kann. Der  *Date*  -Argumentausdruck, Spaltenausdruck, benutzerdefinierte Variable oder Zeichenfolgenliteral.  </span><span class="sxs-lookup"><span data-stu-id="d2bde-p104">An expression that can be resolved to a Date/Time value. The  *Date*  argument expression, column expression, user-defined variable or string literal.  </span></span><br/> |
   
## <a name="remarks"></a><span data-ttu-id="d2bde-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d2bde-121">Remarks</span></span>

<span data-ttu-id="d2bde-122">In der folgenden Tabelle werden alle zulässigen  *DatePart*  -Argumente aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="d2bde-122">The following table lists all valid  *DatePart*  arguments.</span></span> 
  
|<span data-ttu-id="d2bde-123">***DatePart***</span><span class="sxs-lookup"><span data-stu-id="d2bde-123">***DatePart***</span></span>|
|:-----|
|<span data-ttu-id="d2bde-124">**year**</span><span class="sxs-lookup"><span data-stu-id="d2bde-124">**year**</span></span> <br/> |
|<span data-ttu-id="d2bde-125">**quarter**</span><span class="sxs-lookup"><span data-stu-id="d2bde-125">**quarter**</span></span> <br/> |
|<span data-ttu-id="d2bde-126">**month**</span><span class="sxs-lookup"><span data-stu-id="d2bde-126">**month**</span></span> <br/> |
|<span data-ttu-id="d2bde-127">**dayofyear**</span><span class="sxs-lookup"><span data-stu-id="d2bde-127">**dayofyear**</span></span> <br/> |
|<span data-ttu-id="d2bde-128">**day**</span><span class="sxs-lookup"><span data-stu-id="d2bde-128">**day**</span></span> <br/> |
|<span data-ttu-id="d2bde-129">**week**</span><span class="sxs-lookup"><span data-stu-id="d2bde-129">**week**</span></span> <br/> |
|<span data-ttu-id="d2bde-130">**hour**</span><span class="sxs-lookup"><span data-stu-id="d2bde-130">**hour**</span></span> <br/> |
|<span data-ttu-id="d2bde-131">**minute**</span><span class="sxs-lookup"><span data-stu-id="d2bde-131">**minute**</span></span> <br/> |
|<span data-ttu-id="d2bde-132">**second**</span><span class="sxs-lookup"><span data-stu-id="d2bde-132">**second**</span></span> <br/> |
|<span data-ttu-id="d2bde-133">**millisecond**</span><span class="sxs-lookup"><span data-stu-id="d2bde-133">**millisecond**</span></span> <br/> |
   
## <a name="example"></a><span data-ttu-id="d2bde-134">Beispiel</span><span class="sxs-lookup"><span data-stu-id="d2bde-134">Example</span></span>

<span data-ttu-id="d2bde-135">Mit dem folgenden Ausdruck wird der letzte Tag des Monats berechnet.</span><span class="sxs-lookup"><span data-stu-id="d2bde-135">The following expression calculates the last day of the current month.</span></span>
  
`DateAdd(Day,-1,DateAdd(Month,DateDiff(Month,0,Today())+1,0))`

<span data-ttu-id="d2bde-136">Mit dem folgenden Ausdruck wird der letzte Tag des vorherigen Monats berechnet.</span><span class="sxs-lookup"><span data-stu-id="d2bde-136">The following expression calculates the last day of the previous month.</span></span>
  
`DateAdd(Day,-1,DateAdd(Month,DateDiff(Month,0,Today()),0))`


