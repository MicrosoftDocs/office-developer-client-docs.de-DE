---
title: Requery-Methode (ADO)
TOCTitle: Requery Method (ADO)
ms:assetid: 1062d907-979f-020a-b2ed-94e11c0e7d08
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248871(v=office.15)
ms:contentKeyID: 48543292
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b3fde13d923a67ca995cdb3e7f59a327e82a9688
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474683"
---
# <a name="requery-method-ado"></a>Requery-Methode (ADO)


**Betrifft**: Access 2013 | Office 2013



Die Daten in einem [Recordset](recordset-object-ado.md)-Objekt werden aktualisiert durch erneutes Ausführen der Abfrage, auf der das Objekt basiert.

## <a name="syntax"></a>Syntax

*Recordset-Objekt*. AktualisierenDaten- *Optionen*

## <a name="parameter"></a>Parameter

  - *Options*

  - Optional. Eine Bitmaske, die die Werte [ExecuteOptionEnum](executeoptionenum.md) und [CommandTypeEnum](commandtypeenum.md) enthält, die sich auf diese Operation auswirken.


> [!NOTE]
> <P>Wenn <EM>Optionen</EM> auf <STRONG>AdAsyncExecute</STRONG>festgelegt ist, wird diese Operation asynchron ausgeführt wird, und ein <A href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">RecordsetChangeComplete</A> -Ereignis wird ausgegeben, wenn er abgeschlossen ist.</P>



Die **ExecuteOpenEnum** -Werte von **adExecuteNoRecords** oder **adExecuteStream** sollten nicht mit **Requery** verwendet werden.

## <a name="remarks"></a>Hinweise

Verwenden Sie die **Requery** -Methode zum Aktualisieren des gesamten Inhalts eines **Recordset** -Objekts über die Datenquelle, indem Sie den ursprünglichen Befehl erneut ausgeben und die Daten ein zweites Mal abrufen. Das Aufrufen dieser Methode entspricht dem aufeinander folgenden Aufrufen der Methoden [Close](close-method-ado.md) und [Open](open-method-ado-recordset.md). Wenn Sie den aktuellen Datensatz bearbeiten oder einen neuen Datensatz hinzufügen, tritt ein Fehler auf.

Während das **Recordset**-Objekt geöffnet ist, sind die Eigenschaften, durch die der Cursor ([CursorType](cursortype-property-ado.md), [LockType](locktype-property-ado.md), [MaxRecords](maxrecords-property-ado.md) usw.) definiert wird, schreibgeschützt. Daher kann durch die **Requery**-Methode nur der aktuelle Cursor aktualisiert werden. Zum Ändern der Cursoreigenschaften und zum Anzeigen der Ergebnisse müssen Sie die [Close](close-method-ado.md)-Methode verwenden, damit wieder der Lese- und Schreibzugriff auf die Eigenschaften möglich ist. Dann können Sie die Eigenschaftseinstellungen ändern und die [Open](open-method-ado-recordset.md)-Methode aufrufen, um den Cursor erneut zu öffnen.
