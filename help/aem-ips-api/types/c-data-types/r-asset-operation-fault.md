---
description: 包含有關批資產操作期間生成的警告或錯誤條件的資訊。 代碼和原因欄位對應於為對等非批處理操作而拋出的故障消息欄位。
seo-description: 包含有關批資產操作期間生成的警告或錯誤條件的資訊。 代碼和原因欄位對應於為對等非批處理操作而拋出的故障消息欄位。
seo-title: AssetOperationFault
solution: Experience Manager
title: AssetOperationFault
uuid: fb6c5482-6e16-4561-927b-e4daeb7bdd7b
feature: Dynamic Media經典，SDK/API，資產管理
role: 開發人員、管理員
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 5%

---


# AssetOperationFault{#assetoperationfault}

包含有關批資產操作期間生成的警告或錯誤條件的資訊。 代碼和原因欄位對應於為對等非批處理操作而拋出的故障消息欄位。

語法

## 參數 {#section-c906f052f43e4785ba46d92b514b0923}

| 名稱 | 類型 | 說明 |
|---|---|---|
| `*`assetHandle`*` | `xsd:string` | 失敗操作的資產句柄。 |
| `*`代碼`*` | `xsd:int` | 操作故障代碼。 |
| `*`原因`*` | `xsd:string` | 錯誤描述或原因。 |

