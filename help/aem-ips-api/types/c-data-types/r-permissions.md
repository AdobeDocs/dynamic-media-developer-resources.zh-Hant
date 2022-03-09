---
description: 管理按組訪問、修改、建立或刪除資產的權限。
solution: Experience Manager
title: 權限
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 18e5f8f6-3cbe-4d36-b02a-5a3002e4498c
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '54'
ht-degree: 12%

---

# 權限{#permission}

管理按組訪問、修改、建立或刪除資產的權限。

語法

## 參數 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名稱 | 類型 | 說明 |
|---|---|---|
| 組句柄 | `xsd:string` | 組句柄。 |
| 組名 | `xsd:string` | 群組名稱. |
| 權限類型 | `xsd:string` | 權限類型的選擇。 |
| 允許 | `xsd:boolean` | 確定是否允許權限。 |
| 是覆蓋 | `xsd:boolean` | 確定權限是否覆蓋其他權限。 |
