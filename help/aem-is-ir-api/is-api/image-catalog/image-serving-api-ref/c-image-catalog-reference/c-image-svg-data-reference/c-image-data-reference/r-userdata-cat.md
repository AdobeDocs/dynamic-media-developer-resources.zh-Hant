---
description: 用戶資料。 伺服器響應req=userdata將此欄位的內容返回給客戶端。
solution: Experience Manager
title: 用戶資料
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4994c91c-52d7-473d-88ee-f136c4193c40
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 3%

---

# 用戶資料{#userdata}

用戶資料。 伺服器響應req=userdata將此欄位的內容返回給客戶端。

## 屬性 {#section-06f2002b77d54a64be07f12fff54ad13}

文本字串值。 建議使用 [屬性資料](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-property-data.md) 格式 如果未使用屬性資料格式，則文本字串不得包含「=」字元。

縮放、旋轉和手冊查看器客戶端假定此欄位使用屬性資料格式。 這些客戶端使用此欄位進行查看器配置和自定義。 有關詳細資訊，請參閱查看器文檔。

此欄位參與文本字串本地化。 請參閱 [文本字串本地化](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) 的 *HTTP協定引用* 的雙曲餘切值。

## 預設 {#section-7ee879762130467199745f2abc662f1e}

無。

## 另請參閱 {#section-e07a022933b2461d9c37b1f188aa8fb5}

[req=userdata](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md) 。 [文本字串本地化](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)
