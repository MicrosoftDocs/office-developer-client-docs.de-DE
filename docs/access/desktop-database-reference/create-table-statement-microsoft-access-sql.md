---
title: CREATE TABLE-Anweisung (Microsoft Access SQL)
TOCTitle: CREATE TABLE Statement (Microsoft Access SQL)
ms:assetid: fc45d36e-6e43-c030-5016-cca8bb1379fe
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837200(v=office.15)
ms:contentKeyID: 48548888
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277563
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 749d593a0c9ed32290ee91aec20c79a141a83f56
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474294"
---
# <a name="create-table-statement-microsoft-access-sql"></a>CREATE TABLE-Anweisung (Microsoft Access SQL)

**Betrifft**: Access 2013 | Office 2013

Erstellt eine neue Tabelle.

> [!NOTE]
> [!HINWEIS] Das Microsoft Access-Datenbankmodul unterstützt nicht die Verwendung der CREATE TABLE- oder anderer DDL-Anweisungen für Datenbanken ohne das Microsoft Access-Datenbankmodul. Verwenden Sie stattdessen die CREATE-Methoden von DAO.

## <a name="syntax"></a>Syntax

Erstellen von \[temporäre\] Tabelle *Tabelle* (*Feld1 Typ* \[(*Größe*)\] \[nicht "NULL"\] \[WITH COMPRESSION | WITH COMP\] \[ *index1* \] \[, *Feld2* *Typ* \[(*Größe*)\] \[nicht "NULL"\] \[ *index2* \] \[,... \] \] \[, CONSTRAINT *mehrerefelderindex* \[,... \]\])

Die CREATE TABLE-Anweisung besteht aus folgenden Komponenten:

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
<td><p><em>Tabelle</em></p></td>
<td><p>Der Name der zu erstellenden Tabelle.</p></td>
</tr>
<tr class="even">
<td><p><em>Feld1</em>, <em>Feld2</em></p></td>
<td><p>Die Namen der in der neuen Tabelle zu erstellenden Felder. Sie müssen mindestens ein Feld erstellen.</p></td>
</tr>
<tr class="odd">
<td><p><em>type</em></p></td>
<td><p>Der Datentyp des <em>Felds</em> in der neuen Tabelle.</p></td>
</tr>
<tr class="even">
<td><p><em>size</em></p></td>
<td><p>Die Feldgröße in Zeichen (nur Text- und binäre Felder).</p></td>
</tr>
<tr class="odd">
<td><p><em>Index1</em>, <em>Index2</em></p></td>
<td><p>Eine CONSTRAINT-Klausel, die einen Index mit einem Feld definiert. Weitere Informationen zum Erstellen dieses Indexes finden Sie unter <a href="constraint-clause-microsoft-access-sql.md">CONSTRAINT-Klausel</a>.  </p></td>
</tr>
<tr class="even">
<td><p><em>Index_mit_mehreren_Feldern</em></p></td>
<td><p>Eine CONSTRAINT-Klausel, die einen Index mit mehreren Feldern definiert. Weitere Informationen zum Erstellen dieses Indexes finden Sie unter <a href="constraint-clause-microsoft-access-sql.md">CONSTRAINT-Klausel</a>.  </p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Hinweise

Verwenden Sie die CREATE TABLE-Anweisung, um eine neue Tabelle und deren Felder und Feldeinschränkungen zu definieren. Wenn für ein Feld NOT NULL angegeben ist, müssen neue Datensätze gültige Daten in diesem Feld aufweisen.

Eine CONSTRAINT-Klausel erstellt verschiedene Einschränkungen für ein Feld und kann zum Erstellen des Primärschlüssels verwendet werden. Sie können auch die [CREATE INDEX](create-index-statement-microsoft-access-sql.md)-Anweisung zum Erstellen eines Primärschlüssels oder zusätzlicher Indizes für vorhandene Tabellen verwenden.

NOT NULL kann für ein einzelnes Feld oder in einer benannten CONSTRAINT-Klausel verwendet werden, die entweder für ein einzelnes Feld oder mehrere Felder namens CONSTRAINT gilt. Jedoch können Sie die NOT NULL-Einschränkung nur einmal auf ein Feld anwenden. Der Versuch, diese Einschränkung mehrmals anzuwenden, führt zu einem Laufzeitfehler.

Beim Erstellen der Tabelle vom Typ TEMPORARY ist diese nur in der Sitzung sichtbar, in der sie erstellt wurde. Sie wird automatisch gelöscht, wenn die Sitzung beendet wird. Auf temporäre Tabellen können mehrere Benutzer zugreifen.

Das WITH COMPRESSION-Attribut kann nur zusammen mit den Datentypen CHARACTER und MEMO (auch TEXT genannt) und den entsprechenden Synonymen verwendet werden.

Das WITH COMPRESSION-Attribut wurde für Zeichenspalten vom Typ CHARACTER aufgrund der Änderung am Unicode-Zeichendarstellungsformat hinzugefügt. Unicode-Zeichen benötigen jeweils zwei Bytes für jedes Zeichen. Für vorhandene Microsoft ® Jet-Datenbanken, die überwiegend Zeichendaten enthalten, kann dies bedeuten, dass die Datenbankdatei bei Konvertierung in das Microsoft Access-Datenbankformat ihre Größe nahezu verdoppelt. Jedoch kann die Unicode-Darstellung vieler Zeichensätze, die früher als Single-Byte Character Sets (SBCS) bezeichnet wurden, auf einfache Weise zu einem einzelnen Byte komprimiert werden. Wenn Sie eine CHARACTER-Spalte mit diesem Attribut definieren, werden die Daten automatisch komprimiert gespeichert und dekomprimiert, wenn der Abruf aus der Spalte erfolgt.

MEMO-Spalten können auch zum Speichern von Daten in einem komprimierten Format definiert werden, wobei jedoch eine Einschränkung gilt. Nur Instanzen von MEMO-Spalten, die in komprimierten Zustand maximal 4096 Byte groß sind, werden komprimiert. Alle anderen Instanzen von MEMO-Spalten bleiben unkomprimiert. Dies bedeutet, dass in einer Tabelle bei einer bestimmten MEMO-Spalte einige Daten möglicherweise komprimiert werden und andere nicht.

## <a name="example"></a>Beispiel

In diesem Beispiel wird eine neue Tabelle namens "ThisTable" mit zwei Textfeldern erstellt.

```vb
    Sub CreateTableX1() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Create a table with two text fields. 
        dbs.Execute "CREATE TABLE ThisTable " _ 
            & "(FirstName CHAR, LastName CHAR);" 
     
        dbs.Close 
     
    End Sub 
```

<br/>

Bei diesem Beispiel wird eine neue Tabelle mit dem Namen "myTable" und zwei Textfeldern erstellt: einem Datums-/Uhrzeitfeld und einen eindeutigen Index, der aus allen drei Feldern besteht.

```vb
    Sub CreateTableX2() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
     
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Create a table with three fields and a unique 
        ' index made up of all three fields. 
        dbs.Execute "CREATE TABLE MyTable " _ 
            & "(FirstName CHAR, LastName CHAR, " _ 
            & "DateOfBirth DATETIME, " _ 
            & "CONSTRAINT MyTableConstraint UNIQUE " _ 
            & "(FirstName, LastName, DateOfBirth));" 
     
        dbs.Close 
     
    End Sub
```

<br/>

Im folgenden Beispiel wird eine neue Tabelle mit zwei Textfeldern und einem Feld vom Typ **Integer** erstellt. Das Feld "SSN" ist der Primärschlüssel.

```vb
    Sub CreateTableX3() 
     
         Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Create a table with three fields and a primary 
        ' key. 
        dbs.Execute "CREATE TABLE NewTable " _ 
            & "(FirstName CHAR, LastName CHAR, " _ 
            & "SSN INTEGER CONSTRAINT MyFieldConstraint " _ 
            & "PRIMARY KEY);" 
     
        dbs.Close 
     
    End Sub
```