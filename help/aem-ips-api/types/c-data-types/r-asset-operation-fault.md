---
description: 包含批資產操作期間生成的有關警告或錯誤條件的資訊。 代碼和原因欄位對應於為等效非批處理操作而拋出的故障消息欄位。
solution: Experience Manager
title: AssetOperationFault
feature: Dynamic Media Classic,SDK/API，資產管理
role: Developer,Administrator
exl-id: c97fc35b-76f8-4ff7-a1ae-e5f9749f376c
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 7%

---

# AssetOperationFault{#assetoperationfault}

包含批資產操作期間生成的有關警告或錯誤條件的資訊。 代碼和原因欄位對應於為等效非批處理操作而拋出的故障消息欄位。

語法

## 參數 {#section-c906f052f43e4785ba46d92b514b0923}

| 名稱 | 類型 | 說明 |
|---|---|---|
| `*`assetHandle`*` | `xsd:string` | 失敗操作的資產句柄。 |
| `*`代碼`*` | `xsd:int` | 操作故障代碼。 |
| `*`原因`*` | `xsd:string` | 錯誤描述或原因。 |
