---
description: 借由在巢狀/內嵌請求中指定cache=on ，可快取由巢狀/內嵌影像伺服與影像呈現請求產生的中間影像資料。 此資料會以專屬格式儲存在回應資料快取中。
solution: Experience Manager
title: 輔助資料快取
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 39906c86-fd9e-4961-a8ba-2ac44c4214a2
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 0%

---

# 輔助資料快取{#auxiliary-data-caches}

借由在巢狀/內嵌請求中指定cache=on ，可快取由巢狀/內嵌影像伺服與影像呈現請求產生的中間影像資料。 此資料會以專屬格式儲存在回應資料快取中。

從外部HTTP伺服器獲得的影像也儲存在響應資料快取中。 在生成快取條目之前，使用驗證實用程式自動驗證這些影像。

Platform Server會編譯影像目錄資料，以有效存取。 此資料儲存在`CS::CatalogCacheFolder`中。
