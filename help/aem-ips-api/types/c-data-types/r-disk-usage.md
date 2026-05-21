---
description: 資產或資料夾的磁碟空間統計資料。
solution: Experience Manager
title: 磁碟使用情況
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: a3c4c1cd-0fcc-4e7a-a4aa-884d0ce2f208
TQID: 'https://experienceleague.adobe.com/Md0oAgpJDqSrn1JRZsebpaZKeXIAoLcgkC5KPaHad5s'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 50
ht-degree: 10%

---

# [!DNL DiskUsage]{#diskusage}

資產或資料夾的磁碟空間統計資料。

語法

## 參數 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名稱 | 類型 | 說明 |
|---|---|---|
| companyHandle | `xsd:string` | 公司控制代碼。 |
| companyName | `xsd:string` | 公司名稱。 |
| imageCount | `xsd:int` | 儲存的影像數。 |
| 磁碟空間使用量 | `xsd:long` | 檔案端總計（以KB為單位）。 |
| lastModified | `xsd:dateTime` | 上次修改`DiskUsage`型別的日期、時間和時區。 |
