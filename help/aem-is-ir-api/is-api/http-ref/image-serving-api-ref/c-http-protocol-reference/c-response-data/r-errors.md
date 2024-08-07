---
description: 如果要求無法成功完成，伺服器會傳回錯誤影像或200以外的HTTP回應狀態以及錯誤訊息。
solution: Experience Manager
title: 錯誤
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9314782f-703b-4e9c-a026-62970d1c752f
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 1%

---

# 錯誤{#errors}

如果要求無法成功完成，伺服器會傳回錯誤影像或200以外的HTTP回應狀態以及錯誤訊息。

回應狀態值取決於錯誤型別；對於最常見的錯誤，則為「403」。 非影像要求型別的錯誤回應符合`req=`所指定的格式。 （目前可能無法一致地實作。）

錯誤訊息中包含的詳細資訊量可使用`attribute::ErrorDetail`設定。

## 錯誤影像 {#section-92e9b20b2507433daa96923abc95f777}

影像伺服可設定為傳回演算為影像的錯誤訊息。

如需詳細資訊，請參閱影像目錄參考中的[attribute：：ErrorImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c)。

如果成功產生錯誤影像，HTTP回應狀態為200。 如果在處理錯誤影像時發生錯誤，則會將標準HTTP錯誤回應和文字訊息傳回使用者端。

## 預設影像 {#section-66bf25fe6b434081bfae96d38d9be25e}

「影像伺服」可設定為以預設影像取代遺失的影像。 可以使用`attribute::DefaultImage`或`defaultImage=`命令指定預設影像。

## 另請參閱 {#section-e261d7f224ca4546bb64bf8cb909db08}

[attribute：：ErrorDetail](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errordetail.md#reference-4987c8cddcba4c88960170e49cafc561) ， [attribute：：ErrorImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c)， [attribute：：DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433)， [defaultImage=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-defaultimage.md#reference-209aa6ce830f490483412eb26af67fd2)
