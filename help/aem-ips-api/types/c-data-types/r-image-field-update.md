---
description: 更新與影像資產關聯的影像欄位。
solution: Experience Manager
title: ImageFieldUpdate
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 82bc016b-8a2b-4811-a0b4-1e2a93add3b6
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '56'
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
