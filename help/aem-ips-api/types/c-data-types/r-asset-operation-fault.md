---
title: AssetOperationFault
description: 包含批資產操作期間生成的有關警告或錯誤條件的資訊。 代碼和原因欄位對應於為等效非批處理操作而拋出的故障消息欄位。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: c97fc35b-76f8-4ff7-a1ae-e5f9749f376c
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 7%

---

# [!DNL AssetOperationFault]{#assetoperationfault}

包含批資產操作期間生成的有關警告或錯誤條件的資訊。 代碼和原因欄位對應於為等效非批處理操作而拋出的故障消息欄位。

語法

## 參數 {#section-c906f052f43e4785ba46d92b514b0923}

| 名稱 | 類型 | 說明 |
|---|---|---|
| assetHandle | `xsd:string` | 失敗操作的資產句柄。 |
| 代碼 | `xsd:int` | 操作故障代碼。 |
| 原因 | `xsd:string` | 錯誤描述或原因。 |
