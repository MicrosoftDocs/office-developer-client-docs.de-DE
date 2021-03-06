---
title: Aktualisieren von Daten (Access-Desktop-Daten Bankreferenz)
TOCTitle: Updating Data
ms:assetid: 02e82066-77c8-cbb2-db28-98e2fc94404c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248794(v=office.15)
ms:contentKeyID: 48542970
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8e6989468e23fc1c9c611eb091172822a6ffe938
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32313566"
---
# <a name="updating-data"></a>Aktualisieren von Daten


**Gilt für**: Access 2013, Office 2013

Aktualisierungsverhalten und Funktionalität sind größtenteils vom Aktualisierungsmodus (Sperrtyp), Cursortyp und Cursorplatzierung abhängig.

Verwenden Sie die **Update** -Methode, um Änderungen am aktuellen Datensatz eines **Recordset** -Objekts seit dem Aufrufen der **AddNew** -Methode oder seit dem Ändern von Feldwerten in einem vorhandenen Datensatz zu speichern. Das **Recordset** -Objekt muss Aktualisierungen unterstützen.

Wenn das **Recordset** -Objekt die Batchaktualisierung unterstützt, können Sie mehrere Änderungen an mindestens einem Datensatz bis zum Aufrufen der **UpdateBatch** -Methode lokal speichern. Falls Sie den aktuellen Datensatz bearbeiten oder einen neuen Datensatz hinzufügen, wenn Sie die **UpdateBatch** -Methode aufrufen, ruft ADO automatisch die **Update** -Methode auf, um ausstehende Änderungen am aktuellen Datensatz zu speichern, bevor die Batchänderungen an den Anbieter übertragen werden.

Der aktuelle Datensatz bleibt aktuell, nachdem Sie die Methode **Update** oder **UpdateBatch** aufgerufen haben.

Dieser Abschnitt enthält die folgenden Themen:

- [Unmittelbarer Modus](immediate-mode.md)
- [Verarbeitung von Transaktionen](transaction-processing.md)
- [Batch Modus (ADO)](batch-mode.md)

