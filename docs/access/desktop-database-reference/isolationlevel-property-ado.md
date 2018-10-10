---
title: IsolationLevel-Eigenschaft (ADO)
TOCTitle: IsolationLevel Property (ADO)
ms:assetid: 19461be5-c94b-4b61-ce08-7abdf702c3dc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248939(v=office.15)
ms:contentKeyID: 48543493
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7424258f4b5a69764189f33a902956f370a56094
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474452"
---
# <a name="isolationlevel-property-ado"></a>IsolationLevel-Eigenschaft (ADO)


**Betrifft**: Access 2013 | Office 2013

Gibt die Isolationsstufe für ein [Connection](connection-object-ado.md)-Objekt an.

## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte

Legt einen [IsolationLevelEnum](isolationlevelenum.md)-Wert fest oder gibt den Wert zurück. Der Standardwert ist **AdXactChaos**.

## <a name="remarks"></a>Hinweise

Legen Sie mit der **IsolationLevel** -Eigenschaft die Isolationsstufe eines **Connection** -Objekts fest. Die Einstellung wird erst beim nächsten Aufrufen der [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md)-Methode wirksam. Wenn die von Ihnen angeforderte Isolationsstufe nicht verfügbar ist, gibt der Anbieter möglicherweise die nächsthöhere Isolationsstufe zurück.

Die **IsolationLevel** -Eigenschaft ist nicht schreibgeschützt.

**Remote Data Service-Verwendung** Wenn für ein clientseitiges Connection-Objekt verwendet wird, kann die **IsolationLevel** -Eigenschaft nur auf **AdXactUnspecified**festgelegt werden.

Da Benutzer mit nicht verbundenen **Recordset** -Objekten in einem clientbasierten Cache arbeiten, können Probleme mit mehreren Benutzern auftreten. Wenn beispielsweise zwei unterschiedliche Benutzer versuchen, denselben Datensatz zu aktualisieren, hat der Benutzer Erfolg, der den Datensatz zuerst aktualisiert. Die Aktualisierungsanforderung des zweiten Benutzers verursacht einen Fehler.
