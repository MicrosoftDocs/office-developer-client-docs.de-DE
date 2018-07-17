---
title: DECIMALSEP-Funktion
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251883
localization_priority: Normal
ms.assetid: 091fe401-05b2-464f-9333-7bb7118cd7cd
description: Gibt das Dezimaltrennzeichen für das Gebietsschema des aktuellen Benutzers zurück.
ms.openlocfilehash: a47bc20702262ab7d4a072694c36e424e6949919
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796819"
---
# <a name="decimalsep-function"></a><span data-ttu-id="d0976-103">DECIMALSEP Function</span><span class="sxs-lookup"><span data-stu-id="d0976-103">DECIMALSEP Function</span></span>

<span data-ttu-id="d0976-104">Gibt das Dezimaltrennzeichen für das Gebietsschema des aktuellen Benutzers zurück.</span><span class="sxs-lookup"><span data-stu-id="d0976-104">Returns the decimal separator string for the current user locale.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="d0976-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d0976-105">Syntax</span></span>

<span data-ttu-id="d0976-106">DECIMALSEP( )</span><span class="sxs-lookup"><span data-stu-id="d0976-106">DECIMALSEP( )</span></span>
  
## <a name="example"></a><span data-ttu-id="d0976-107">Beispiel</span><span class="sxs-lookup"><span data-stu-id="d0976-107">Example</span></span>

<span data-ttu-id="d0976-108">SETF(GETREF(User.Size), Benutzer.wholepart &amp; DECIMALSEP() &amp; Benutzer.fracpart)</span><span class="sxs-lookup"><span data-stu-id="d0976-108">SETF(GETREF(user.size), user.wholePart &amp; DECIMALSEP() &amp; user.fracPart)</span></span> 
  
