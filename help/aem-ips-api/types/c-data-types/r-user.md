---
description: 系統中資源和類型的用戶。
solution: Experience Manager
title: 使用者
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: 5747f5bf-0175-4707-bfcb-1a9b97d7a24a
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '77'
ht-degree: 10%

---

# 使用者{#user}

系統中資源和類型的用戶。

語法

## 參數 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名稱 | 類型 | 說明 |
|---|---|---|
| `*`userHandle`*` | `xsd:string` | 用戶句柄。 |
| `*`firstName`*` | `xsd:string` | 用戶名。 |
| `*`lastName`*` | `xsd:string` | 用戶名。 |
| `*`電子郵件`*` | `xsd:string` | 電子郵件地址。 |
| `*`defaultRole`*` | `xsd:string` | 設定使用者所屬每個公司中的角色。 但是，用戶角色`IpsAmin`將覆蓋其他用戶角色。 |
| `*`isValid`*` | `xsd:boolean` | 確定用戶是否有效。 |
| `*`passwordExpires`*` | `xsd:dateTime` | 設定密碼到期日期。 |
