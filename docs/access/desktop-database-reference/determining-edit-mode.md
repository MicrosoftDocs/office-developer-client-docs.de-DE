---
title: Bestimmen des Bearbeitungsmodus
TOCTitle: Determining Edit mode
ms:assetid: 45e21fa7-94e8-3449-e062-09cbcf15cba8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249215(v=office.15)
ms:contentKeyID: 48544563
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b5b62bc282a99472d0e7399ee9f3dd9d0648f0c7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293917"
---
# <a name="determining-edit-mode"></a>Bestimmen des Bearbeitungsmodus


**Gilt für**: Access 2013, Office 2013

ADO verwaltet einen Bearbeitungspuffer, der dem aktuellen Datensatz zugeordnet ist. Die **EditMode** -Eigenschaft gibt an, ob Änderungen an diesem Puffer vorgenommen wurden, oder ob ein neuer Datensatz erstellt wurde. Verwenden Sie **EditMode**, um den Bearbeitungsstatus des aktuellen Datensatzes zu bestimmen. Sie können testen, ob ausstehende Änderungen vorhanden sind, falls ein Bearbeitungsprozess unterbrochen wurde, und ermitteln, ob Sie die **Update** - oder **CancelUpdate** -Methode verwenden müssen.

**EditMode** gibt eine der **EditModeEnum**-Konstanten zurück, die in der folgenden Tabelle aufgeführt sind.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Konstante</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adEditNone</strong></p></td>
<td><p>Gibt an, dass kein Bearbeitungsvorgang ausgeführt wird.</p></td>
</tr>
<tr class="even">
<td><p><strong>adEditInProgress</strong></p></td>
<td><p>Gibt an, dass Daten im aktuellen Datensatz geändert, aber nicht gespeichert wurden.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adEditAdd</strong></p></td>
<td><p>Gibt an, dass die <strong>AddNew</strong>-Methode aufgerufen wurde, und dass der aktuelle Datensatz im Kopierpuffer ein neuer Datensatz ist, der nicht in der Datenbank gespeichert wurde.</p></td>
</tr>
<tr class="even">
<td><p><strong>adEditDelete</strong></p></td>
<td><p>Gibt an, dass der aktuelle Datensatz gelöscht wurde.</p></td>
</tr>
</tbody>
</table>


**EditMode** kann nur einen gültigen Wert zurückgeben, wenn ein aktueller Datensatz vorhanden ist. **EditMode** gibt einen Fehler zurück, falls **BOF** oder **EOF** gleich **True** ist, oder falls der aktuelle Datensatz gelöscht wurde.

