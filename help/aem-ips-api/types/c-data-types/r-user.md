---
description: 系統中資源和類型的用戶。
solution: Experience Manager
title: 使用者
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 5747f5bf-0175-4707-bfcb-1a9b97d7a24a
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 11%

---

# 使用者{#user}

系統中資源和類型的用戶。

語法

## 參數 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名稱 | 類型 | 說明 |
|---|---|---|
| userHandle | `xsd:string` | 用戶句柄。 |
| 名字 | `xsd:string` | 用戶名。 |
| 姓氏 | `xsd:string` | 用戶姓。 |
| 電子郵件 | `xsd:string` | 電子郵件地址。 |
| 預設角色 | `xsd:string` | 設定用戶所屬每個公司中用戶的角色。 但是，用戶角色 `IpsAmin` 覆蓋其他用戶角色。 |
| 有效 | `xsd:boolean` | 確定用戶是否有效。 |
| 密碼過期 | `xsd:dateTime` | 設定密碼到期日期。 |
