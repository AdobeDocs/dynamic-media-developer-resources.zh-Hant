---
title: 資產操作故障
description: 包含有關批資產操作期間生成的警告或錯誤條件的資訊。 代碼欄位和原因欄位對應於為等效非批處理操作而拋出的故障消息欄位。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: c97fc35b-76f8-4ff7-a1ae-e5f9749f376c
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 7%

---

# 資產操作故障{#assetoperationfault}

包含有關批資產操作期間生成的警告或錯誤條件的資訊。 代碼欄位和原因欄位對應於為等效非批處理操作而拋出的故障消息欄位。

語法

## 參數 {#section-c906f052f43e4785ba46d92b514b0923}

| 名稱 | 類型 | 說明 |
|---|---|---|
| 資產句柄 | `xsd:string` | 失敗操作的資產句柄。 |
| 代碼 | `xsd:int` | 操作故障代碼。 |
| 原因 | `xsd:string` | 故障描述或原因。 |
