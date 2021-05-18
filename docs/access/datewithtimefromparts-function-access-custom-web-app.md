---
title: DateWithTimeFromParts-Funktion (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: aa97cbaa-8b14-42e3-a098-938ebe0769eb
description: Gibt ein Datum und eine Uhrzeit basierend auf einem angegebenen Jahr, Monat, Tag und Uhrzeit zurück.
ms.openlocfilehash: ee995d346ca27e683f342cf3f611c1147997d24e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422089"
---
# <a name="datewithtimefromparts-function-access-custom-web-app"></a><span data-ttu-id="d37a4-103">DateWithTimeFromParts-Funktion (benutzerdefinierte Access-Web-App)</span><span class="sxs-lookup"><span data-stu-id="d37a4-103">DateWithTimeFromParts function (Access custom web app)</span></span>

<span data-ttu-id="d37a4-104">Gibt ein Datum und eine Uhrzeit basierend auf einem angegebenen Jahr, Monat, Tag und Uhrzeit zurück.</span><span class="sxs-lookup"><span data-stu-id="d37a4-104">Returns a Date and Time based on a specified year, month, day, and time.</span></span>
  
> [!NOTE]
> <span data-ttu-id="d37a4-p101">Die in diesem Artikel beschriebene Cloudspeicherfunktion wird in Office 2013 und Office 2016 nicht mehr unterstützt und kann dazu führen, dass die folgende Fehlermeldung angezeigt wird: >  *Leider bestehen Serverprobleme, sodass wir \<Dienst\> zurzeit nicht hinzufügen können. Bitte versuchen Sie es später erneut.* > Informationen zum Cloudspeicher für Office Online, Office für iOS und Office für Android finden Sie in unserem [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="d37a4-p101">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.* > For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="d37a4-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d37a4-107">Syntax</span></span>

<span data-ttu-id="d37a4-108">**DateWithTimeFromParts** (*Year*, *Month*, *Day*, *Hour*, *Minute*, *Second*)</span><span class="sxs-lookup"><span data-stu-id="d37a4-108">**DateWithTimeFromParts** (*Year*, *Month*, *Day*, *Hour*, *Minute*, *Second*)</span></span> 
  
<span data-ttu-id="d37a4-109">Die **DateWithTimeFromParts-Funktion** enthält die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="d37a4-109">The **DateWithTimeFromParts** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="d37a4-110">**Argumentname**</span><span class="sxs-lookup"><span data-stu-id="d37a4-110">**Argument name**</span></span>|<span data-ttu-id="d37a4-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d37a4-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="d37a4-112">*Jahr*</span><span class="sxs-lookup"><span data-stu-id="d37a4-112">*Year*</span></span>  <br/> |<span data-ttu-id="d37a4-113">Ganzzahliger Ausdruck, der ein Jahr an gibt.</span><span class="sxs-lookup"><span data-stu-id="d37a4-113">Integer expression specifying a year.</span></span>  <br/> |
| <span data-ttu-id="d37a4-114">*Month*</span><span class="sxs-lookup"><span data-stu-id="d37a4-114">*Month*</span></span>  <br/> |<span data-ttu-id="d37a4-115">Ganzzahliger Ausdruck, der einen Monat an gibt.</span><span class="sxs-lookup"><span data-stu-id="d37a4-115">Integer expression specifying a month.</span></span>  <br/> |
| <span data-ttu-id="d37a4-116">*Day*</span><span class="sxs-lookup"><span data-stu-id="d37a4-116">*Day*</span></span>  <br/> |<span data-ttu-id="d37a4-117">Ganzzahliger Ausdruck, der einen Tag an gibt.</span><span class="sxs-lookup"><span data-stu-id="d37a4-117">Integer expression specifying a day.</span></span>  <br/> |
| <span data-ttu-id="d37a4-118">*Hour*</span><span class="sxs-lookup"><span data-stu-id="d37a4-118">*Hour*</span></span>  <br/> |<span data-ttu-id="d37a4-119">Ganzzahliger Ausdruck, der Stunden an gibt.</span><span class="sxs-lookup"><span data-stu-id="d37a4-119">Integer expression specifying hours.</span></span>  <br/> |
| <span data-ttu-id="d37a4-120">*Minute*</span><span class="sxs-lookup"><span data-stu-id="d37a4-120">*Minute*</span></span>  <br/> |<span data-ttu-id="d37a4-121">Ganzzahliger Ausdruck, der Minuten an gibt.</span><span class="sxs-lookup"><span data-stu-id="d37a4-121">Integer expression specifying minutes.</span></span>  <br/> |
| <span data-ttu-id="d37a4-122">*Zweiter*</span><span class="sxs-lookup"><span data-stu-id="d37a4-122">*Second*</span></span>  <br/> |<span data-ttu-id="d37a4-123">Ganzzahliger Ausdruck, der Sekunden an gibt.</span><span class="sxs-lookup"><span data-stu-id="d37a4-123">Integer expression specifying seconds.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d37a4-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d37a4-124">Remarks</span></span>

<span data-ttu-id="d37a4-125">**DateWithTimeFromParts gibt** einen vollständig initialisierten Date/Time-Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="d37a4-125">**DateWithTimeFromParts** returns a fully initialized Date/Time value.</span></span> <span data-ttu-id="d37a4-126">Wenn die Argumente ungültig sind, wird ein Fehler ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="d37a4-126">If the arguments are not valid, an error is raised.</span></span> <span data-ttu-id="d37a4-127">Wenn erforderliche Argumente Null sind, wird Null zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d37a4-127">If required arguments are Null, then Null is returned.</span></span> 
  

