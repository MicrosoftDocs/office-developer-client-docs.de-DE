---
title: REVOKE-Anweisung (Microsoft Access SQL)
TOCTitle: REVOKE Statement (Microsoft Access SQL)
ms:assetid: 69399fd6-c4e8-f2e2-e5f4-48ae779323f5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195272(v=office.15)
ms:contentKeyID: 48545409
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277479
f1_categories:
- Office.Version=v15
ms.openlocfilehash: bf8bbe65b8fe359e9e410d652deb41a1192efa92
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473295"
---
# <a name="revoke-statement-microsoft-access-sql"></a>REVOKE-Anweisung (Microsoft Access SQL)


**Betrifft**: Access 2013 | Office 2013

Widerruft bestimmte Berechtigungen eines vorhandenen Benutzers oder einer Gruppe.

## <a name="syntax"></a>Syntax

REVOKE {*Berechtigung*\[, *Berechtigung*,... \]} ON {Tabelle *Tabelle* | OBJECT- *Objekt*|

CONTAINTER *Container*} FROM {*autorisierungsname*\[, *autorisierungsname*,... \]}

Die REVOKE-Anweisung enthält folgende Bestandteile:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argument</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Berechtigung</em></p></td>
<td><p>Der geringsten Rechte oder Berechtigungen, die widerrufen werden. Berechtigungen werden mithilfe der folgenden Schlüsselwörter angegeben: auswählen, löschen, einfügen, aktualisieren und DROP, SELECTSECURITY, UPDATESECURITY, DBPASSWORD, UPDATEIDENTITY, CREATE, SELECTSCHEMA, SCHEMA und UPDATEOWNER.</p></td>
</tr>
<tr class="even">
<td><p><em>Tabelle</em></p></td>
<td><p>Ein gültiger Tabellenname.</p></td>
</tr>
<tr class="odd">
<td><p><em>Objekt</em></p></td>
<td><p>Dies kann jedes Objekt sein, das nicht aus einer Tabelle stammt. Ein Beispiel ist eine gespeicherte Abfrage (Sicht oder Prozedur).</p></td>
</tr>
<tr class="even">
<td><p><em>Container</em></p></td>
<td><p>Der Name eines gültigen Containers.</p></td>
</tr>
<tr class="odd">
<td><p><em>Autorisierungsname</em></p></td>
<td><p>Ein Benutzer- oder Gruppenname.</p></td>
</tr>
</tbody>
</table>
