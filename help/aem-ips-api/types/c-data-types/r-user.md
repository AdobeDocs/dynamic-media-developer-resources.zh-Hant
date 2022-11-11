---
description: 系統中資源和類型的用戶。
solution: Experience Manager
title: 使用者
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 5747f5bf-0175-4707-bfcb-1a9b97d7a24a
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 9%

---

# [!DNL User]{#user}

系統中資源和類型的用戶。

語法

## 參數 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名稱 | 類型 | 說明 |
|---|---|---|
| userHandle | `xsd:string` | 用戶句柄。 |
| firstName | `xsd:string` | 用戶名。 |
| lastName | `xsd:string` | 用戶名。 |
| 電子郵件 | `xsd:string` | 電子郵件地址。 |
| defaultRole | `xsd:string` | 設定使用者所屬每個公司中的角色。 不過，使用者角色 `IpsAmin` 會覆寫其他使用者角色。 |
| isValid | `xsd:boolean` | 確定用戶是否有效。 |
| passwordExpires | `xsd:dateTime` | 設定密碼到期日期。 |
