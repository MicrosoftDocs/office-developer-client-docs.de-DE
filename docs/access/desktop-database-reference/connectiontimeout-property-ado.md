---
title: ConnectionTimeout-Eigenschaft (ADO)
TOCTitle: ConnectionTimeout Property (ADO)
ms:assetid: efc39fd8-afce-5ac0-2fff-cbb55c1a444d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250218(v=office.15)
ms:contentKeyID: 48548589
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 375af7f4dc84d1a630c290df1c38e77ee6580b5d
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473907"
---
# <a name="connectiontimeout-property-ado"></a>ConnectionTimeout-Eigenschaft (ADO)


**Betrifft**: Access 2013 | Office 2013

Gibt an, wie lange beim Einrichten einer Verbindung gewartet wird, bis der Versuch beendet und ein Fehler generiert wird.

## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte

Mit dieser Eigenschaft wird ein Wert vom Datentyp Long festgelegt oder zurückgegeben, der angibt, wie viele Sekunden gewartet werden soll, bis die Verbindung geöffnet wird. Der Standard ist 15.

## <a name="remarks"></a>Hinweise

Verwenden Sie die **ConnectionTimeout** -Eigenschaft für ein [Connection](connection-object-ado.md) -Objekt Wenn Verzögerungen von Datenverkehr oder fett Netzwerkserver verwenden es erforderlich machen, einen Verbindungsversuch zu verlassen. Wenn das von der Einstellung der **ConnectionTimeout** -Eigenschaft vor dem Öffnen der Verbindung verstrichen, tritt ein Fehler auf, und ADO bricht den Versuch ab. Wenn Sie die Eigenschaft auf 0 (null) festlegen, wartet ADO unbegrenzt, bis die Verbindung geöffnet wird. Stellen Sie sicher, dass der Anbieter, den Sie Code schreiben, die **ConnectionTimeout** -Funktionalität unterstützt.

Die **ConnectionTimeout** -Eigenschaft hat Lese-/Schreibzugriff, wenn die Verbindung geschlossen ist. Wenn die Verbindung geöffnet ist, ist sie schreibgeschützt.
