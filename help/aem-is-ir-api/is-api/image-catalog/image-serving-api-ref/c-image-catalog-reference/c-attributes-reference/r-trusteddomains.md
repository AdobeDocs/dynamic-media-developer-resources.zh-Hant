---
description: Flash應用程式網域。 Adobe Flash應用程式可能需要存取以fmt=swf或fmt=swf3傳送之影像的屬性。
solution: Experience Manager
title: TrustedDomain
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 925ac9d1-203c-4814-a701-71060bf47c20
TQID: 'https://experienceleague.adobe.com/xGn-usdBOB3NjRaffq6w0SJDlDerpeQJHGhKej-L3Cw'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 107
ht-degree: 2%

---

# TrustedDomain{#trusteddomains}

Flash應用程式網域。 Adobe Flash應用程式可能需要存取以fmt=swf或fmt=swf3傳送之影像的屬性。

SWF必須透過註冊信任的應用程式網域名稱來明確授與存取權。

## 屬性 {#section-e7f95bbb749f441e83e90c2bc3d5a6e0}

包含以逗號分隔的網路網域名稱清單的字串。 如果空白，則必須從與影像演算相同的網域提供應用程式，才能存取SWF格式回應中的影像屬性。

## 預設 {#section-5c52ed3c7310488380f5a6f9540bf981}

從`default::TrustedDomains`繼承（如果不存在）。

## 另請參閱 {#section-65d0846e41674882a4d0d56a8f6d524b}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
