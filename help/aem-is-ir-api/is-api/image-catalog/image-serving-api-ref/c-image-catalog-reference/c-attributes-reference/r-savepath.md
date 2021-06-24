---
description: saveToFile=的根路徑。 根資料夾的相對路徑，應將以req=saveToFile生成的影像寫入到該根資料夾。
solution: Experience Manager
title: SavePath
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 6e2814b9-898f-4cf4-8e4f-aa972d554213
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 4%

---

# SavePath{#savepath}

saveToFile=的根路徑。 根資料夾的相對路徑，應將以req=saveToFile生成的影像寫入到該根資料夾。

`SavePath` 是文字字串值。

## 屬性 {#section-343d1371e966491c92854a8df14c3c50}

文字字串。 必須為空或有效的相對資料夾路徑。 始終與配置了`ImageServer::SaveDirectory`的絕對根路徑相結合。

## 預設 {#section-ae751eea97654f399c6aaee3f3252cbb}

若未定義，則繼承自`default::SavePath`。 如果解析的值為空，則會停用儲存至檔案。

## 另請參閱 {#section-b38b045bbf084ca5a4b24ea12c4877ae}

[req=saveToFile](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
