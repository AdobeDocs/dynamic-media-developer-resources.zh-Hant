---
description: 系統中資源和類型的用戶。
solution: Experience Manager
title: 使用者
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 10%

---


# 使用者{#user}

系統中資源和類型的用戶。

語法

## 參數 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名稱 | 類型 | 說明 |
|---|---|---|
| `*`userHandle`*` | `xsd:string` | 使用者控制代碼。 |
| `*`firstName`*` | `xsd:string` | 用戶名。 |
| `*`lastName`*` | `xsd:string` | 用戶名。 |
| `*`電子郵件`*` | `xsd:string` | 電子郵件地址。 |
| `*`defaultRole`*` | `xsd:string` | 為用戶所屬的每個公司設定角色。 但是，用戶角色`IpsAmin`會覆蓋其他用戶角色。 |
| `*`isValid`*` | `xsd:boolean` | 判斷使用者是否有效。 |
| `*`passwordExpires`*` | `xsd:dateTime` | 設定密碼到期日。 |

