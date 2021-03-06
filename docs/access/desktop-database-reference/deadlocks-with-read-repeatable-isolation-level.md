---
title: Deadlocks mit Read REPEATABLE Isolation Level
TOCTitle: Deadlocks with read repeatable isolation level
ms:assetid: 3d5f3293-33bb-cf6d-362a-278f9ec1bd3c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249165(v=office.15)
ms:contentKeyID: 48544342
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5c3e38f6054e6548dfc14d30ce6ec89dcb2e4b01
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294176"
---
# <a name="deadlocks-with-read-repeatable-isolation-level"></a>Deadlocks mit Read REPEATABLE Isolation Level


**Gilt für**: Access 2013, Office 2013

If a custom business object uses an isolation level of read repeatable to access a SQL Server, and the business object is called simultaneously by two clients that send a query and update in the same transaction, a deadlock is possible. Remote Data Service is designed to allow one of the processes to time out to release the deadlock, but the update will fail for that client.

Verwenden Sie die Dynamic-Eigenschaft des [Cursor Dienst](microsoft-cursor-service-for-ole-db-ado-service-component.md)-**Befehls** Timeout, um die Länge des Timeouts zu ändern.

