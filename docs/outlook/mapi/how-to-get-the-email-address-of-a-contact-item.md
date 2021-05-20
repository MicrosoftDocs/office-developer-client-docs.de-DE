---
title: Abrufen der E-Mail-Adresse eines Kontaktelements
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 032f7242-5500-1e21-06d3-b2d947eb1043
description: 'Letzte �nderung: Montag, 25. Juni 2012'
ms.openlocfilehash: fab09d0c594bac1374973f523abe6ff0b9c09dd0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429593"
---
# <a name="get-the-email-address-of-a-contact-item"></a>Abrufen der E-Mail-Adresse eines Kontaktelements

**Gilt für**: Outlook 2013 | Outlook 2016 
  
In diesem Thema wird gezeigt, wie Sie den Wert einer benannten Eigenschaft abrufen, die die E-Mail-Adresse eines Microsoft Outlook 2010 oder Microsoft Outlook 2013 darstellt.
  
Sie können bis zu drei E-Mail-Adressen einem Kontaktelement in Outlook 2010 und Outlook 2013 zuordnen. Jede E-Mail-Adresse entspricht einer Eigenschaft des Outlook 2010- oder Outlook 2013 **ContactItem-Objekts** in den Objektmodellen Outlook 2010 und Outlook 2013. Intern in Outlook 2010 und Outlook 2013 entspricht die E-Mail-Adresse auch einer MAPI-benannten Eigenschaft. Die erste E-Mail-Adresse eines Kontakts entspricht beispielsweise der **Email1Address-Eigenschaft** des **ContactItem-Objekts** in den Objektmodellen Outlook 2010 und Outlook 2013 sowie den internen Outlook 2010- und Outlook 2013-Objektmodellen mit dem Namen [PidLidEmail1EmailAddress Canonical Property](pidlidemail1emailaddress-canonical-property.md).
  
Zum Abrufen des Werts einer E-Mail-Adresse eines Kontaktelements können Sie das **PropertyAccessor-Objekt** des Outlook 2010- oder Outlook 2013-Objektmodells verwenden oder zunächst [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) verwenden, um das Eigenschaftstag der benannten Eigenschaft zu erhalten, und dieses Eigenschaftstag dann in [IMAPIProp::GetProps](imapiprop-getprops.md) angeben, um den Wert zu erhalten. Geben Sie beim Aufrufen von **IMAPIProp::GetIDsFromNames** die entsprechenden Werte für die [MAPINAMEID-Struktur](mapinameid.md) an, auf die der Eingabeparameter _lppPropNames zeigt._ Das folgende Codebeispiel zeigt, wie Sie die erste E-Mail-Adresse eines angegebenen Kontakts mit `lpContact` **GetIDsFromNames** und **GetProps abrufen.** 
  
```cpp
HRESULT HrGetEmail1(LPMESSAGE lpContact) 
{ 
    HRESULT hRes = S_OK; 
    LPSPropTagArray lpNamedPropTags = NULL; 
    MAPINAMEID NamedID = {0}; 
    LPMAPINAMEID lpNamedID = &NamedID; 
    NamedID.lpguid = (LPGUID)&PSETID_Address; 
    NamedID.ulKind = MNID_ID; 
    NamedID.Kind.lID = dispidEmailEmailAddress; 
 
    hRes = lpContact->GetIDsFromNames( 
           1,  
           &lpNamedID,  
           NULL,  
           &lpNamedPropTags); 
 
    if (SUCCEEDED(hRes) && lpNamedPropTags) 
    { 
        SPropTagArray sPropTagArray; 
 
        sPropTagArray.cValues = 1; 
        sPropTagArray.aulPropTag[0] = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[0],PT_STRING8); 
        LPSPropValue lpProps = NULL; 
        ULONG cProps = 0; 
 
        hRes = lpContact->GetProps( 
               &sPropTagArray, 
               NULL, 
               &cProps, 
               &lpProps); 
        if (SUCCEEDED(hRes) &&  
            1 == cProps &&  
            lpProps &&  
            PT_STRING8 == PROP_TYPE(lpProps[0].ulPropTag) && 
            lpProps[0].Value.lpszA) 
        { 
            printf("Email address 1 = \"%s\"\n",lpProps[0].Value.lpszA); 
        } 
        MAPIFreeBuffer(lpProps); 
        MAPIFreeBuffer(lpNamedPropTags); 
     } 
     return hRes; 
}
```


