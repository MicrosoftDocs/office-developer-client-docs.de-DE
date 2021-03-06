---
title: StreamReadEnum (Access Desktop Database Reference)
TOCTitle: StreamReadEnum
ms:assetid: 12432c0d-dc2e-10ea-13db-0c07b6ba29bc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248895(v=office.15)
ms:contentKeyID: 48543336
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e4d9c96a7bb34fe0ab3512a316a92e1f7a01ef4b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314721"
---
# <a name="streamreadenum"></a>StreamReadEnum

**Gilt für**: Access 2013, Office 2013

Gibt an, ob der gesamte Datenstrom oder die nächste Zeile aus einem [Stream](stream-object-ado.md)-Objekt gelesen werden sollte.

<br/>

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
<td><p><strong>adReadAll</strong></p></td>
<td><p>-1</p></td>
<td><p>Standardwert. Liest alle Bytes aus dem Datenstrom, von der aktuellen Position bis zur <a href="eos-property-ado.md">EOS</a>-Markierung. Dies ist der einzige gültige <strong>StreamReadEnum</strong>-Wert mit binären Datenströmen (<a href="type-property-ado-stream.md">Typ</a> ist <strong>adTypeBinary</strong>).</p></td>
</tr>
<tr class="even">
<td><p><strong>Angleichen</strong></p></td>
<td><p>-2</p></td>
<td><p>Liest die nächste Zeile aus dem Datenstrom (angegeben durch die <a href="lineseparator-property-ado.md">LineSeparator</a>-Eigenschaft).</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>ADO/WFC-Äquivalent

Diese Konstanten haben keine ADO/WFC-Entsprechungen.

