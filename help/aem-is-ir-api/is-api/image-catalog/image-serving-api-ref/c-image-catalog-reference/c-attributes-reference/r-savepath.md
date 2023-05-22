---
description: saveToFile=的根路徑。 應將使用req=saveToFile生成的影像寫入到的根資料夾的相對路徑。
solution: Experience Manager
title: 保存路徑
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6e2814b9-898f-4cf4-8e4f-aa972d554213
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 3%

---

# 保存路徑{#savepath}

saveToFile=的根路徑。 應將使用req=saveToFile生成的影像寫入到的根資料夾的相對路徑。

`SavePath` 是文本字串值。

## 屬性 {#section-343d1371e966491c92854a8df14c3c50}

文本字串。 必須為空或有效的相對資料夾路徑。 始終與配置為的絕對根路徑組合 `ImageServer::SaveDirectory`。

## 預設 {#section-ae751eea97654f399c6aaee3f3252cbb}

繼承自 `default::SavePath` 的子菜單。 如果解析值為空，則禁用保存到檔案。

## 另請參閱 {#section-b38b045bbf084ca5a4b24ea12c4877ae}

[req=saveToFile](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
