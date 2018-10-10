---
title: KopierenDatenbankdatei-Makroaktion
TOCTitle: CopyDatabaseFile Macro Action
ms:assetid: e6320b55-946b-9efc-9b64-b86513801a37
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835963(v=office.15)
ms:contentKeyID: 48548373
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2b52644cb9a0a5140f45c42eaead84a63723c23e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475615"
---
# <a name="copydatabasefile-macro-action"></a>KopierenDatenbankdatei-Makroaktion


**Betrifft**: Access 2013 | Office 2013

Sie können die **KopierenDatenbankdatei** -Aktion verwenden, um eine Kopie der aktuellen Microsoft SQL Server 7.0-Datenbank oder einer neueren Datenbank anzulegen, die mit Ihrem Access-Projekt verbunden ist. Access trennt die aktuelle Datenbank und fügt sie dann auf den Zielserver. Weitere Informationen zum Trennen und Verbinden einer Datenbank finden Sie in der SQL Server-Dokumentation.


> [!NOTE]
> <P>[!HINWEIS] Diese Aktion wird nicht erlaubt, wenn die Datenbank nicht vertrauenswürdig ist. Informationen zur Aktivierung von Makros finden Sie unter den Links im Abschnitt See Also dieses Artikels.</P>



## <a name="setting"></a>Einstellung

Die **KopierenDatenbankdatei** -Aktion hat die folgenden Argumente.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Aktionsargument</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Datenbankname</strong></p></td>
<td><p>Der Name der neuen Masterdatendatei. Der Standardpfad der Datei ist der aktuelle Speicherort der Access-Projektdatei (ADP).</p></td>
</tr>
<tr class="even">
<td><p><strong>Datei überschreiben</strong></p></td>
<td><p>Gibt an, ob eine vorhandene Datei mit demselben Namen ersetzt werden soll. Wenn <strong>Ja</strong> festgelegt und der Dateiname bereits vorhanden ist, wird die Datei überschrieben. Wenn <strong>Nein</strong> festgelegt und der Dateiname bereits vorhanden ist, wird die Datei nicht überschrieben, und die Aktion schlägt fehl. Wenn die Datei noch nicht vorhanden ist, wird diese Einstellung ignoriert. Die Standardeinstellung ist <strong>Ja</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Alle Verbindungen trennen</strong></p></td>
<td><p>Gibt an, ob Access das Trennen von Datenbankverbindungen erzwingen sollte. Wenn <strong>Ja</strong> festgelegt ist, werden alle Verbindungen mit der aktuellen Datenbank getrennt, damit das Kopieren der Datenbank fortgesetzt werden kann. Wenn <strong>Nein</strong> festgelegt ist und mindestens eine Verbindung zur Datenbank besteht, schlägt das Kopieren der Datenbank fehl. Die Standardeinstellung ist <strong>Nein</strong>. 

</p>

> [!WARNING]
> <P>Wenn Verbindungen zu einer Datenbank ohne angemessene Warnung getrennt werden, kann es zu Datenverlusten kommen.</P>


<p></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Hinweise

Der Kopiervorgang läuft synchron ab. Daher können Sie andere Vorgänge erst ausführen, wenn das Kopieren der Datenbank abgeschlossen ist.

Die **KopierenDatenbankdatei** -Aktion kopiert nicht nur Daten, Datendefinitionen und Datenbankobjekte, sondern auch erweiterte Eigenschaften wie Standardwerte, Texteinschränkungen und Nachschlagewerte.

Voraussetzungen für das Kopieren einer Datenbank:

  - Sie müssen vor dem Kopieren der Datenbankdatei alle Anwendungen und Benutzer trennen.

  - Alle Objekte und Sichten mit Ausnahme des Navigationsbereichs müssen geschlossen sein.

  - Die aktuelle Datenbank darf nicht repliziert sein.

  - Bei der Quellserverdatenbank muss es sich um Microsoft SQL Server, Version 7.0 oder höher, oder SQL Server 2000 Desktop Engine handeln, die auf einem lokalen Computer ausgeführt wird.

<!-- end list -->

  - Bei der SQL Server-Datenbank auf dem Quellserver muss es sich um eine einzelne Dateidatenbank handeln.

  - 
				Sie müssen auf dem Quell- und dem Zielcomputer mit SQL Server ein Mitglied der Rolle sysadmin sein.


Verwenden Sie die **CopyDatabaseFile** -Methode des **DoCmd**-Objekts, um die **KopierenDatenbankdatei**-Aktion in einem VBA-Modul (Visual Basic für Applikationen) auszuführen.
