---
title: Transport-Neutral Encapsulation Format (TNEF)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 98d4fe3c-3908-4cd2-bfdb-ff1874a80b24
description: 'Letzte Änderung: 12. März 2013'
ms.openlocfilehash: d902039fa1081e30947ddd8f70ead9ae7acec06a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428690"
---
# <a name="transport-neutral-encapsulation-format-tnef"></a><span data-ttu-id="d570f-103">Transport-Neutral Encapsulation Format (TNEF)</span><span class="sxs-lookup"><span data-stu-id="d570f-103">Transport-Neutral Encapsulation Format (TNEF)</span></span>

 
  
<span data-ttu-id="d570f-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d570f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d570f-105">TNEF ist ein Format zur Konvertierung einer Reihe von MAPI-Eigenschaften – einer MAPI-Nachricht – in einen seriellen Datenstrom.</span><span class="sxs-lookup"><span data-stu-id="d570f-105">TNEF is a format for converting a set of MAPI properties—a MAPI message—into a serial data stream.</span></span> <span data-ttu-id="d570f-106">Die TNEF-Funktionen werden hauptsächlich von Transportanbietern verwendet, die MAPI-Nachrichteneigenschaften für die Übertragung über ein Messagingsystem codieren müssen, das diese Eigenschaften nicht direkt unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d570f-106">The TNEF functions are primarily used by transport providers that need to encode MAPI message properties for transmission through a messaging system that does not support those properties directly.</span></span> <span data-ttu-id="d570f-107">Beispielsweise verwendet ein SMTP-basierter Transport TNEF zum Codieren von Eigenschaften wie **PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md)), die keine direkten Darstellungen in der Struktur einer #A0 aufweisen.</span><span class="sxs-lookup"><span data-stu-id="d570f-107">For example, an SMTP-based transport uses TNEF to encode properties like **PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md)), which do not have direct representations in the structure of an SMTP message.</span></span>
  
<span data-ttu-id="d570f-108">Die TNEF-Implementierung definiert mehrere TNEF-spezifische Attribute, von denen jedes einer bestimmten MAPI-Eigenschaft entspricht.</span><span class="sxs-lookup"><span data-stu-id="d570f-108">The TNEF implementation defines several TNEF-specific attributes, each of which corresponds to a particular MAPI property.</span></span> <span data-ttu-id="d570f-109">Diese Attribute werden verwendet, um ihre jeweiligen MAPI-Eigenschaften in den TNEF-Stream zu codieren.</span><span class="sxs-lookup"><span data-stu-id="d570f-109">These attributes are used to encode their respective MAPI properties into the TNEF stream.</span></span> <span data-ttu-id="d570f-110">Darüber hinaus wird ein spezielles Attribut definiert, das zum Kapseln einer beliebigen MAPI-Eigenschaft verwendet werden kann, die nicht über ein bestimmtes Attribut verfügt, das ihr entspricht.</span><span class="sxs-lookup"><span data-stu-id="d570f-110">In addition, a special attribute is defined that can be used to encapsulate any MAPI property that does not have a specific attribute corresponding to it.</span></span> <span data-ttu-id="d570f-111">Der Grund, warum diese Attribute definiert werden – anstatt einfach eine einheitliche Codierungsmethode für alle MAPI-Eigenschaften zu verwenden – besteht in der Aktivierung der Abwärtskompatibilität mit nicht MAPI-kompatibler Software, die TNEF verwendet.</span><span class="sxs-lookup"><span data-stu-id="d570f-111">The reason these attributes are defined — instead of simply using a uniform encoding method for all MAPI properties — is to enable backward compatibility with non-MAPI-compliant software that is using TNEF.</span></span>
  
<span data-ttu-id="d570f-112">Im restlichen Teil dieses Abschnitts werden die Struktur und Syntax eines TNEF-Datenstroms, die Zuordnung zwischen #A0 und TNEF-Attributen sowie wichtige Überlegungen für bestimmte #A1 beschrieben.</span><span class="sxs-lookup"><span data-stu-id="d570f-112">The remainder of this section describes the structure and syntax of a TNEF stream, the mapping between MAPI properties and TNEF attributes, and important considerations for certain TNEF attributes.</span></span>
  

