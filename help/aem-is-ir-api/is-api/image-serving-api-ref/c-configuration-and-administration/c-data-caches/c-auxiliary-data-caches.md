---
description: 通過在嵌套/嵌入請求中指定cache=on，可快取由嵌套/嵌入影像服務和影像呈現請求產生的中間影像資料。 該資料以專有格式儲存在響應資料快取中。
solution: Experience Manager
title: 輔助資料快取
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 39906c86-fd9e-4961-a8ba-2ac44c4214a2
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 0%

---

# 輔助資料快取{#auxiliary-data-caches}

通過在嵌套/嵌入請求中指定cache=on，可快取由嵌套/嵌入影像服務和影像呈現請求產生的中間影像資料。 該資料以專有格式儲存在響應資料快取中。

從外部HTTP伺服器獲得的影像也儲存在響應資料快取中。 在生成快取條目之前，使用驗證實用程式自動驗證這些影像。

的 [!DNL Platform Server] 編譯影像目錄資料以便有效訪問。 此資料儲存在 `CS::CatalogCacheFolder`。
