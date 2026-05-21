---
description: 更新與影像資產關聯的影像欄位。
solution: Experience Manager
title: ImageFieldUpdate
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 82bc016b-8a2b-4811-a0b4-1e2a93add3b6
TQID: 'https://experienceleague.adobe.com/IsOZvDzvJTa0KJfUkYblEln9Qrx7nQm79FEEbnFVjiw'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 56
ht-degree: 8%

---

# [!DNL ImageFieldUpdate]{#imagefieldupdate}

更新與影像資產關聯的影像欄位。

語法

## 參數 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名稱 | 類型 | 說明 |
|---|---|---|
| assetHandle | `xsd:string` | 資產控制代碼。 |
| [!DNL resolution] | `xsd:double` | 影像解析度，以畫素/英吋為單位。 |
| [!DNL anchorX] | `xsd:int` | X軸影像錨點。 |
| [!DNL anchorY] | `xsd:int` | Y軸影像錨點。 |
| [!DNL userData] | `xsd:string` | `userData`中繼資料欄位的值，此欄位已發佈至影像伺服使用者資料目錄欄位。 |
