---
description: saveToFile=的根路徑。 將以req=saveToFile產生的影像寫入的根資料夾相對路徑。
solution: Experience Manager
title: 儲存路徑
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6e2814b9-898f-4cf4-8e4f-aa972d554213
TQID: 'https://experienceleague.adobe.com/CXC5-22MiZRyIjwOgOcgpRGq6kVZSZ6S-EKq8N-k7ME'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 89
ht-degree: 3%

---

# 儲存路徑{#savepath}

saveToFile=的根路徑。 將以req=saveToFile產生的影像寫入的根資料夾相對路徑。

`SavePath`是文字字串值。

## 屬性 {#section-343d1371e966491c92854a8df14c3c50}

文字字串。 必須為空白或有效的相對資料夾路徑。 一律與使用`ImageServer::SaveDirectory`設定的絕對根路徑結合。

## 預設 {#section-ae751eea97654f399c6aaee3f3252cbb}

如果未定義，則繼承自`default::SavePath`。 如果解析的值為空白，則會停用儲存至檔案的功能。

## 另請參閱 {#section-b38b045bbf084ca5a4b24ea12c4877ae}

[req=saveToFile](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
