---
title: BOF-, EOF- und Bookmark-Eigenschaft (Beispiel) (VB)
TOCTitle: BOF, EOF, and Bookmark Properties Example (VB)
ms:assetid: 30d4b424-b3d8-292f-7553-bb15b094eef8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249085(v=office.15)
ms:contentKeyID: 48544037
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 88c0cecb83e83f3572e0e78c2bcc4fb4e4235c17
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474382"
---
# <a name="bof-eof-and-bookmark-properties-example-vb"></a>BOF-, EOF- und Bookmark-Eigenschaft (Beispiel) (VB)


**Betrifft**: Access 2013 | Office 2013

In diesem Beispiel wird mithilfe der Eigenschaften [BOF](bof-eof-properties-ado.md) und [EOF](bof-eof-properties-ado.md) eine Nachricht angezeigt, falls ein Benutzer versucht, über den ersten oder letzten Datensatz eines [Recordset](recordset-object-ado.md)-Objekts hinaus zu navigieren. Mit der [Bookmark](bookmark-property-ado.md)-Eigenschaft kann der Benutzer einen Datensatz in einem **Recordset** -Objekt kennzeichnen und später zu diesem zurückkehren.

```vb 
 
'BeginBOFVB 
 
 'To integrate this code 
 'replace the data source and initial catalog values 
 'in the connection string 
 
Public Sub Main() 
 On Error GoTo ErrorHandler 
 
 'recordset and connection variables 
 Dim Cnxn As ADODB.Connection 
 Dim rstPublishers As ADODB.Recordset 
 Dim strCnxn As String 
 Dim strSQLPubs As String 
 'record variables 
 Dim strMessage As String 
 Dim intCommand As Integer 
 Dim varBookmark As Variant 
 
 ' open connection 
 Set Cnxn = New ADODB.Connection 
 strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Pubs';Integrated Security='SSPI';" 
 Cnxn.Open strCnxn 
 
 ' Open recordset and use client cursor 
 ' to enable AbsolutePosition property 
 Set rstPublishers = New ADODB.Recordset 
 strSQLPubs = "SELECT pub_id, pub_name FROM publishers ORDER BY pub_name" 
 rstPublishers.Open strSQLPubs, strCnxn, adUseClient, adOpenStatic, adCmdText 
 
 rstPublishers.MoveFirst 
 Do Until rstPublishers.EOF 
 ' Display information about current record 
 ' and get user input 
 strMessage = "Publisher: " & rstPublishers!pub_name & _ 
 vbCr & "(record " & rstPublishers.AbsolutePosition & _ 
 " of " & rstPublishers.RecordCount & ")" & vbCr & vbCr & _ 
 "Enter command:" & vbCr & _ 
 "[1 - next / 2 - previous /" & vbCr & _ 
 "3 - set bookmark / 4 - go to bookmark]" 
 intCommand = Val(InputBox(strMessage)) 
 
 ' Check user input 
 Select Case intCommand 
 Case 1 
 ' Move forward trapping for EOF 
 rstPublishers.MoveNext 
 If rstPublishers.EOF Then 
 MsgBox "Moving past the last record." & _ 
 vbCr & "Try again." 
 rstPublishers.MoveLast 
 End If 
 Case 2 
 ' Move backward trapping for BOF 
 rstPublishers.MovePrevious 
 If rstPublishers.BOF Then 
 MsgBox "Moving past the first record." & _ 
 vbCr & "Try again." 
 rstPublishers.MoveFirst 
 End If 
 Case 3 
 ' Store the bookmark of the current record 
 varBookmark = rstPublishers.Bookmark 
 Case 4 
 ' Go to the record indicated by the stored bookmark 
 If IsEmpty(varBookmark) Then 
 MsgBox "No Bookmark set!" 
 Else 
 rstPublishers.Bookmark = varBookmark 
 End If 
 Case Else 
 Exit Do 
 End Select 
 Loop 
 
 ' clean up 
 rstPublishers.Close 
 Cnxn.Close 
 Set rstPublishers = Nothing 
 Set Cnxn = Nothing 
 Exit Sub 
 
ErrorHandler: 
 ' clean up 
 If Not rstPublishers Is Nothing Then 
 If rstPublishers.State = adStateOpen Then rstPublishers.Close 
 End If 
 Set rstPublishers = Nothing 
 
 If Not Cnxn Is Nothing Then 
 If Cnxn.State = adStateOpen Then Cnxn.Close 
 End If 
 Set Cnxn = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
'EndBOFVB 
```

In diesem Beispiel wird mithilfe der Eigenschaften **Bookmark** und [Filter](filter-property-ado.md) eine begrenzte Ansicht des **Recordset** -Objekts erstellt. Der Zugriff ist nur auf Datensätze möglich, auf die vom Lesezeichenarray verwiesen wird.

```vb 
 
'BeginBOF2VB 
Public Sub Main() 
 On Error GoTo ErrorHandler 
 
 'recordset and connection variables 
 Dim rs As New ADODB.Recordset 
 Dim Cnxn As ADODB.Connection 
 Dim strSQL As String 
 Dim strCnxn As String 
 
 Dim bmk(10) 
 
 ' open connection 
 Set Cnxn = New ADODB.Connection 
 strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Pubs';Integrated Security='SSPI';" 
 Cnxn.Open strCnxn 
 
 'open the recordset client-side 
 Set rs = New ADODB.Recordset 
 strSQL = "Select * from Authors" 
 rs.Open strSQL, Cnxn, adUseClient, adLockReadOnly, adCmdText 
 Debug.Print "Number of records before filtering: ", rs.RecordCount 
 
 Dim ii As Integer 
 ii = 0 
 
 If rs.EOF <> True And ii < 11 Then 
 Do 
 If Not (rs.EOF <> True And ii < 11) Then Exit Do 
 bmk(ii) = rs.Bookmark 
 ii = ii + 1 
 rs.Move 2 
 Loop Until rs.EOF 
 End If 
 
 rs.Filter = bmk 
 Debug.Print "Number of records after filtering: ", rs.RecordCount 
 
 rs.MoveFirst 
 If rs.EOF <> True Then 
 Do 
 Debug.Print rs.AbsolutePosition, rs("au_lname") 
 rs.MoveNext 
 Loop Until rs.EOF 
 End If 
 
 ' clean up 
 rs.Close 
 Cnxn.Close 
 Set rs = Nothing 
 Set Cnxn = Nothing 
 Exit Sub 
 
ErrorHandler: 
 ' clean up 
 If Not rs Is Nothing Then 
 If rs.State = adStateOpen Then rs.Close 
 End If 
 Set rs = Nothing 
 
 If Not Cnxn Is Nothing Then 
 If Cnxn.State = adStateOpen Then Cnxn.Close 
 End If 
 Set Cnxn = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
'EndBOF2VB 
```
