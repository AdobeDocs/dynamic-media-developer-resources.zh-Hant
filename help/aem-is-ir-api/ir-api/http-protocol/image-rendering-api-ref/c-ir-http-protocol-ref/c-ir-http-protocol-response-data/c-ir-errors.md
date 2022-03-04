---
title: 錯誤
description: 如果請求無法成功完成，伺服器將返回錯誤映像或HTTP響應狀態（200以外），並返回錯誤消息。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e45e3968-3659-470b-a88a-fe7ba73d8207
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 2%

---

# 錯誤{#errors}

如果請求無法成功完成，伺服器將返回錯誤映像或HTTP響應狀態（200以外），並返回錯誤消息。

響應狀態值取決於錯誤類型；對於最常見的錯誤，它是「403」。 非映像請求類型的錯誤響應符合使用指定的格式 `req=`。 （當前可能未一致實施。）

錯誤消息中包含的詳細資訊量可配置為 `attribute::ErrorDetail`。

**錯誤影像**

映像服務可配置為返回呈現到映像中的錯誤消息。 請參閱 `attribute::ErrorImage` 影像目錄引用中獲取詳細資訊。 如果成功生成錯誤影像，則HTTP響應狀態為200。 如果處理錯誤影像時出錯，則標準HTTP錯誤響應和文本消息將返回給客戶端。

**另請參閱**

[屬性：:ErrorDetail](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errordetail.md#reference-123b56eed6cf49cea6e0490672b7c53b) 。 [屬性：:ErrorImage](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0)
