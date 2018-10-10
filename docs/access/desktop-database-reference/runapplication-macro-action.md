---
title: AusführenAnwendung-Makroaktion
TOCTitle: RunApplication Macro Action
ms:assetid: 29967e6e-c441-b115-3ee6-2299b8a3bc25
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192038(v=office.15)
ms:contentKeyID: 48543885
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm93359
f1_categories:
- Office.Version=v15
ms.openlocfilehash: ba7d40031a5a90c4f3e3d25459cc62023bc96832
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475680"
---
# <a name="runapplication-macro-action"></a>AusführenAnwendung-Makroaktion


**Betrifft**: Access 2013 | Office 2013

<table>
<thead>
<tr class="header">
<th><img src="media/access-alert-security.gif" title="Sicherheitshinweis" alt="Security note" /><strong>Sicherheitshinweis</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Seien Sie mit der Ausführung von ausführbaren Dateien oder ausführbarem Code in Makros oder Anwendungen vorsichtig. Ausführbare Dateien oder ausführbarer Code können verwendet werden, um Aktionen auszuführen, welche die Sicherheit Ihres Computers und Ihrer Daten gefährden können.</td>
</tr>
</tbody>
</table>


Sie können die **AusführenAnwendung** -Aktion verwenden, um eine Microsoft Windows-basierte oder MS-DOS-basierte Anwendung, wie Microsoft Excel, Microsoft Word oder Microsoft PowerPoint, in Microsoft Access auszuführen. Sie können z. B. Excel-Tabellenkalkulationsdaten in Ihre Access-Datenbank einfügen.


> [!NOTE]
> <P>[!HINWEIS] Diese Aktion wird nicht erlaubt, wenn die Datenbank nicht vertrauenswürdig ist. Informationen zur Aktivierung von Makros finden Sie unter den Links im Abschnitt See Also dieses Artikels.</P>



## <a name="setting"></a>Einstellung

Die **AusführenAnwendung** -Aktion hat das folgende Argument.

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
<td><p><strong>Befehlszeile</strong></p></td>
<td><p>Die Befehlszeile, die zum Starten der Anwendung verwendet wird (einschließlich des Pfads und aller anderen erforderlichen Parameter wie Switches, mit denen die Anwendung in einem bestimmten Modus ausgeführt wird). Geben Sie die Befehlszeile im Feld Befehlszeile im Abschnitt Aktionsargumente des Bereichs Makro-Generator ein. Dies ist ein erforderliches Argument.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Hinweise

Die mit dieser Aktion ausgewählte Anwendung wird im Vordergrund ausgeführt. Das Makro, das diese Aktion enthält, wird nach dem Starten der Anwendung weiter ausgeführt.

Sie können Daten zwischen der anderen Anwendung und Access übertragen, indem Sie die Microsoft Windows-Funktion Dynamischer Datenaustausch (Dynamic Data Exchange, DDE) oder die Zwischenablage verwenden. Um Tastaturbefehle an eine andere Anwendung zu senden (obwohl DDE eine effizientere Methode für das Übertragen von Daten ist), können Sie die **Tastaturbefehle** -Aktion verwenden. Sie können Daten auch zwischen Anwendungen freigeben, indem Sie die Automatisierung verwenden.

MS-DOS-basierte Anwendungen werden in einem MS-DOS-Fenster innerhalb der Windows-Umgebung ausgeführt.

In Windows-Betriebssystemen gibt es eine Reihe von Möglichkeiten, eine Anwendung auszuführen, u. a. Starten des Programms in Windows-Explorer, Verwenden des Befehls **Ausführen** im Menü **Start** und Doppelklicken auf ein Programmsymbol auf dem Windows- Desktop.

Sie können die **AusführenAnwendung** -Aktion nicht in einem Modul für Visual Basic für Applikationen (VBA) ausführen. Verwenden Sie stattdessen die **Shell** -Funktion von VBA.
