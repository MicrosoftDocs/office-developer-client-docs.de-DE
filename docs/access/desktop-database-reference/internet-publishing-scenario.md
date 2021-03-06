---
title: Szenario für Veröffentlichungen im Internet
TOCTitle: Internet publishing scenario
ms:assetid: 25a3fa8b-86ec-9e72-5e62-bf0d849479b7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249024(v=office.15)
ms:contentKeyID: 48543790
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0f28b14f3eaf6792a74ef0967d698d5a3914955a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291272"
---
# <a name="internet-publishing-scenario"></a>Szenario für Veröffentlichungen im Internet

**Gilt für**: Access 2013, Office 2013

Mit diesem Code wird die Verwendung von ADO (ActiveX Data Objects) mit dem Microsoft OLE DB-Anbieter für Internet Publishing veranschaulicht. In diesem Szenario erstellen Sie eine Visual Basic-Anwendung, von der mithilfe der Objekte **Recordset**, **Record** und **Stream** die Inhalte von Ressourcen angezeigt werden, die mit dem Internet Publishing-Anbieter veröffentlicht wurden.

Für die Erstellung dieses Szenarios sind die folgenden Schritte erforderlich: 

1. Richten Sie das Visual Basic-Projekt ein.
2. Initialisieren Sie das Haupt Listenfeld.
3. Füllen Sie das Listenfeld Felder aus.
4. Füllen Sie das Textfeld Details aus.

## <a name="step-1-set-up-the-visual-basic-project"></a>Schritt 1: Einrichten des Visual Basic-Projekts

Dieses Szenario geht davon aus, dass Sie Microsoft Visual Basic 6.0 oder höher, ADO 2.5 oder höher und den Microsoft OLE DB-Anbieter für Internet Publishing auf dem System installiert haben.

### <a name="create-an-ado-project"></a>Erstellen eines ADO-Projekts

1.  Erstellen Sie in Microsoft Visual Basic ein neues Standard EXE-Projekt.

2.  Klicken Sie im Menü **Project** auf **References**.

3.  Wählen Sie **Microsoft ActiveX Data Objects 2,5 Library**aus, und klicken Sie dann auf **OK**.

### <a name="insert-controls-on-the-main-form"></a>Einfügen von Steuerelementen auf dem Hauptformular

1.  Add a ListBox control to Form1. Legen Sie die **Name** -Eigenschaft auf **von IstMain**.

2.  Add another ListBox control to Form1. Legen Sie die **Name** -Eigenschaft auf **lstDetails**.

3.  Add a TextBox control to Form1. Legen Sie die **Name** -Eigenschaft auf **txtDetails**.

## <a name="step-2-initialize-the-main-list-box"></a>Schritt 2: Initialisieren des Haupt Listenfelds

### <a name="declare-global-record-and-recordset-objects"></a>Deklarieren globaler Daten Satz-und Recordset-Objekte

- Insert the following code into the (General) (Declarations) for Form1:
    
   ```vb 
     
    Option Explicit 
    Dim grec As Record 
    Dim grs As Recordset 
   ```
    
   Dieser Code deklariert globale Objektverweise für die Objekte **Record** und **Recordset**, die später in diesem Szenario verwendet werden.

### <a name="connect-to-a-url-and-populate-lstmain"></a>Herstellen einer Verbindung mit einer URL und Auffüllen von von IstMain

- Fügen Sie im Form Load-Ereignishandler für Form1 den folgenden Code ein:
    
   ```vb 
     
    Private Sub Form_Load() 
        Set grec = New Record 
        Set grs = New Recordset 
        grec.Open "", "URL=https://servername/foldername/", , _ 
            adOpenIfExists Or adCreateCollection 
        Set grs = grec.GetChildren 
        While Not grs.EOF 
            lstMain.AddItem grs(0) 
            grs.MoveNext 
        Wend 
    End Sub 
   ```
    
   Dieser Code instanziiert die globalen Objekte **Record** und **Recordset**. Der **Datensatz** `grec` wird mit einer als **ActiveConnection**angegebenen URL geöffnet. Wenn die URL vorhanden ist, wird Sie geöffnet; Wenn es noch nicht vorhanden ist, wird es erstellt. 
   
   Beachten Sie, dass Sie `https://servername/foldername/` eine gültige URL aus Ihrer Umgebung ersetzen sollten. 
   
   Das **Recordset** `grs` -Objekt wird für die untergeordneten Elemente des **Record** `grec`-Objekts geöffnet. Die von IstMain wird dann mit den Dateinamen der in der URL veröffentlichten Ressourcen aufgefüllt.

## <a name="step-3-populate-the-fields-list-box"></a>Schritt 3: aufFüllen des Listenfelds "Felder"

- Insert the following code into the Click event handler of lstMain:

   ```vb 
    
    Private Sub lstMain_Click() 
        Dim rec As Record 
        Dim rs As Recordset 
        Set rec = New Record 
        Set rs = New Recordset 
        grs.MoveFirst 
        grs.Move lstMain.ListIndex 
        lstDetails.Clear 
        rec.Open grs 
        Select Case rec.RecordType 
            Case adCollectionRecord: 
                Set rs = rec.GetChildren 
                While Not rs.EOF 
                    lstDetails.AddItem rs(0) 
                    rs.MoveNext 
                Wend 
            Case adSimpleRecord: 
                recFields rec, lstDetails, txtDetails 
                
            Case adStructDoc: 
        End Select 
        
    End Sub 
   ```

   Dieser Code deklariert und instanziiert lokale **Record** -und **Recordset** -Objekte `rec` und `rs`/oder.

   Die Zeile, die der in von IstMain ausgewählten Ressource entspricht, ist die aktuelle Zeile `grs`von. Das Listenfeld **Details** wird dann gelöscht und `rec` mit der aktuellen Zeile `grs` als Quelle geöffnet.

   Wenn es sich bei der Ressource um einen Auflistungs Daten **** Satz handelt (wie von RecordType angegeben), wird das lokale `rec` **Recordset** `rs` -Objekt für die untergeordneten Elemente von geöffnet. lstDetails wird dann mit den Werten aus den Zeilen von `rs`gefüllt.

   Wenn die Ressource ein einfacher Datensatz ist, `recFields` wird aufgerufen. Weitere Informationen `recFields`finden Sie im nächsten Schritt.

   Ist die Ressource ein strukturiertes Dokument, wird kein Code implementiert.

## <a name="step-4-populate-the-details-text-box"></a>Schritt 4: aufFüllen des Textfelds "Details"

- Erstellen Sie eine neue Subroutine mit `recFields` dem Namen, und fügen Sie den folgenden Code ein:

   ```vb 
    
    Sub recFields(r As Record, l As ListBox, t As TextBox) 
        Dim f As Field 
        Dim s As Stream 
        Set s = New Stream 
        Dim str As String 
        
        For Each f In r.Fields 
            l.AddItem f.Name & ": " & f.Value 
        Next 
        t.Text = "" 
        If r!RESOURCE_CONTENTCLASS = "text/plain" Then 
            s.Open r, adModeRead, adOpenStreamFromRecord 
            str = s.ReadText(1) 
            s.Position = 0 
            If Asc(Mid(str, 1, 1)) = 63 Then '//63 = "?" 
                s.Charset = "ascii" 
                s.Type = adTypeText 
            End If 
            t.Text = s.ReadText(adReadAll) 
        End If 
    End Sub 
   ```

   Dieser Code füllt lstDetails mit den Feldern und Werten des einfachen Datensatzes, der übergeben `recFields`wird. If the resource is a text file, a text **Stream** is opened from the resource record. Der Code bestimmt, ob der Zeichensatz ASCII ist, und kopiert **** den Inhalt des `txtDetails`Streams in.

