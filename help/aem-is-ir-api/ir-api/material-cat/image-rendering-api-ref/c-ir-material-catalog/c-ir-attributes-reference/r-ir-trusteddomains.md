---
description: Flash應用程式Web域。 AdobeFlash應用程式可能需要訪問以swf格式傳送的影像的屬性。swf必須通過註冊其信任的應用程式域的名稱來顯式授予訪問權。
solution: Experience Manager
title: TrustedDomains *
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 41794f62-6140-4e54-9de2-908b20c51b37
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 3%

---

# TrustedDomains *{#trusteddomains}

Flash應用程式Web域。 AdobeFlash應用程式可能需要訪問以swf格式傳送的影像的屬性。swf必須通過註冊其信任的應用程式域的名稱來顯式授予訪問權。

## 屬性 {#section-5d6ecfa431a04abd8628a28e0ab3be83}

包含以逗號分隔的Web域名清單的字串。 如果為空，則必須從與影像呈現相同的域為應用程式提供服務，才能訪問[!DNL swf]格式化響應中的影像屬性。

## 預設 {#section-8fae0c896f7d46e7a61b0fd7e2b34dc3}

從`default::TrustedDomains`繼承（如果不存在）。

## 另請參閱 {#section-2f829671c385411d8e1a7525def5529f}

[src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272) ,  `mask=`, [屬性：:RootUrl](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rooturl.md#reference-b8d706a573814802bd6794223cc78402)
