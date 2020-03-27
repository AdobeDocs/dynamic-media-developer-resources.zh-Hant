---
description: 通過在嵌套／嵌入請求中指定cache=on，可快取由嵌套／嵌入的影像服務和影像渲染請求產生的中間影像資料。 該資料以專有格式儲存在響應資料快取中。
seo-description: 通過在嵌套／嵌入請求中指定cache=on，可快取由嵌套／嵌入的影像服務和影像渲染請求產生的中間影像資料。 該資料以專有格式儲存在響應資料快取中。
seo-title: 輔助資料快取
solution: Experience Manager
title: 輔助資料快取
topic: Scene7 Image Serving - Image Rendering API
uuid: 10ce998e-e300-4d24-9d92-a8693dade327
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 輔助資料快取{#auxiliary-data-caches}

通過在嵌套／嵌入請求中指定cache=on，可快取由嵌套／嵌入的影像服務和影像渲染請求產生的中間影像資料。 該資料以專有格式儲存在響應資料快取中。

從外部HTTP伺服器獲得的影像也儲存在響應資料快取中。 在生成快取條目之前，使用驗證實用程式自動驗證這種影像。

平台伺服器會編譯影像目錄資料，以有效存取。 此資料儲存於 `CS::CatalogCacheFolder`。
