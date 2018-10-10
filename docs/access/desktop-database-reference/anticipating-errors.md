---
title: Vorhersehen von Fehlern
TOCTitle: Anticipating Errors
ms:assetid: f2368a03-d446-ab42-b505-d5f5a214c000
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250229(v=office.15)
ms:contentKeyID: 48548645
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f062eb86b45778cc7f25fb2d0d0588b82bdd78b3
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475259"
---
# <a name="anticipating-errors"></a>Vorhersehen von Fehlern


**Betrifft**: Access 2013 | Office 2013

Die Fehlervermeidung ist mindestens so wichtig wie die Fehlerbehandlung. Dieser letzte Abschnitt enthält eine kurze Aufstellung der Vorsichtsmaßnahmen für Ihre Anwendung, um die Wahrscheinlichkeit von Fehlern zu reduzieren.

Überprüfen Sie den Status von Objekten, indem Sie den Wert der **State** -Eigenschaft überprüfen, bevor Sie einen Vorgang mithilfe dieser Objekte ausführen. Wenn die Anwendung z. B. ein globales **Connection** -Objekt verwendet, überprüfen Sie dessen **State** -Eigenschaft, um festzustellen, ob es bereits geöffnet ist, bevor Sie die **Open** -Methode aufrufen.

  - Jedes Programm, das Daten von einem Benutzer annimmt, muss Code zum Überprüfen dieser Daten enthalten, bevor sie an den Datenspeicher gesendet werden. Sie können sich nicht darauf verlassen, dass Sie vom Datenspeicher, vom Anbieter, von ADO oder sogar von der Programmiersprache über Probleme informiert werden. Sie müssen jedes von den Benutzern eingegebene Byte überprüfen und sicherstellen, dass die Daten den richtigen Typ für das Feld aufweisen und dass erforderliche Felder nicht leer sind.

Überprüfen Sie die Daten, bevor Sie versuchen, Daten in den Datenspeicher zu schreiben. Dazu verwenden Sie am einfachsten das Ereignis **WillMove** oder **WillUpdateRecordset**. Ausführlichere Informationen zum Behandeln von ADO-Ereignissen finden Sie in [Kapitel 7: Behandeln von ADO-Ereignissen](chapter-7-handling-ado-events.md).

Stellen Sie sicher, dass Recordset-Objekte nicht außerhalb der Begrenzungen des Recordset-Objekts liegen, bevor Sie versuchen den Datensatzzeiger zu verschieben. Ein Fehler tritt auf, falls Sie versuchen MoveNext auszuführen, wenn EOF gleich True ist, oder MovePrev, wenn BOF gleich True ist. Falls Sie eine der Move-Methoden ausführen, wenn sowohl EOF als auch BOF gleich True sind, wird ein Fehler generiert.

Fehler treten ebenfalls auf, wenn Sie z. B. versuchen, **Seek** oder **Find** für ein leeres **Recordset** -Objekt auszuführen.
