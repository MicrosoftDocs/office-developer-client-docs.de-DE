---
title: BeginTrans-, CommitTrans-und RollbackTrans-Methoden (ADO)
TOCTitle: BeginTrans, CommitTrans, and RollbackTrans methods (ADO)
ms:assetid: 9a0415f0-9424-8d1c-4779-92e932292d46
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249694(v=office.15)
ms:contentKeyID: 48546529
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8d9dc28bd64966e85d16ee2d8cb62fdebc3ba942
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296871"
---
# <a name="begintrans-committrans-and-rollbacktrans-methods-ado"></a>BeginTrans-, CommitTrans-und RollbackTrans-Methoden (ADO)

**Gilt für**: Access 2013, Office 2013

Durch diese Transaktionsmethoden wird die Transaktionsverarbeitung in einem [Connection](connection-object-ado.md)-Objekt wie folgt verwaltet:

- **BeginTrans** - Eine neue Transaktion wird begonnen.

- **CommitTrans** - Alle Änderungen werden gespeichert, und die aktuelle Transaktion wird beendet. Möglicherweise wird auch eine neue Transaktion gestartet.

- **RollbackTrans** - Alle während der aktuellen Transaktion vorgenommenen Änderungen werden abgebrochen, und die Transaktion wird beendet. Möglicherweise wird auch eine neue Transaktion gestartet.

## <a name="syntax"></a>Syntax

*Level* = -*Objekt*. BeginTrans ()

- *Objekt*. BeginTrans

- *Objekt*. CommitTrans

- *Objekt*. RollbackTrans

## <a name="return-value"></a>Rückgabewert

**BeginTrans** kann als Funktion aufgerufen werden, von der eine **Long**-Variable zurückgegeben wird, durch die die Schachtelungsebene der Transaktion angegeben wird.

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*Objekt* |Ein **Connection** -Objekt.|

### <a name="connection"></a>Verbindung

Verwenden Sie diese Methoden mit einem **Connection**-Objekt, wenn Sie eine Reihe von an den Quelldaten vorgenommenen Änderungen als einzelne Einheit speichern oder abbrechen möchten. Beispielsweise subtrahieren Sie zum Übertragen von Geldbeträgen zwischen Konten einen Betrag von einem Konto und addieren den gleichen Betrag zu einem anderen Konto. Wenn eine der Aktualisierungen fehlschlägt, sind die Konten nicht mehr ausgeglichen. Durch das Vornehmen dieser Änderungen mit einer geöffneten Transaktion wird sichergestellt, dass alle oder keine der Änderungen durchlaufen.

> [!NOTE]
> Transaktionen werden nicht von allen Anbietern unterstützt. Stellen Sie sicher, dass die Anbieter definierte Eigenschaft **Transaction DDL** in der [Properties](properties-collection-ado.md) -Auflistung des **Connection** -Objekts angezeigt wird, was darauf hinweist, dass der Anbieter Transaktionen unterstützt. Wenn Transaktionen vom Anbieter nicht unterstützt werden, wird beim Aufrufen einer dieser Methoden ein Fehler zurückgegeben.

Nach dem Aufrufen der **BeginTrans**-Methode wird vom Anbieter erst wieder sofort ein Commit für vorgenommene Änderungen ausgeführt, wenn Sie **CommitTrans** oder **RollbackTrans** aufrufen, um die Transaktion zu beenden.

Für Anbieter, von denen geschachtelte Transaktionen unterstützt werden, wird durch das Aufrufen der **BeginTrans**-Methode in einer geöffneten Transaktion eine neue geschachtelte Transaktion gestartet. Durch den Rückgabewert wird die Ebene der Schachtelung angegeben: Durch den Rückgabewert "1" wird angegeben, dass Sie eine Transaktion der obersten Ebene geöffnet haben (d. h., die Transaktion ist nicht in einer anderen Transaktion geschachtelt), durch "2" wird angegeben, dass Sie eine Transaktion der zweiten Ebene geöffnet haben (eine Transaktion, die in einer Transaktion der obersten Ebene geschachtelt ist) usw. Das Aufrufen von **CommitTrans** oder **RollbackTrans** wirkt sich nur auf die zuletzt geöffnete Transaktion aus. Sie müssen die aktuelle Transaktion schließen oder ein Rollback ausführen, bevor Sie Transaktionen einer höheren Ebene auflösen können.

Durch das Aufrufen der **CommitTrans** -Methode werden in einer geöffneten Transaktion vorgenommene Änderungen für die Verbindung gespeichert, und die Transaktion wird beendet. Durch das Aufrufen der **RollbackTrans** -Methode werden alle in einer geöffneten Transaktion vorgenommenen Änderungen rückgängig gemacht, und die Transaktion wird beendet. Durch das Aufrufen einer der Methoden ohne geöffnete Transaktion wird ein Fehler generiert.

Abhängig von der **Attributes**-Eigenschaft des [Connection](attributes-property-ado.md) -Objekts wird durch das Aufrufen der Methoden **CommitTrans** oder **RollbackTrans** möglicherweise automatisch eine neue Transaktion gestartet. Wenn die **Attributes** -Eigenschaft auf **adXactCommitRetaining** festgelegt ist, wird nach einem **CommitTrans** -Aufruf automatisch vom Anbieter eine neue Transaktion gestartet. Wenn die **Attributes** -Eigenschaft auf **adXactAbortRetaining** festgelegt ist, wird nach einem **RollbackTrans** -Aufruf automatisch vom Anbieter eine neue Transaktion gestartet.

### <a name="remote-data-service"></a>Remote Data Service

Die Methoden **BeginTrans**, **CommitTrans** und **RollbackTrans** stehen für ein clientseitiges **Connection**-Objekt nicht zur Verfügung.

