---
title: CREATE USER or GROUP Statement (Microsoft Access SQL)
TOCTitle: CREATE USER or GROUP statement (Microsoft Access SQL)
ms:assetid: 62148ce2-0f81-944e-a1ab-edef990fff9f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194914(v=office.15)
ms:contentKeyID: 48545229
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5b294af16498778eae94b38a7a31b93fd029585e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295380"
---
# <a name="create-user-or-group-statement-microsoft-access-sql"></a>CREATE USER or GROUP Statement (Microsoft Access SQL)

**Gilt für**: Access 2013, Office 2013

Erstellt einen oder mehrere neue Benutzer bzw. eine oder mehrere neue Gruppen.

## <a name="syntax"></a>Syntax

### <a name="create-a-user"></a>Erstellen eines Benutzers

Create User ** *Password PID* \[, *User* *Password PID*,...\]

### <a name="create-a-group"></a>Erstellen einer Gruppe

Gruppen *Gruppen* *-PID*\[, *Gruppen* - *PID*,...\]

Die CREATE USER- oder GROUP-Anweisung besteht aus folgenden Komponenten:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Teil</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>user</em></p></td>
<td><p>Der Name eines Benutzers, der zur Informationsdatei der Arbeitsgruppe hinzugefügt werden soll.</p></td>
</tr>
<tr class="even">
<td><p><em>group</em></p></td>
<td><p>Der Name einer Gruppe, der zur Informationsdatei der Arbeitsgruppe hinzuzufügen ist.</p></td>
</tr>
<tr class="odd">
<td><p><em>password</em></p></td>
<td><p>Das Kennwort, das dem angegebenen <em>Benutzer</em> zuzuordnen ist.</p></td>
</tr>
<tr class="even">
<td><p><em>pid</em></p></td>
<td><p>Die persönliche ID.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Bemerkungen

Ein *Benutzer* und eine *Gruppe* können nicht über den gleichen Namen verfügen.

Ein *Kennwort* ist für jeden erstellten *Benutzer* bzw. für jede erstellte *Gruppe* erforderlich.

