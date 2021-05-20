---
title: ITnefEncodeRecips
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITnef.EncodeRecips
api_type:
- COM
ms.assetid: b3ce4b0e-4f48-4a7e-a30c-c4754bccb12c
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: d8caa503e557d35e259db743505d39ea4809dbfd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437651"
---
# <a name="itnefencoderecips"></a>ITnef::EncodeRecips

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Codiert eine Ansicht für die Empfängertabelle einer Nachricht im Transport-Neutral Encapsulation Format (TNEF)-Datenstrom für die Nachricht.
  
```cpp
HRESULT EncodeRecips(
  ULONG ulFlags,
  LPMAPITABLE lpRecipientTable
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> [in] Reserviert. NULL muss sein.
    
 _lpRecipientTable_
  
> [in] Ein Zeiger auf die Empfängertabelle, für die die Ansicht codiert ist. Der  _lpRecipientTable-Parameter_ kann NULL sein. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf war erfolgreich und hat den erwarteten Wert oder die erwarteten Werte zurückgegeben.
    
## <a name="remarks"></a>Hinweise

Transportanbieter, Nachrichtenspeicheranbieter und Gateways rufen die **ITnef::EncodeRecips-Methode** auf, um die TNEF-Codierung für eine bestimmte Empfängertabellesansicht durchzuführen. Die TNEF-Codierung ist z. B. hilfreich, wenn ein Anbieter oder Gateway einen bestimmten Spaltensatz, eine Sortierreihenfolge oder eine Einschränkung für die Empfängertabelle erfordert. 
  
Ein Anbieter oder Gateway übergibt die Tabellenansicht, die im  _lpRecipientTable-Parameter codiert werden_ soll. Die TNEF-Implementierung codiert die Empfängertabelle mit der angegebenen Ansicht mithilfe der angegebenen Spaltensatz, Sortierreihenfolge, Einschränkung und Position. Wenn ein Anbieter oder Gateway NULL in  _lpRecipientTable_ übergibt, ruft TNEF die Empfängertabelle aus der Nachricht ab, die mithilfe der [IMessage::GetRecipientTable-Methode](imessage-getrecipienttable.md) codiert wird, und verarbeitet jede Zeile der Tabelle mithilfe der aktuellen Einstellungen der Tabelle in den TNEF-Stream. 
  
Das Aufrufen von **EncodeRecips** mit NULL in _lpRecipientTable_ codiert daher alle Nachrichtenempfänger und entspricht dem Aufrufen der [ITnef::AddProps-Methode](itnef-addprops.md) mit dem TNEF_PROP_INCLUDE-Flag im _ulFlags-Parameter_ und der **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))-Eigenschaft im _lpPropList-Parameter._ 
  
Beachten Sie, dass es selten erforderlich **ist, EncodeRecips** aufzugeben, es sei denn, es ist erforderlich, eine bestimmte Empfängertabelle zu codieren. Fremde Messagingsysteme verfügen fast immer über Möglichkeiten zum Behandeln von Empfängerlisten, die leistungsfähig genug sind, um die allgemeinen Anforderungen der Codierung von Empfängerlisten zu erfüllen. Daher benötigen diese Systeme zu diesem Zweck fast nie TNEF. 
  
## <a name="see-also"></a>Siehe auch



[IMessage::GetRecipientTable](imessage-getrecipienttable.md)
  
[ITnef::AddProps](itnef-addprops.md)
  
[PidTagMessageRecipients (kanonische Eigenschaft)](pidtagmessagerecipients-canonical-property.md)
  
[ITnef : IUnknown](itnefiunknown.md)

