---
description: Flash應用程式網域。 AdobeFlash應用程式可能需要存取以swf格式傳送的影像屬性。swf必須註冊其信任的應用程式網域名稱，以明確授與存取權。
solution: Experience Manager
title: TrustedDomains *
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 3%

---


# TrustedDomains *{#trusteddomains}

Flash應用程式網域。 AdobeFlash應用程式可能需要存取以swf格式傳送的影像屬性。swf必須註冊其信任的應用程式網域名稱，以明確授與存取權。

## 屬性 {#section-5d6ecfa431a04abd8628a28e0ab3be83}

包含以逗號分隔的Web域名清單的字串。 如果為空，則必須從與「影像演算」相同的網域提供應用程式，才能存取[!DNL swf]格式化回應中的影像屬性。

## 預設 {#section-8fae0c896f7d46e7a61b0fd7e2b34dc3}

繼承自`default::TrustedDomains`（如果不存在）。

## 另請參閱 {#section-2f829671c385411d8e1a7525def5529f}

[src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272) ,  `mask=`，屬 [性：:RootUrl](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rooturl.md#reference-b8d706a573814802bd6794223cc78402)
