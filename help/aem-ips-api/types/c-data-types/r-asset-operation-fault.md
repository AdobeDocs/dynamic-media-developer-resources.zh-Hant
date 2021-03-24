---
description: 包含有關批資產操作期間生成的警告或錯誤條件的資訊。 代碼和原因欄位對應於為對等非批處理操作而拋出的故障消息欄位。
solution: Experience Manager
title: AssetOperationFault
feature: Dynamic Media經典，SDK/API，資產管理
role: 開發人員、管理員
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 7%

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

