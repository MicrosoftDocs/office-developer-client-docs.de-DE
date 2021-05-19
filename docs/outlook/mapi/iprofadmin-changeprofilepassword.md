---
title: IProfAdminChangeProfilePassword
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.ChangeProfilePassword
api_type:
- COM
ms.assetid: a41f707a-5c84-49aa-aeb6-469b2600e181
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: c7124c8e3f2ced66d303321ff7aee8592a723a2b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420241"
---
# <a name="iprofadminchangeprofilepassword"></a><span data-ttu-id="2c503-103">IProfAdmin::ChangeProfilePassword</span><span class="sxs-lookup"><span data-stu-id="2c503-103">IProfAdmin::ChangeProfilePassword</span></span>

  
  
<span data-ttu-id="2c503-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2c503-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2c503-105">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="2c503-105">Deprecated.</span></span> <span data-ttu-id="2c503-106">Ändert das Kennwort für ein Profil.</span><span class="sxs-lookup"><span data-stu-id="2c503-106">Changes the password for a profile.</span></span>
  
```cpp
HRESULT ChangeProfilePassword(
  LPSTR lpszProfileName,
  LPSTR lpszOldPassword,
  LPSTR lpszNewPassword,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="2c503-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="2c503-107">Parameters</span></span>

 <span data-ttu-id="2c503-108">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="2c503-108">_lpszProfileName_</span></span>
  
> <span data-ttu-id="2c503-109">[in] Ein Zeiger auf den Namen des Profils, das dem zu ändernde Kennwort zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="2c503-109">[in] A pointer to the name of the profile associated with the password to be changed.</span></span>
    
 <span data-ttu-id="2c503-110">_lpszOldPassword_</span><span class="sxs-lookup"><span data-stu-id="2c503-110">_lpszOldPassword_</span></span>
  
> <span data-ttu-id="2c503-111">[in] Ein Zeiger auf das aktuelle Kennwort.</span><span class="sxs-lookup"><span data-stu-id="2c503-111">[in] A pointer to the current password.</span></span>
    
 <span data-ttu-id="2c503-112">_lpszNewPassword_</span><span class="sxs-lookup"><span data-stu-id="2c503-112">_lpszNewPassword_</span></span>
  
> <span data-ttu-id="2c503-113">[in] Ein Zeiger auf das neue Kennwort.</span><span class="sxs-lookup"><span data-stu-id="2c503-113">[in] A pointer to the new password.</span></span>
    
 <span data-ttu-id="2c503-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="2c503-114">_ulFlags_</span></span>
  
> <span data-ttu-id="2c503-115">[in] Eine Bitmaske mit Flags, die den Typ der übergebenen Zeichenfolgen steuert.</span><span class="sxs-lookup"><span data-stu-id="2c503-115">[in] A bitmask of flags that controls the type of the passed-in strings.</span></span> <span data-ttu-id="2c503-116">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="2c503-116">The following flag can be set:</span></span>
    
<span data-ttu-id="2c503-117">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="2c503-117">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="2c503-118">Der Profilname und die Kennwörter sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="2c503-118">The profile name and passwords are in Unicode format.</span></span> <span data-ttu-id="2c503-119">Wenn das MAPI_UNICODE nicht festgelegt ist, sind diese Zeichenfolgen im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="2c503-119">If the MAPI_UNICODE flag is not set, these strings are in ANSI format.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2c503-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2c503-120">Return value</span></span>

<span data-ttu-id="2c503-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="2c503-121">S_OK</span></span> 
  
> <span data-ttu-id="2c503-122">Wenn diese Methode aufgerufen wird, gibt sie S_OK.</span><span class="sxs-lookup"><span data-stu-id="2c503-122">If this method is called, it will return S_OK.</span></span> <span data-ttu-id="2c503-123">Es werden jedoch keine Aktionen ergriffen.</span><span class="sxs-lookup"><span data-stu-id="2c503-123">However, no action will be taken.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2c503-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2c503-124">Remarks</span></span>

<span data-ttu-id="2c503-125">Verwenden Sie diese Methode nicht.</span><span class="sxs-lookup"><span data-stu-id="2c503-125">Do not use this method.</span></span> <span data-ttu-id="2c503-126">MAPI unterstützt keine Kennwörter für Profile.</span><span class="sxs-lookup"><span data-stu-id="2c503-126">MAPI does not support passwords for profiles.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2c503-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2c503-127">See also</span></span>



[<span data-ttu-id="2c503-128">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2c503-128">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)

