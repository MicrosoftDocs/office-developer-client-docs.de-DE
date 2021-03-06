---
title: Source-Eigenschaft (ADO Record)
TOCTitle: Source property (ADO Record)
ms:assetid: f36f0f5f-4493-d8c5-db4b-c72f5031bcb3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250235(v=office.15)
ms:contentKeyID: 48548670
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9bd1e1259eb7b089d0387dd385ee5157eeac2f34
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314553"
---
# <a name="source-property-ado-record"></a>Source-Eigenschaft (ADO Record)


**Gilt für**: Access 2013, Office 2013

Gibt die vom [Record](record-object-ado.md)-Objekt dargestellte Datenquelle oder das Objekt an.

## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte

Legt einen **Variant**-Wert fest, der die vom **Record**-Objekt dargestellte Entität angibt, oder gibt den Wert zurück.

## <a name="remarks"></a>Bemerkungen

Die **Source**-Eigenschaft gibt das *Source*-Argument der [Open](open-method-ado-record.md)-Methode des **Record**-Objekts zurück. Sie kann die Zeichenfolge einer absoluten oder relativen URL enthalten. Eine absolute URL kann verwendet werden, ohne dass die [ActiveConnection](activeconnection-property-ado.md)-Eigenschaft festgelegt werden muss, um das **Record** -Objekt direkt zu öffnen. In diesem Fall wird ein implizites **Connection**-Objekt erstellt.

Die **Source**-Eigenschaft kann auch einen Verweis auf ein bereits geöffnetes **Recordset**-Objekt enthalten. Dadurch wird ein **Record**-Objekt geöffnet, das die aktuelle Zeile im **Recordset**-Objekt darstellt.

Außerdem kann die **Source**-Eigenschaft einen Verweis auf ein [Command](command-object-ado.md)-Objekt enthalten, das eine einzelne Datenzeile vom Anbieter zurückgibt.

Wenn die **ActiveConnection** -Eigenschaft ebenfalls festgelegt ist, muss die **Source** -Eigenschaft auf ein Objekt verweisen, das im Bereich dieser Verbindung vorhanden ist. Wenn z. B. in einem strukturierten Namespace die **Source** -Eigenschaft eine absolute URL enthält, muss sie auf einen Knoten zeigen, der innerhalb des Knotenbereichs vorhanden ist, der durch die URL in der Verbindungszeichenfolge identifiziert wird. Enthält die **Source** -Eigenschaft eine relative URL, dann wird sie innerhalb des Kontexts überprüft, der von der **ActiveConnection** -Eigenschaft festgelegt wird.

Die **Source** -Eigenschaft ist nicht schreibgeschützt, wenn das **Record** -Objekt geschlossen ist, und schreibgeschützt, wenn das **Record** -Objekt geöffnet ist.

> [!NOTE]
> [!HINWEIS] Bei URLs, die das HTTP-Schema verwenden, wird automatisch der [Microsoft OLE DB-Anbieter für Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md) aufgerufen. Weitere Informationen finden Sie unter [absolute und relative URLs](absolute-and-relative-urls.md).


