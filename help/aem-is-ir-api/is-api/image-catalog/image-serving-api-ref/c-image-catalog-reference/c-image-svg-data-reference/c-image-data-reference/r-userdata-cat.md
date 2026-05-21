---
description: 使用者資料。 伺服器會將此欄位的內容傳回給使用者端，以回應req=userdata。
solution: Experience Manager
title: 使用者資料
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4994c91c-52d7-473d-88ee-f136c4193c40
TQID: 'https://experienceleague.adobe.com/9jhCw--mmCQ1-j1uNGFmfTEcnkNzxbKfXJtve5GugdA'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 123
ht-degree: 3%

---

# 使用者資料{#userdata}

使用者資料。 伺服器會將此欄位的內容傳回給使用者端，以回應req=userdata。

## 屬性 {#section-06f2002b77d54a64be07f12fff54ad13}

文字字串值。 建議使用[屬性資料](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-property-data.md)格式。 若未使用屬性資料格式，文字字串不得包含&#39;=&#39;字元。

縮放、迴轉和小冊子檢視器使用者端會假設此欄位使用屬性資料格式。 這些使用者端使用此欄位來設定檢視器並自訂。 如需詳細資訊，請參閱檢視器檔案。

此欄位參與文字字串本地化。 如需詳細資訊，請參閱&#x200B;*HTTP通訊協定參考*&#x200B;中的[文字字串本地化](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)。

## 預設 {#section-7ee879762130467199745f2abc662f1e}

無。

## 另請參閱 {#section-e07a022933b2461d9c37b1f188aa8fb5}

[req=userdata](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md) ， [文字字串本地化](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)
