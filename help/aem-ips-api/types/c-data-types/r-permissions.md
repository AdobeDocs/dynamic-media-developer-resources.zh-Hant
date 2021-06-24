---
description: 管理依群組存取、修改、建立或刪除資產的權限。
solution: Experience Manager
title: 權限
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: 18e5f8f6-3cbe-4d36-b02a-5a3002e4498c
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '59'
ht-degree: 11%

---

# 權限{#permission}

管理依群組存取、修改、建立或刪除資產的權限。

語法

## 參數 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名稱 | 類型 | 說明 |
|---|---|---|
| `*`groupHandle`*` | `xsd:string` | 組句柄。 |
| `*`groupName`*` | `xsd:string` | 群組名稱. |
| `*`permissionType`*` | `xsd:string` | 權限類型的選擇。 |
| `*`isAllowed`*` | `xsd:boolean` | 判斷是否允許權限。 |
| `*`isOverride`*` | `xsd:boolean` | 確定權限是否覆蓋另一個權限。 |
