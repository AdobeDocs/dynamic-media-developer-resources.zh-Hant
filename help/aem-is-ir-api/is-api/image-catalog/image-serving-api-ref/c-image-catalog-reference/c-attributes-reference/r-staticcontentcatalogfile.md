---
description: 靜態內容目錄資料檔案路徑。 指定包含此目錄之靜態內容資料的檔案。
solution: Experience Manager
title: statictcontentcatalogfile
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ff6f0ad8-189f-4172-89cb-f138d2df8fe4
TQID: 'https://experienceleague.adobe.com/98uNzMz83z3lfa2d3LNixYKZzUWWE9zqrK1fnPo-JNA'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 116
ht-degree: 3%

---

# statictcontentcatalogfile{#staticcontentcatalogfile}

靜態內容目錄資料檔案路徑。 指定包含此目錄之靜態內容資料的檔案。

靜態內容目錄資料檔案會依指定的順序載入。 如果相同的`static::Id`值出現在多個記錄中（在相同或不同的目錄檔案中），則最後一個執行個體會優先。

## 屬性 {#section-3f8dc8d21fa84fbeb71db6ca1ecbdd8c}

一或多個文字字串值，以逗號分隔。 選擇性. 每個值都必須是絕對檔案路徑或相對於目錄資料夾的路徑。

## 預設 {#section-702edfbc00c54fc29e412a3ff99fef2b}

空白，表示此影像目錄不包含任何靜態內容資料。

## 另請參閱 {#section-13d78d475fff40e7a4edf9a9c73f3c15}

[目錄資料](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-catalog-data-fields/c-catalog-data-fields.md#concept-b19581028ec44f98b9f5943624403d29)
