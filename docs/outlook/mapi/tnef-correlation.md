---
title: TNEF-Korrelation
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 93d1716d-a0be-45aa-85d2-6c9be65f5fd2
description: 'Letzte Änderung: 12. März 2013'
ms.openlocfilehash: 8d601bb2bbc65e21c5bc83179cc29e53ddd33876
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410371"
---
# <a name="tnef-correlation"></a><span data-ttu-id="9d8fd-103">TNEF-Korrelation</span><span class="sxs-lookup"><span data-stu-id="9d8fd-103">TNEF Correlation</span></span>

 
  
<span data-ttu-id="9d8fd-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9d8fd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9d8fd-105">Einige Messagingsysteme führen eine Korrelationsprüfung für jeden Transport-Neutral Encapsulation Format (TNEF)-Stream durch, der an eine eingehende Nachricht angefügt ist, um sicherzustellen, dass der TNEF-Stream tatsächlich zu dieser Nachricht gehört.</span><span class="sxs-lookup"><span data-stu-id="9d8fd-105">Some messaging systems perform a correlation check on any Transport-Neutral Encapsulation Format (TNEF) stream attached to an inbound message to verify that the TNEF stream does in fact belong to that message.</span></span> <span data-ttu-id="9d8fd-106">Dazu muss der Wert eines Felds in der Kopfzeile der eingehenden Nachricht mit einer Kopie dieses Werts übereinstimmen, die in einer Eigenschaft im TNEF-Stream gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="9d8fd-106">This involves matching the value of some field in the header of the inbound message with a copy of that value stored in some property in the TNEF stream.</span></span> <span data-ttu-id="9d8fd-107">Werte, die für jede Nachricht wahrscheinlich eindeutig sind, z. B. Nachrichten-ID-Nummern, werden in der Regel dafür verwendet.</span><span class="sxs-lookup"><span data-stu-id="9d8fd-107">Values that are presumably unique for each message, such as message ID numbers, are typically used for this.</span></span> <span data-ttu-id="9d8fd-108">Der Transport oder das Gateway, mit dem der TNEF-Stream erstellt wurde, ist dafür verantwortlich, einen geeigneten Wert aus dem Nachrichtenkopf zu wählen und eine Kopie in eine entsprechende Eigenschaft zu platzieren, bevor die Eigenschaften der ausgehenden Nachricht in den TNEF-Stream codiert werden.</span><span class="sxs-lookup"><span data-stu-id="9d8fd-108">The transport or gateway that created the TNEF stream is responsible for choosing an appropriate value from the message header and placing a copy into an appropriate property before encoding the outgoing message's properties into the TNEF stream.</span></span> <span data-ttu-id="9d8fd-109">Gateways oder Transporte, die die Nachricht empfangen, können diese Eigenschaft dann aus dem TNEF-Stream extrahieren und überprüfen, ob ihr Wert dem Wert des entsprechenden Kopfzeilenfelds für die eingehende Nachricht entspricht.</span><span class="sxs-lookup"><span data-stu-id="9d8fd-109">Gateways or transports that receive the message can then extract that property from the TNEF stream and verify that its value matches the value of the corresponding header field on the inbound message.</span></span>
  
<span data-ttu-id="9d8fd-110">Wenn die Werte nicht übereinstimmen, sollte das Gateway oder der Transport den TNEF-Stream verwerfen und nur den systemeigenen Nachrichtenumschlag verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="9d8fd-110">If the values do not match, the gateway or transport should discard the TNEF stream and process only the native message envelope.</span></span> <span data-ttu-id="9d8fd-111">Solche Prüfungen sind sinnvoll, da nicht MAPI-basierte E-Mail-Clients eine Datei anfügen können, die einen #A0 aus einer alten Nachricht an eine Weiterleitung oder gar eine nicht zusammenhängende Nachricht enthält. Wenn diese Option nicht aktiviert ist, kann ein solcher Fehler den Nachrichtentextverlust verursachen.</span><span class="sxs-lookup"><span data-stu-id="9d8fd-111">Such checks are prudent because non-MAPI-based mail clients may attach a file that contains a TNEF stream from an old message to a forwarding or even an unrelated message; if not checked, such an error may cause the loss of message text.</span></span>
  
<span data-ttu-id="9d8fd-112">Der ausgewählte Kopfzeilenfeldwert muss für die Nachricht eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="9d8fd-112">The header field value chosen must be unique to the message.</span></span> <span data-ttu-id="9d8fd-113">Es gibt kein festes Kopfzeilenfeld für alle Messagingsysteme, da unterschiedliche Messagingsysteme unterschiedliche Kopfzeilenfelder verwenden, aber in der Regel weist das Messagingsystem der Nachricht einen eindeutigen Bezeichner zu, der für diesen Zweck geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="9d8fd-113">There is no fixed header field for all messaging systems because different messaging systems use different header fields, but typically the messaging system assigns a unique identifier to the message which is suitable for this purpose.</span></span> <span data-ttu-id="9d8fd-114">Beispielsweise verwenden SMTP-Systeme in der Regel den MessageID-Header, während X.400-Systeme in der Regel das IM_THIS_IPM verwenden.</span><span class="sxs-lookup"><span data-stu-id="9d8fd-114">For example, SMTP systems typically use the MessageID header, while X.400 systems typically use the IM_THIS_IPM attribute.</span></span>
  

