---
description: 包含有關批資產操作期間生成的警告或錯誤條件的資訊。 代碼和原因欄位對應於為對等非批處理操作而拋出的故障消息欄位。
seo-description: 包含有關批資產操作期間生成的警告或錯誤條件的資訊。 代碼和原因欄位對應於為對等非批處理操作而拋出的故障消息欄位。
seo-title: AssetOperationFault
solution: Experience Manager
title: AssetOperationFault
topic: Dynamic Media Image Production System API
uuid: fb6c5482-6e16-4561-927b-e4daeb7bdd7b
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '126'
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

