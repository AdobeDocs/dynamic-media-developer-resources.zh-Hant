---
description: Flash應用程式Web域。 AdobeFlash應用程式可能需要訪問使用fmt=swf或fmt=swf3傳送的影像的屬性。
solution: Experience Manager
title: 受信任的域
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 925ac9d1-203c-4814-a701-71060bf47c20
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 3%

---

# 受信任的域{#trusteddomains}

Flash應用程式Web域。 AdobeFlash應用程式可能需要訪問使用fmt=swf或fmt=swf3傳送的影像的屬性。

swf必須通過註冊它信任的應用程式域的名稱來顯式授予訪問權。

## 屬性 {#section-e7f95bbb749f441e83e90c2bc3d5a6e0}

包含以逗號分隔的Web域名清單的字串。 如果為空，則必須從與影像呈現相同的域提供應用程式，才能訪問swf格式響應中的影像屬性。

## 預設 {#section-5c52ed3c7310488380f5a6f9540bf981}

從`default::TrustedDomains`繼承（如果不存在）。

## 另請參閱 {#section-65d0846e41674882a4d0d56a8f6d524b}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
