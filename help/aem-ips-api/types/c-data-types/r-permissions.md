---
description: 管理依群組存取、修改、建立或刪除資產的許可權。
solution: Experience Manager
title: 許可權
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 18e5f8f6-3cbe-4d36-b02a-5a3002e4498c
TQID: 'https://experienceleague.adobe.com/BfB4MGiJFqPkJqL26YSmrhd52KfxhVX5TC-LHxEhevo'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 53
ht-degree: 9%

---

# [!DNL Permission]{#permission}

管理依群組存取、修改、建立或刪除資產的許可權。

語法

## 參數 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名稱 | 類型 | 說明 |
|---|---|---|
| groupHandle | `xsd:string` | 群組控制代碼。 |
| groupName | `xsd:string` | 群組名稱。 |
| permissionType | `xsd:string` | 許可權型別的選擇。 |
| isAllowed | `xsd:boolean` | 決定是否允許許可權。 |
| isOverride | `xsd:boolean` | 決定許可權是否覆寫其他許可權。 |
