---
description: 管理依群組存取、修改、建立或刪除資產的權利。
seo-description: 管理依群組存取、修改、建立或刪除資產的權利。
seo-title: 權限
solution: Experience Manager
title: 權限
topic: Dynamic Media Image Production System API
uuid: 3b3580d3-e5bc-42bf-bfbe-ab0ec2dea574
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '66'
ht-degree: 10%

---


# 權限{#permission}

管理依群組存取、修改、建立或刪除資產的權利。

語法

## 參數 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名稱 | 類型 | 說明 |
|---|---|---|
| `*`groupHandle`*` | `xsd:string` | 群組控制代碼。 |
| `*`groupName`*` | `xsd:string` | 群組名稱. |
| `*`permissionType`*` | `xsd:string` | 權限類型的選擇。 |
| `*`isAllowed`*` | `xsd:boolean` | 確定是否允許該權限。 |
| `*`isOverride`*` | `xsd:boolean` | 確定權限是否覆蓋另一個權限。 |

