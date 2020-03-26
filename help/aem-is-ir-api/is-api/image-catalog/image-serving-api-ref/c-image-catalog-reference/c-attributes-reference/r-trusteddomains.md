---
description: Flash應用程式網域。 Adobe Flash應用程式可能需要存取使用fmt=swf或fmt=swf3傳送的影像屬性。
seo-description: Flash應用程式網域。 Adobe Flash應用程式可能需要存取使用fmt=swf或fmt=swf3傳送的影像屬性。
seo-title: 受信任網域
solution: Experience Manager
title: 受信任網域
topic: Scene7 Image Serving - Image Rendering API
uuid: 1d056d68-b699-413c-897c-8612444735c5
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 受信任網域{#trusteddomains}

Flash應用程式網域。 Adobe Flash應用程式可能需要存取使用fmt=swf或fmt=swf3傳送的影像屬性。

swf必須註冊其信任的應用程式網域名稱，以明確授與存取權。

## 屬性 {#section-e7f95bbb749f441e83e90c2bc3d5a6e0}

包含以逗號分隔的Web域名清單的字串。 如果空白，則必須從與影像演算相同的網域提供應用程式，才能存取swf格式回應中的影像屬性。

## 預設 {#section-5c52ed3c7310488380f5a6f9540bf981}

繼承自( `default::TrustedDomains` 如果不存在)。

## 另請參閱 {#section-65d0846e41674882a4d0d56a8f6d524b}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
