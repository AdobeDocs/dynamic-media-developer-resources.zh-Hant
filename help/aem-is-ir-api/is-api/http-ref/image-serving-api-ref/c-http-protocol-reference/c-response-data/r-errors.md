---
description: 如果請求無法成功完成，伺服器將返回錯誤映像或HTTP響應狀態（200以外），並返回錯誤消息。
solution: Experience Manager
title: 錯誤
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9314782f-703b-4e9c-a026-62970d1c752f
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 2%

---

# 錯誤{#errors}

如果請求無法成功完成，伺服器將返回錯誤映像或HTTP響應狀態（200以外），並返回錯誤消息。

響應狀態值取決於錯誤類型；對於最常見的錯誤，它是「403」。 非映像請求類型的錯誤響應符合使用指定的格式 `req=`。 （此時可能未一致實施。）

錯誤消息中包含的詳細資訊量可配置為 `attribute::ErrorDetail`。

## 錯誤影像 {#section-92e9b20b2507433daa96923abc95f777}

映像服務可配置為返回呈現到映像中的錯誤消息。

請參閱 [屬性：:ErrorImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c) 影像目錄引用中獲取詳細資訊。

如果成功生成錯誤影像，則HTTP響應狀態為200。 如果處理錯誤影像時出錯，則標準HTTP錯誤響應和文本消息將返回給客戶端。

## 預設影像 {#section-66bf25fe6b434081bfae96d38d9be25e}

映像服務可配置為用預設映像替換缺失的映像。 可以使用 `attribute::DefaultImage` 或 `defaultImage=` 的子菜單。

## 另請參閱 {#section-e261d7f224ca4546bb64bf8cb909db08}

[屬性：:ErrorDetail](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errordetail.md#reference-4987c8cddcba4c88960170e49cafc561) 。 [屬性：:ErrorImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c)。 [屬性：:DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433)。 [defaultImage=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-defaultimage.md#reference-209aa6ce830f490483412eb26af67fd2)
