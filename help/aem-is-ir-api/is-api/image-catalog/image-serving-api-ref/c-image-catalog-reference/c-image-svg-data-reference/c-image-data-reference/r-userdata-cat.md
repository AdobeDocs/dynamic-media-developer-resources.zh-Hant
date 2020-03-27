---
description: 使用者資料. 伺服器會回應req=userdata，將此欄位的內容傳回給用戶端。
seo-description: 使用者資料. 伺服器會回應req=userdata，將此欄位的內容傳回給用戶端。
seo-title: 使用者資料
solution: Experience Manager
title: 使用者資料
topic: Scene7 Image Serving - Image Rendering API
uuid: cadc9f3c-c0ca-4c88-bc8a-97c28b439b01
translation-type: tm+mt
source-git-commit: b4331c6f033903ec64f168da0b739927c6066710

---


# 使用者資料{#userdata}

使用者資料. 伺服器會回應req=userdata，將此欄位的內容傳回給用戶端。

## 屬性 {#section-06f2002b77d54a64be07f12fff54ad13}

文字字串值。 建議使用屬性資 [料格式](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-property-data.md) 。 如果未使用屬性資料格式，文字字串不得包含&#39;=&#39;字元。

縮放、回轉和手冊檢視器用戶端會假設此欄位使用屬性資料格式。 這些用戶端使用此欄位進行檢視器設定和自訂。 如需詳細資訊，請參閱檢視器檔案。

此欄位參與文字字串本地化。 如需詳細 [資訊，請參閱](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)*HTTP通訊協定參考中的文字字串本地化* 。

## 預設 {#section-7ee879762130467199745f2abc662f1e}

無。

## 另請參閱 {#section-e07a022933b2461d9c37b1f188aa8fb5}

[req=userdata](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md) ，文字字 [串本地化](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)
