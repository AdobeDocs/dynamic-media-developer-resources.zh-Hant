---
description: 系統中資源和型別的使用者。
solution: Experience Manager
title: 使用者
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 5747f5bf-0175-4707-bfcb-1a9b97d7a24a
TQID: 'https://experienceleague.adobe.com/XM-2FjVie-j71W3Sc3-TypNJUFnz5AQuZZuGOx1fePs'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 70c478ebbe0b38d9e35c1bb26074a458c0197b2b
workflow-type: tm+mt
source-wordcount: 71
ht-degree: 9%

---

# [!DNL User]{#user}

系統中資源和型別的使用者。

語法

## 參數 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名稱 | 類型 | 說明 |
|---|---|---|
| userHandle | `xsd:string` | 使用者控制代碼。 |
| 名字 | `xsd:string` | 使用者名字。 |
| 姓氏 | `xsd:string` | 使用者姓氏。 |
| 電子郵件 | `xsd:string` | 電子郵件地址。 |
| defaultrole | `xsd:string` | 設定使用者在其所屬每個公司中的角色。 但是，使用者角色`IpsAmin`會覆寫其他使用者角色。 |
| isValid | `xsd:boolean` | 判斷使用者是否有效。 |
| 密碼過期 | `xsd:dateTime` | 設定密碼到期日。 |

