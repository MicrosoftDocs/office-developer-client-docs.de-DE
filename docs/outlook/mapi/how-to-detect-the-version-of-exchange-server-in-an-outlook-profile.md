---
title: Ermitteln der Version des Exchange-Servers in einem Outlook-Profil
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e2d8d8a9-7e8f-9cf0-56a8-d8a6281ad589
description: 'Letzte Änderung: 03. Juli 2012'
ms.openlocfilehash: c6aaac128e1a3e1a8d77d3fa8b6c50a335348b71
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424448"
---
# <a name="detect-the-version-of-exchange-server-in-an-outlook-profile"></a>Ermitteln der Version des Exchange-Servers in einem Outlook-Profil

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Dieses Thema enthält ein Codebeispiel in C++, in dem gezeigt wird, wie Sie die **[PR_PROFILE_SERVER_VERSION-](pidtagprofileserverversion-canonical-property.md)** und **[PR_PROFILE_SERVER_FULL_VERSION-Eigenschaft](pidtagprofileserverfullversion-canonical-property.md)** verwenden, um Versionsinformationen des Microsoft Exchange Server abrufen, mit dem das aktive Konto verbunden ist. 
  
Die  `GetProfileServiceVersion` Funktion im Codebeispiel akzeptiert ein Profil als Eingabeparameter. Je nachdem, ob **die PR_PROFILE_SERVER_VERSION-Eigenschaft** und die **PR_PROFILE_SERVER_FULL_VERSION-Eigenschaft** im angegebenen Profil vorhanden sind, ruft die Funktion jede Eigenschaft ab und gibt die entsprechenden Versionsinformationen als Ausgabeparameter zurück. 
  
`GetProfileServiceVersion` ruft zuerst die **[MAPIAdminProfiles-Funktion](mapiadminprofiles.md)** auf, um ein Profilverwaltungsobjekt zu erstellen. Anschließend wird das Profilverwaltungsobjekt zum Aufrufen von **[IProfAdmin::AdminServices verwendet,](iprofadmin-adminservices.md)** um ein Nachrichtendienstverwaltungsobjekt zu erhalten. Mithilfe des Nachrichtendienstverwaltungsobjekts ruft es **[IMsgServiceAdmin::OpenProfileSection](imsgserviceadmin-openprofilesection.md)** auf, um einen Abschnitt des aktuellen Profils zu erhalten, und ruft **[dann HrGetOneProp](hrgetoneprop.md)** auf, um zu überprüfen, ob jede der beiden Eigenschaften in diesem Abschnitt des Profils vorhanden ist, und legt, falls ja, die Versionsinformationen in den entsprechenden Ausgabeparametern fest. 
  
```cpp
TZDEFINITION* BinToTZDEFINITION(ULONG cbDef, LPBYTE lpbDef) 
{ 
    if (!lpbDef) return NULL; 
 
    // Update this if parsing code is changed. 
    // This checks the size up to the flag member. 
    if (cbDef &lt; 2*sizeof(BYTE) + 2*sizeof(WORD)) return NULL; 
 
    TZDEFINITION tzDef = {0}; 
    TZRULE* lpRules = NULL; 
    LPBYTE lpPtr = lpbDef; 
    WORD cchKeyName = NULL; 
    WCHAR* szKeyName = NULL; 
    WORD i = 0; 
 
    BYTE bMajorVersion = *((BYTE*)lpPtr); 
    lpPtr += sizeof(BYTE); 
    BYTE bMinorVersion = *((BYTE*)lpPtr); 
    lpPtr += sizeof(BYTE); 
 
    // We only understand TZ_BIN_VERSION_MAJOR 
    if (TZ_BIN_VERSION_MAJOR != bMajorVersion) return NULL; 
 
    // We only understand if &gt;= TZ_BIN_VERSION_MINOR 
    if (TZ_BIN_VERSION_MINOR &gt; bMinorVersion) return NULL; 
 
    lpPtr += sizeof(WORD); 
 
    tzDef.wFlags = *((WORD*)lpPtr); 
    lpPtr += sizeof(WORD); 
 
    if (TZDEFINITION_FLAG_VALID_GUID &amp; tzDef.wFlags) 
    { 
        if (lpbDef + cbDef - lpPtr &lt; sizeof(GUID)) return NULL; 
        tzDef.guidTZID = *((GUID*)lpPtr); 
        lpPtr += sizeof(GUID); 
    } 
 
    if (TZDEFINITION_FLAG_VALID_KEYNAME &amp; tzDef.wFlags) 
    { 
        if (lpbDef + cbDef - lpPtr &lt; sizeof(WORD)) return NULL; 
        cchKeyName = *((WORD*)lpPtr); 
        lpPtr += sizeof(WORD); 
        if (cchKeyName) 
        { 
            if (lpbDef + cbDef - lpPtr &lt; (BYTE)sizeof(WORD)*cchKeyName) return NULL; 
            szKeyName = (WCHAR*)lpPtr; 
            lpPtr += cchKeyName*sizeof(WORD); 
        } 
    } 
 
    if (lpbDef+ cbDef - lpPtr &lt; sizeof(WORD)) return NULL; 
    tzDef.cRules = *((WORD*)lpPtr); 
    lpPtr += sizeof(WORD); 
    if (tzDef.cRules) 
    { 
        lpRules = new TZRULE[tzDef.cRules]; 
        if (!lpRules) return NULL; 
 
        LPBYTE lpNextRule = lpPtr; 
        BOOL bRuleOK = false; 

```


