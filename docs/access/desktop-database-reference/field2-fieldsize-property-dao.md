---
title: Field2.FieldSize Property (DAO)
TOCTitle: FieldSize Property
ms:assetid: d609801d-7761-663f-2840-de5923bb120c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835039(v=office.15)
ms:contentKeyID: 48547976
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052870
f1_categories:
- Office.Version=v15
ms.openlocfilehash: e87c8eba8f8db9eb54bebc9e2e7098e7c26b1b9d
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472703"
---
# <a name="field2fieldsize-property-dao"></a>Field2.FieldSize Property (DAO)


**Betrifft**: Access 2013 | Office 2013


Gibt die in der Datenbank (nicht im Arbeitsspeicher) verwendete Anzahl von Bytes eines Field2-Objekts vom Typ Memo oder Long Binary in der Fields-Auflistung eines Recordset-Objekts zurück.

## <a name="syntax"></a>Syntax

*Ausdruck* . Feldgröße

*Ausdruck* Eine Variable, die ein **Field2** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Sie können die **FieldSize**-Eigenschaft mit den Methoden **[AppendChunk](field-appendchunk-method-dao.md)** und **[GetChunk](field-getchunk-method-dao.md)** zum Bearbeiten großer Felder verwenden.

Da die Größe eines Felds vom Datentyp Long Binary oder Memo 64 KB überschreiten kann, sollten Sie den von der FieldSize-Eigenschaft zurückgegebenen Wert einer Variablen zuordnen, deren Größe zum Speichern einer Long-Variablen ausreicht.

Wenn Sie die Größe eines Field2-Objekts eines anderen Typs als Memo and Long Binary ermitteln möchten, verwenden Sie die Size-Eigenschaft.

  - Der Datenbankserver oder ODBC-Treiber unterstützt keine serverseitigen Cursor.

  - Sie verwenden die ODBC-Cursorbibliothek (d. h. die **DefaultCursorDriver**-Eigenschaft ist auf **dbUseODBC** festgelegt oder auf **dbUseDefault**, wenn der Server keine serverseitigen Cursor unterstützt).

  - Sie verwenden eine Abfrage ohne Cursor (d. h. die **DefaultCursorDriver**-Eigenschaft ist auf **dbUseNoCursor** festgelegt).

Die **FieldSize**-Eigenschaft und die VBA-Funktionen **Len()** oder **LenB()** geben möglicherweise unterschiedliche Werte als Länge derselben Zeichenfolge zurück. Zeichenfolgen werden in einer Microsoft Access-Datenbank in einem MBCS-Format (Multi-Byte Character Set, Mehrbyte-Zeichensatz) gespeichert, jedoch in VBA im Unicode-Format angezeigt. Folglich gibt die **Len()**-Funktion immer die Anzahl von Zeichen, die **LenB**-Funktion immer die Anzahl von Zeichen mal 2 (Unicode verwendet 2 Bytes pro Zeichen) und die **FieldSize**-Eigenschaft einen Wert dazwischen zurück, wenn die Zeichenfolge MBCS-Zeichen enthält. Angenommen, eine Zeichenfolge besteht aus 3 normalen Zeichen und 2 MBCS-Zeichen, dann gibt **Len()** 5 zurück, **LenB()** 10 und **FieldSize** 7, d. h. die Summe von 1 für jedes normale Zeichen und 2 für jedes MBCS-Zeichen.

## <a name="example"></a>Beispiel

Dieses Beispiel veranschaulicht, wie Sie mit der FieldSize-Eigenschaft die Anzahl von Bytes auflisten, die in Field-Objekten vom Typ Memo und Long Binary in zwei verschiedenen Tabellen verwendet werden.

```vb
    Sub FieldSizeX() 
     
     Dim dbsNorthwind As Database 
     Dim rstCategories As Recordset 
     Dim rstEmployees As Recordset 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstCategories = _ 
     dbsNorthwind.OpenRecordset("Categories", _ 
     dbOpenDynaset) 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees", _ 
     dbOpenDynaset) 
     
     Debug.Print _ 
     "Field sizes from records in Categories table" 
     
     With rstCategories 
     Debug.Print " CategoryName - " & _ 
     "Description (bytes) - Picture (bytes)" 
     
     ' Enumerate the Categories Recordset and print the size 
     ' in bytes of the picture field for each record. 
     Do While Not .EOF 
     Debug.Print " " & !CategoryName & " - " & _ 
     !Description.FieldSize & " - " & _ 
     !Picture.FieldSize 
     .MoveNext 
     Loop 
     
     .Close 
     End With 
     
     Debug.Print "Field sizes from records in Employees table" 
     
     With rstEmployees 
     Debug.Print " LastName - Notes (bytes) - " & _ 
     "Photo (bytes)" 
     
     ' Enumerate the Employees Recordset and print the size 
     ' in bytes of the picture field for each record. 
     Do While Not .EOF 
     Debug.Print " " & !LastName & " - " & _ 
     !Notes.FieldSize & " - " & !Photo.FieldSize 
     .MoveNext 
     Loop 
     
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
```

<br/>

In diesem Beispiel werden die Methoden **AppendChunk** und **GetChunk** verwendet, um ein OLE-Objektfeld mit Daten aus einem anderen Datensatz zu füllen (immer jeweils 32 KB). In einer echten Anwendung kann es sinnvoll sein, mit einer Prozedur wie dieser einen Mitarbeiterdatensatz (inklusive Foto des Mitarbeiters) von einer Tabelle in eine andere zu kopieren. In diesem Beispiel wird der Datensatz einfach wieder in dieselbe Tabelle kopiert. Beachten Sie, dass die gesamte Bearbeitung des Abschnitts innerhalb einer einzelnen AddNew-Aktualisierungssequenz erfolgt.

```vb
    Sub AppendChunkX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset 
     Dim rstEmployees2 As Recordset 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     ' Open two recordsets from the Employees table. 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees", _ 
     dbOpenDynaset) 
     Set rstEmployees2 = rstEmployees.Clone 
     
     ' Add a new record to the first Recordset and copy the 
     ' data from a record in the second Recordset. 
     With rstEmployees 
     .AddNew 
     !FirstName = rstEmployees2!FirstName 
     !LastName = rstEmployees2!LastName 
     CopyLargeField rstEmployees2!Photo, !Photo 
     .Update 
     
     ' Delete new record because this is a demonstration. 
     .Bookmark = .LastModified 
     .Delete 
     .Close 
     End With 
     
     rstEmployees2.Close 
     dbsNorthwind.Close 
     
    End Sub 
     
    Function CopyLargeField(fldSource As Field2, _ 
     fldDestination As Field2) 
     
     ' Set size of chunk in bytes. 
     Const conChunkSize = 32768 
     
     Dim lngOffset As Long 
     Dim lngTotalSize As Long 
     Dim strChunk As String 
     
     ' Copy the photo from one Recordset to the other in 32K 
     ' chunks until the entire field is copied. 
     lngTotalSize = fldSource.FieldSize 
     Do While lngOffset < lngTotalSize 
     strChunk = fldSource.GetChunk(lngOffset, conChunkSize) 
     fldDestination.AppendChunk strChunk 
     lngOffset = lngOffset + conChunkSize 
     Loop 
     
    End Function
```