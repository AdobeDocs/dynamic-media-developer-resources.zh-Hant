---
description: 如果請求無法成功完成，伺服器會傳回錯誤影像或200以外的HTTP回應狀態，並顯示錯誤訊息。
seo-description: 如果請求無法成功完成，伺服器會傳回錯誤影像或200以外的HTTP回應狀態，並顯示錯誤訊息。
seo-title: 錯誤
solution: Experience Manager
title: 錯誤
topic: Scene7 Image Serving - Image Rendering API
uuid: 5984fa9e-63c8-426b-be5f-48f66fc918c3
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 2%

---


# 錯誤{#errors}

如果請求無法成功完成，伺服器會傳回錯誤影像或200以外的HTTP回應狀態，並顯示錯誤訊息。

響應狀態值取決於錯誤的類型；對於最常見的錯誤，它是&#39;403&#39;。 非影像請求類型的錯誤回應符合使用`req=`指定的格式。 （目前可能不會一致地實施。）

錯誤消息中包含的詳細資訊量可配置為`attribute::ErrorDetail`。

**錯誤影像**

「影像伺服」可設定為傳回演算為影像的錯誤訊息。 如需詳細資訊，請參閱影像目錄參考中的`attribute::ErrorImage`。 如果成功產生錯誤影像，HTTP回應狀態為200。 如果在處理錯誤影像時發生錯誤，則會傳回標準HTTP錯誤回應和文字訊息給用戶端。

**另請參閱**

[attribute::ErrorDetail](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errordetail.md#reference-123b56eed6cf49cea6e0490672b7c53b) ,  [attribute::ErrorImage](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0)
