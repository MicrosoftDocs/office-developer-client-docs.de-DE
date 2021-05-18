---
title: PidTagNextSendAcct
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 1cf5b314-39fa-996f-fd88-00380ffbc4de
description: Gibt den sekundären Accountsendstamp für die Nachricht an.
ms.openlocfilehash: 3aa88a1fd5a73cc4ae2e990e6dad0697083bb694
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327713"
---
# <a name="pidtagnextsendacct"></a><span data-ttu-id="f02f0-103">PidTagNextSendAcct</span><span class="sxs-lookup"><span data-stu-id="f02f0-103">PidTagNextSendAcct</span></span>

<span data-ttu-id="f02f0-104">Gibt den sekundären Kontostempel "Senden" für die Nachricht an.</span><span class="sxs-lookup"><span data-stu-id="f02f0-104">Specifies the secondary account "send" stamp for the message.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="f02f0-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="f02f0-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f02f0-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="f02f0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f02f0-107">PR_NEXT_SEND_ACCT</span><span class="sxs-lookup"><span data-stu-id="f02f0-107">PR_NEXT_SEND_ACCT</span></span>  <br/> |
|<span data-ttu-id="f02f0-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="f02f0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f02f0-109">0x0E29</span><span class="sxs-lookup"><span data-stu-id="f02f0-109">0x0E29</span></span>  <br/> |
|<span data-ttu-id="f02f0-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="f02f0-110">Data type:</span></span>  <br/> |<span data-ttu-id="f02f0-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f02f0-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="f02f0-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="f02f0-112">Area:</span></span>  <br/> |<span data-ttu-id="f02f0-113">Outlook-Anwendung</span><span class="sxs-lookup"><span data-stu-id="f02f0-113">Outlook application</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f02f0-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f02f0-114">Remarks</span></span>

<span data-ttu-id="f02f0-115">Diese Eigenschaft gilt für ein MAPI-Nachrichtenobjekt.</span><span class="sxs-lookup"><span data-stu-id="f02f0-115">This property applies to a MAPI message object.</span></span> <span data-ttu-id="f02f0-116">Für eine empfangene Nachricht gibt der sekundäre Kontostempel "Senden" an, mit welchem Konto ein Forward oder eine Antwort gesendet werden soll, wenn die Weiterleitung oder Antwort nicht mit dem primären Konto gesendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="f02f0-116">For a received message, the secondary account "send" stamp indicates which account a forward or a reply should be sent with, if the forward or reply cannot be sent with the primary account.</span></span> <span data-ttu-id="f02f0-117">Für eine ausgehende Nachricht bestimmt der sekundäre Kontostempel "Senden", mit welchem Konto die Nachricht gesendet werden soll, wenn die Nachricht nicht mit dem primären Konto gesendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="f02f0-117">For an outgoing message, the secondary account "send" stamp determines with which account to send the message, if the message cannot be sent with the primary account.</span></span> <span data-ttu-id="f02f0-118">Der Wert ist der [PROP_ACCT_SEND_STAMP](prop_acct_send_stamp.md) von der [IOlkAccount-Schnittstelle](iolkaccount.md) des Kontos, mit dem die Nachricht gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="f02f0-118">Its value is the [PROP_ACCT_SEND_STAMP](prop_acct_send_stamp.md) value from the [IOlkAccount](iolkaccount.md) interface of the account with which the message is being sent.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f02f0-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f02f0-119">See also</span></span>

- [<span data-ttu-id="f02f0-120">Konstanten (Account Management API)</span><span class="sxs-lookup"><span data-stu-id="f02f0-120">Constants (Account management API)</span></span>](constants-account-management-api.md)
- [<span data-ttu-id="f02f0-121">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f02f0-121">MAPI Properties</span></span>](https://msdn.microsoft.com/library/3b980217-b65b-442b-8c18-b8b9f3ff487a%28Office.15%29.aspx) 
- [<span data-ttu-id="f02f0-122">PidTagNextSendAcct (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="f02f0-122">PidTagNextSendAcct Canonical Property</span></span>](https://msdn.microsoft.com/library/b7429c2e-0d9d-4921-9f56-9ecad817f8cb%28Office.15%29.aspx)

