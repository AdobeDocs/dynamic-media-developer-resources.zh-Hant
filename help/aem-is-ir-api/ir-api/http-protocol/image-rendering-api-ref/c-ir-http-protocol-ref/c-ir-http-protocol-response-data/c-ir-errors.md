---
description: 如果無法成功完成請求，伺服器將返回錯誤影像或200以外的HTTP響應狀態，並返回錯誤消息。
solution: Experience Manager
title: 錯誤
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: e45e3968-3659-470b-a88a-fe7ba73d8207
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 2%

---

# 錯誤{#errors}

如果無法成功完成請求，伺服器將返回錯誤影像或200以外的HTTP響應狀態，並返回錯誤消息。

回應狀態值取決於錯誤的類型；對於大多數常見錯誤，它為「403」。 非影像要求類型的錯誤回應符合使用`req=`指定的格式。 （目前可能無法一致地實作。）

錯誤消息中包含的詳細資訊量可以使用`attribute::ErrorDetail`配置。

**錯誤影像**

可以配置「影像服務」以返回呈現到影像中的錯誤消息。 如需詳細資訊，請參閱影像目錄參考中的`attribute::ErrorImage` 。 如果成功產生錯誤影像，HTTP回應狀態為200。 如果在處理錯誤影像時發生錯誤，則會將標準HTTP錯誤回應和文字訊息傳回給用戶端。

**另請參閱**

[屬性：:ErrorDetail](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errordetail.md#reference-123b56eed6cf49cea6e0490672b7c53b) ，屬 [性：:ErrorImage](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0)
