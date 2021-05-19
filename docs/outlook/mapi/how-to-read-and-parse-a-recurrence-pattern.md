---
title: Lesen und Analysieren eines Serienmusters
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 75113097-b3ae-4d20-9796-85c62a592ef0
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: c226fe79fd002cda3c557fc8416c25f98ad33626
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345927"
---
# <a name="read-and-parse-a-recurrence-pattern"></a>Lesen und Analysieren eines Serienmusters
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
MAPI kann zum Lesen und Analysieren eines Serienmusters für einen Termin verwendet werden.
  
Informationen zum Herunterladen, Anzeigen und Ausführen des Codes aus dem MFCMAPI-Anwendungsprojekt, auf das in diesem Thema verwiesen wird, finden Sie unter [Install the Samples Used in This Section](how-to-install-the-samples-used-in-this-section.md).

### <a name="to-parse-a-recurrence-blob"></a>So analysieren Sie ein Serien-Blob

1. Öffnen Sie ein Terminelement. Informationen zum Öffnen einer Nachricht finden Sie unter [Opening a Message](opening-a-message.md).
    
2. Rufen Sie die benannte **Eigenschaft dispidApptRecur** ([PidLidAppointmentRecur Canonical Property](pidlidappointmentrecur-canonical-property.md)) ab. Informationen zum Abrufen benannter Eigenschaften finden Sie unter [MAPI Named Properties](mapi-named-properties.md).
    
3. Befolgen Sie die Anweisungen in [[MS-OXOCAL]](https://msdn.microsoft.com/library/cc425490%28EXCHG.80%29.aspx) zum Lesen der Terminserienmusterstruktur. 
    
Die MFCMAPI-Referenzanwendung veranschaulicht den letzten Schritt mit der Funktion in der  `BinToAppointmentRecurrencePatternStruct` InterpretProp2.cpp-Quelldatei des MFCMapi-Projekts. Die  `BinToAppointmentRecurrencePatternStruct` Funktion verwendet einen Zeiger auf einen Puffer im Arbeitsspeicher als Parameter. Die MFCMAPI-Anwendung ruft diesen Puffer ab, indem sie zunächst die **benannte eigenschaft dispidApptRecur** einem Eigenschaftstag zuzuordnen und dann den Wert der Eigenschaft mithilfe der [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) anfordert. Wenn die Eigenschaft zu groß ist, um sie mithilfe der **GetProps-Methode** abzurufen, öffnet MFCMAPI eine Streamschnittstelle, um die Eigenschaft mithilfe der [IMAPIProp::OpenProperty-Methode abzurufen.](imapiprop-openproperty.md) Die MFCMAPI-Anwendung liest dann die Daten aus dem Datenstrom, um den Puffer zu erstellen. 
  
Informationen zum Format des Puffers finden Sie unter [PidLidAppointmentRecur Canonical Property](pidlidappointmentrecur-canonical-property.md). Der Großteil der Daten im Puffer besteht aus Feldern mit einer festen Anzahl von Bytes, die eins nach dem anderen gelesen werden müssen. Einige Felder sind nur vorhanden, wenn andere Felder bestimmte Werte enthalten, und die Größe einiger Felder kann vom Wert anderer Felder abhängen. Die Analyse des Puffers zum Lesen der verschiedenen Felder erfordert viel Buchhaltung. MFCMAPI verwendet eine interne Hilfsklasse namens,  `CBinaryParser` um diese Buchhaltung zu kapseln. Die Funktion überprüft beispielsweise, ob genügend Bytes im Puffer verbleiben, um ein DWORD zu lesen, und liest dann den Wert und aktualisiert  `CBinaryParser::GetDWORD` die Zeiger. 
  
Nachdem der Puffer in eine Struktur analysiert wurde, verwendet die MFCMAPI-Anwendung die Funktion, um die Struktur in eine Zeichenfolge zu konvertieren, die dem Benutzer  `AppointmentRecurrencePatternStructToString` angezeigt wird. Dies ist nicht dieselbe Zeichenfolge, Outlook angezeigt wird, sondern eine rohe Ansicht der Daten, auf denen Outlook erstellt. 
  
Es ist möglich, einen Puffer zu finden, der beschädigte Daten oder mehr Daten enthält, als zum Codieren eines Serienmusters erforderlich sind. Um diese Szenarien zu identifizieren, verfolgt die MFCMAPI-Anwendung, wie viele Daten erfolgreich analysiert wurden und wie viel im Puffer verbleibt. Wenn daten im Puffer bleiben, nachdem die Analyse abgeschlossen ist, enthält MFCMAPI diese "Junkdaten" in die Struktur, damit sie untersucht werden können.
  
Im Folgenden finden Sie die vollständige Auflistung der  `BinToAppointmentRecurrencePatternStruct` Funktion. 
  
```cpp
AppointmentRecurrencePatternStruct* BinToAppointmentRecurrencePatternStruct(ULONG cbBin, LPBYTE lpBin)
{
   if (!lpBin) return NULL;
   AppointmentRecurrencePatternStruct arpPattern = {0};
   CBinaryParser Parser(cbBin,lpBin);
   size_t cbBinRead = 0;
   arpPattern.RecurrencePattern = BinToRecurrencePatternStruct(cbBin,lpBin,&cbBinRead);
   Parser.Advance(cbBinRead);
   Parser.GetDWORD(&arpPattern.ReaderVersion2);
   Parser.GetDWORD(&arpPattern.WriterVersion2);
   Parser.GetDWORD(&arpPattern.StartTimeOffset);
   Parser.GetDWORD(&arpPattern.EndTimeOffset);
   Parser.GetWORD(&arpPattern.ExceptionCount);
   if (arpPattern.ExceptionCount &&
      arpPattern.ExceptionCount == arpPattern.RecurrencePattern->ModifiedInstanceCount &&
      arpPattern.ExceptionCount < _MaxExceptions)
   {
      arpPattern.ExceptionInfo = new ExceptionInfoStruct[arpPattern.ExceptionCount];
      if (arpPattern.ExceptionInfo)
      {
         memset(arpPattern.ExceptionInfo,0,sizeof(ExceptionInfoStruct) * arpPattern.ExceptionCount);
         WORD i = 0;
         for (i = 0 ; i < arpPattern.ExceptionCount ; i++)
         {
            Parser.GetDWORD(&arpPattern.ExceptionInfo[i].StartDateTime);
            Parser.GetDWORD(&arpPattern.ExceptionInfo[i].EndDateTime);
            Parser.GetDWORD(&arpPattern.ExceptionInfo[i].OriginalStartDate);
            Parser.GetWORD(&arpPattern.ExceptionInfo[i].OverrideFlags);
            if (arpPattern.ExceptionInfo[i].OverrideFlags & ARO_SUBJECT)
            {
               Parser.GetWORD(&arpPattern.ExceptionInfo[i].SubjectLength);
               Parser.GetWORD(&arpPattern.ExceptionInfo[i].SubjectLength2);
               if (arpPattern.ExceptionInfo[i].SubjectLength2 && arpPattern.ExceptionInfo[i].SubjectLength2 + 1 
                  == arpPattern.ExceptionInfo[i].SubjectLength)
               {
                  Parser.GetStringA(arpPattern.ExceptionInfo[i].SubjectLength2,&arpPattern.ExceptionInfo[i].Subject);
               }
            }
            if (arpPattern.ExceptionInfo[i].OverrideFlags & ARO_MEETINGTYPE)
            {
               Parser.GetDWORD(&arpPattern.ExceptionInfo[i].MeetingType);
            }
            if (arpPattern.ExceptionInfo[i].OverrideFlags & ARO_REMINDERDELTA)
            {
               Parser.GetDWORD(&arpPattern.ExceptionInfo[i].ReminderDelta);
            }
            if (arpPattern.ExceptionInfo[i].OverrideFlags & ARO_REMINDER)
            {
               Parser.GetDWORD(&arpPattern.ExceptionInfo[i].ReminderSet);
            }
            if (arpPattern.ExceptionInfo[i].OverrideFlags & ARO_LOCATION)
            {
               Parser.GetWORD(&arpPattern.ExceptionInfo[i].LocationLength);
               Parser.GetWORD(&arpPattern.ExceptionInfo[i].LocationLength2);
               if (arpPattern.ExceptionInfo[i].LocationLength2 && arpPattern.ExceptionInfo[i].LocationLength2 
                  + 1 == arpPattern.ExceptionInfo[i].LocationLength)
               {
                  Parser.GetStringA(arpPattern.ExceptionInfo[i].LocationLength2,&arpPattern.ExceptionInfo[i].Location);
               }
            }
            if (arpPattern.ExceptionInfo[i].OverrideFlags & ARO_BUSYSTATUS)
            {
               Parser.GetDWORD(&arpPattern.ExceptionInfo[i].BusyStatus);
            }
            if (arpPattern.ExceptionInfo[i].OverrideFlags & ARO_ATTACHMENT)
            {
               Parser.GetDWORD(&arpPattern.ExceptionInfo[i].Attachment);
            }
            if (arpPattern.ExceptionInfo[i].OverrideFlags & ARO_SUBTYPE)
            {
               Parser.GetDWORD(&arpPattern.ExceptionInfo[i].SubType);
            }
            if (arpPattern.ExceptionInfo[i].OverrideFlags & ARO_APPTCOLOR)
            {
               Parser.GetDWORD(&arpPattern.ExceptionInfo[i].AppointmentColor);
            }
         }
      }
   }
   Parser.GetDWORD(&arpPattern.ReservedBlock1Size);
   if (arpPattern.ReservedBlock1Size && arpPattern.ReservedBlock1Size < _MaxReservedBlock)
   {
      Parser.GetBYTES(arpPattern.ReservedBlock1Size,&arpPattern.ReservedBlock1);
   }
   if (arpPattern.ExceptionCount &&
      arpPattern.ExceptionCount == arpPattern.RecurrencePattern->ModifiedInstanceCount &&
      arpPattern.ExceptionCount < _MaxExceptions &&
      arpPattern.ExceptionInfo)
   {
      arpPattern.ExtendedException = new ExtendedExceptionStruct[arpPattern.ExceptionCount];
      if (arpPattern.ExtendedException)
      {
         memset(arpPattern.ExtendedException,0,sizeof(ExtendedExceptionStruct) * arpPattern.ExceptionCount);
         WORD i = 0;
         for (i = 0 ; i < arpPattern.ExceptionCount ; i++)
         {
            if (arpPattern.WriterVersion2 >= 0x0003009)
            {
               Parser.GetDWORD(&arpPattern.ExtendedException[i].ChangeHighlight.ChangeHighlightSize);
               Parser.GetDWORD(&arpPattern.ExtendedException[i].ChangeHighlight.ChangeHighlightValue);
               if (arpPattern.ExtendedException[i].ChangeHighlight.ChangeHighlightSize > sizeof(DWORD))
               {
                  Parser.GetBYTES(arpPattern.ExtendedException[i].ChangeHighlight.ChangeHighlightSize 
                     - sizeof(DWORD),&arpPattern.ExtendedException[i].ChangeHighlight.Reserved);
               }
            }
            Parser.GetDWORD(&arpPattern.ExtendedException[i].ReservedBlockEE1Size);
            if (arpPattern.ExtendedException[i].ReservedBlockEE1Size &&
                arpPattern.ExtendedException[i].ReservedBlockEE1Size < _MaxReservedBlock)
            {
               Parser.GetBYTES(arpPattern.ExtendedException[i].ReservedBlockEE1Size,&arpPattern.ExtendedException[i].ReservedBlockEE1);
            }
            if (arpPattern.ExceptionInfo[i].OverrideFlags & ARO_SUBJECT ||
               arpPattern.ExceptionInfo[i].OverrideFlags & ARO_LOCATION)
            {
               Parser.GetDWORD(&arpPattern.ExtendedException[i].StartDateTime);
               Parser.GetDWORD(&arpPattern.ExtendedException[i].EndDateTime);
               Parser.GetDWORD(&arpPattern.ExtendedException[i].OriginalStartDate);
            }
            if (arpPattern.ExceptionInfo[i].OverrideFlags & ARO_SUBJECT)
            {
               Parser.GetWORD(&arpPattern.ExtendedException[i].WideCharSubjectLength);
               if (arpPattern.ExtendedException[i].WideCharSubjectLength)
               {
                  Parser.GetStringW(arpPattern.ExtendedException[i].WideCharSubjectLength,&arpPattern.ExtendedException[i].WideCharSubject);
               }
            }
            if (arpPattern.ExceptionInfo[i].OverrideFlags & ARO_LOCATION)
            {
               Parser.GetWORD(&arpPattern.ExtendedException[i].WideCharLocationLength);
               if (arpPattern.ExtendedException[i].WideCharLocationLength)
               {
                  Parser.GetStringW(arpPattern.ExtendedException[i].WideCharLocationLength,&arpPattern.ExtendedException[i].WideCharLocation);
               }
            }
            if (arpPattern.ExceptionInfo[i].OverrideFlags & ARO_SUBJECT ||
               arpPattern.ExceptionInfo[i].OverrideFlags & ARO_LOCATION)
            {
               Parser.GetDWORD(&arpPattern.ExtendedException[i].ReservedBlockEE2Size);
               if (arpPattern.ExtendedException[i].ReservedBlockEE2Size && arpPattern.ExtendedException[i].ReservedBlockEE2Size < _MaxReservedBlock)
               {
                  Parser.GetBYTES(arpPattern.ExtendedException[i].ReservedBlockEE2Size,&arpPattern.ExtendedException[i].ReservedBlockEE2);
               }
            }
         }
      }
   }
   Parser.GetDWORD(&arpPattern.ReservedBlock2Size);
   if (arpPattern.ReservedBlock2Size && arpPattern.ReservedBlock2Size < _MaxReservedBlock)
   {
      Parser.GetBYTES(arpPattern.ReservedBlock2Size,&arpPattern.ReservedBlock2);
   }
   // Junk data remains.
   if (Parser.RemainingBytes() > 0)
   {
      arpPattern.JunkDataSize = Parser.RemainingBytes();
      Parser.GetBYTES(arpPattern.JunkDataSize,&arpPattern.JunkData);
   }
   AppointmentRecurrencePatternStruct* parpPattern = new AppointmentRecurrencePatternStruct;
   if (parpPattern)
   {
      *parpPattern = arpPattern;
   }
   return parpPattern;
}

```

## <a name="see-also"></a>Siehe auch

- [Verwenden von MAPI zum Erstellen Outlook 2007-Elementen](https://msdn.microsoft.com/library/cc678348%28office.12%29.aspx)

