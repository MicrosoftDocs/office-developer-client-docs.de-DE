---
title: CommandTimeout-Eigenschaft (ADO)
TOCTitle: CommandTimeout Property (ADO)
ms:assetid: a0b6209c-9feb-08ae-002a-15d1d20734a8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249739(v=office.15)
ms:contentKeyID: 48546714
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231124
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 58d95f6a3238d09ae10ddb3ba127a9fa68631f4f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473439"
---
# <a name="commandtimeout-property-ado"></a>CommandTimeout-Eigenschaft (ADO)


**Betrifft**: Access 2013 | Office 2013

Gibt an, wie lange beim Ausführen eines Befehls gewartet wird, bis der Versuch beendet und ein Fehler generiert wird.

## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte

Mit dieser Eigenschaft wird ein Wert vom Datentyp Long festgelegt oder zurückgegeben, der angibt, wie lange in Sekunden gewartet werden soll, bis ein Befehl ausgeführt wird. Der Standard ist 30.

## <a name="remarks"></a>Hinweise

Verwenden Sie die **CommandTimeout** -Eigenschaft in einem [Connection](connection-object-ado.md) -Objekt oder ein [Command](command-object-ado.md) -Objekt, um den Abbruch des einen Aufruf der [Execute](https://msdn.microsoft.com/library/jj248785\(v=office.15\)) -Methode, aufgrund Verzögerungen aus Netzwerkverkehrs oder fett Server Nutzung zu erlauben. Wenn das Intervall, in der **CommandTimeout** -Eigenschaft verstreicht, bevor der Befehl abgeschlossen wurde, tritt ein Fehler auf, und ADO bricht den Befehl ab. Wenn Sie die Eigenschaft auf 0 (null) festlegen, wartet ADO unbegrenzt, bis die Ausführung abgeschlossen ist. Vergewissern Sie sich die Anbieter- und Datenquellen, die Sie Code Unterstützung die **CommandTimeout** -Funktionalität schreiben.

Die Einstellung von **CommandTimeout** in einem **Connection** -Objekt hat keine Auswirkung auf die Einstellung von **CommandTimeout** in einem **Command** -Objekt im gleichen **Connection** -Objekt. Das heißt, die **CommandTimeout** -Eigenschaft eines **Command** -Objekts erbt den Wert der **CommandTimeout** -Eigenschaft des **Connection** -Objekts nicht.

In einem **Connection** -Objekt behält die **CommandTimeout** -Eigenschaft nach dem Öffnen des **Connection** -Objekts Lese-/Schreibzugriff.
