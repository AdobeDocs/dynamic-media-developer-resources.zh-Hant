---
description: saveToFile=的根路徑。 以req=saveToFile生成的映像應寫入到的根資料夾的相對路徑。
solution: Experience Manager
title: SavePath
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 4%

---


# SavePath{#savepath}

saveToFile=的根路徑。 以req=saveToFile生成的映像應寫入到的根資料夾的相對路徑。

`SavePath` 是文字字串值。

## 屬性 {#section-343d1371e966491c92854a8df14c3c50}

文字字串。 必須為空或有效的相對資料夾路徑。 始終與配置有`ImageServer::SaveDirectory`的絕對根路徑相結合。

## 預設 {#section-ae751eea97654f399c6aaee3f3252cbb}

如果未定義，則繼承自`default::SavePath`。 如果解析的值為空，則會禁用保存到檔案。

## 另請參閱 {#section-b38b045bbf084ca5a4b24ea12c4877ae}

[req=saveToFile](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
