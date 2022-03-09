---
title: AssetContextStateUpdate
description: 為與資產關聯的發佈上下文設定一組新的發佈狀態標誌。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: ecbadafc-e77d-4c7e-a3d5-31c2b2a9b2ea
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '63'
ht-degree: 6%

---

# AssetContextStateUpdate{#assetcontextstateupdate}

為與資產關聯的發佈上下文設定一組新的發佈狀態標誌。

**參數**

| 名稱 | 類型 | 說明 |
|---|---|---|
| 資產句柄 | `xsd:string` | 處理要更新的資產。 |
| contextStateUpdateArray | `types:ContextStateUpdateArray` | 您要更新的資產的發佈聯繫人狀態的陣列。 |
