---
description: 瀏覽器中點選動作的目標定義。
solution: Experience Manager
title: ImageMapDefinition
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 58478e7c-e3a1-4dd5-8ff9-e9752301b93c
TQID: 'https://experienceleague.adobe.com/x27LpaNACQ5k-n09O-9Bhw7aecAjWQ6wNkLt8XewVXs'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 71
ht-degree: 12%

---

# [!DNL ImageMapDefinition]{#imagemapdefinition}

瀏覽器中點選動作的目標定義。

語法

## 參數 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名稱 | 類型 | 說明 |
|---|---|---|
| name | `xsd:string` | 影像地圖定義的名稱。 |
| shapetype | `xsd:string` | 區域形狀值之一。 |
| 區域 | `xsd:string` | 影像地圖座標。 格式是以HTML `<area>`標籤屬性為基礎。 |
| 操作 | `xsd:string` | 要包含在HTML `<area>`標籤中的其他屬性，包括`href` URL。 |
| 啟動 | `xsd:boolean` | 如果影像地圖已啟用，則為True。 |
