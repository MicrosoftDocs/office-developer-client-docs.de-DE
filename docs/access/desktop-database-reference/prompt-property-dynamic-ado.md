---
title: Refrom Dynamic Property (ADO)
TOCTitle: Prompt dynamic property (ADO)
ms:assetid: 6c899b03-1d1f-a81f-dc17-7205a0230af9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249428(v=office.15)
ms:contentKeyID: 48545473
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 261ac5640b5239f27ad91e01d1cb23794f88740a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301323"
---
# <a name="prompt-dynamic-property-ado"></a>Refrom Dynamic Property (ADO)

**Gilt für**: Access 2013, Office 2013

Es wird angegeben, ob der OLE DB-Anbieter den Benutzer zur Angabe von Initialisierungsinformationen auffordern sollte.

## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte

Mit dieser Eigenschaft wird ein [ConnectPromptEnum](connectpromptenum.md)-Wert festgelegt und zurückgegeben.

## <a name="remarks"></a>Bemerkungen

**Prompt** ist eine dynamische Eigenschaft, die vom OLE DB-Anbieter an die [Properties](connection-object-ado.md)-Auflistung des [Connection](properties-collection-ado.md)-Objekts angefügt werden kann. Für die Aufforderung zur Eingabe von Initialisierungsinformationen zeigen OLE DB-Anbieter dem Benutzer normalerweise ein Dialogfeld an.

Dynamische Eigenschaften eines [Connection](connection-object-ado.md)-Objekts gehen beim Schließen des **Connection** -Objekts verloren. Die **Prompt** -Eigenschaft muss vor dem erneuten Öffnen des **Connection** -Objekts zurückgesetzt werden, um einen anderen als den Standardwert zu verwenden.

> [!NOTE]
> [!HINWEIS] In Fällen, in denen der Benutzer nicht auf das Dialogfeld reagieren kann, sollten Sie nicht festlegen, dass der Anbieter den Benutzer zur Eingabe auffordern soll. Beispielsweise kann der Benutzer nicht reagieren, wenn die Anwendung nicht auf dem Client des Benutzers, sondern auf einem Serversystem ausgeführt wird, oder wenn die Anwendung auf einem System ohne angemeldeten Benutzer ausgeführt wird. In diesen Fällen wartet die Anwendung unbegrenzt auf eine Antwort und ist scheinbar abgestürzt.

**Verwendung**

```vb
    Set cn = New Connection
    cn.Provider = "SQLOLEDB"
    cn.Properties("Prompt") = adPromptNever    ' do not prompt the user
```
