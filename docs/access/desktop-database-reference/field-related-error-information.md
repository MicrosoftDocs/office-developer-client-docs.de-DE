---
title: Feldbezogene Fehlerinformationen
TOCTitle: Field-related error information
ms:assetid: 81a2c5a4-ab09-53d8-b270-e889b00a0c1a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249559(v=office.15)
ms:contentKeyID: 48545958
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3a0d0362b8f0ff9570a92a3c1c364061d1f9a584
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292972"
---
# <a name="field-related-error-information"></a>Feldbezogene Fehlerinformationen


**Gilt für**: Access 2013, Office 2013

Wenn sich ein Fehler direkt auf ein Feld bezieht – z. B., wenn die Daten fehlen oder wenn sie für das Feld den falschen Datentyp aufweisen – können Sie weitere Informationen zur Ursache des Problems abrufen, indem Sie die **Status**-Eigenschaft des **Field**-Objekts überprüfen. Diese Eigenschaft wurde optimiert und stellt nun spezifische Informationen zum Problem bereit. Wenn z. B. bei einem Aufruf von **UpdateBatch** ein Fehler erzeugt wird, kann die Ursache des Problems bestimmt werden, indem Sie die **Status**-Eigenschaft des **Fields**-Objekts in allen betroffenen Datensätzen überprüfen. Die Eigenschaft enthält einen der Werte in der **FieldStatusEnum**-Konstante. Die folgende Tabelle enthält die Werte, die beim Auftreten eines Fehlers von besonderem Interesse sind.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Konstante</p></th>
<th><p>Wert</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adFieldCantConvertValue</strong></p></td>
<td><p>2</p></td>
<td><p>Gibt an, dass das Feld nicht ohne Datenverlust abgerufen oder gespeichert werden kann.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldDataOverflow</strong></p></td>
<td><p>6</p></td>
<td><p>Gibt an, dass die vom Anbieter zurückgegebenen Daten einen Datentypüberlauf des Felds verursacht haben.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldDefault</strong></p></td>
<td><p>13</p></td>
<td><p>Gibt an, dass beim Festlegen von Daten der Standardwert verwendet wurde.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldIgnore</strong></p></td>
<td><p>15</p></td>
<td><p>Gibt an, dass beim Festlegen von Datenwerten in der Quelle dieses Feld ausgelassen wurde. Vom Anbieter wurde kein Wert festgelegt.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldIntegrityViolation</strong></p></td>
<td><p>10</p></td>
<td><p>Gibt an, dass das Feld nicht geändert werden kann, da es eine berechnete oder abgeleitete Entität ist.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldIsNull</strong></p></td>
<td><p>3</p></td>
<td><p>Gibt an, dass der Anbieter einen NULL-Wert zurückgab.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldOutOfSpace</strong></p></td>
<td><p>22</p></td>
<td><p>Gibt an, dass der Anbieter nicht genügend Speicherplatz abrufen kann, um einen Verschiebe- oder Kopiervorgang abzuschließen.</p></td>
</tr>
</tbody>
</table>

