---
description: 為與資產相關聯的發佈內容設定一組新的發佈狀態標幟。
solution: Experience Manager
title: AssetContextStateUpdate
feature: Dynamic Media Classic,SDK/API，資產管理
role: Developer,Administrator
exl-id: ecbadafc-e77d-4c7e-a3d5-31c2b2a9b2ea
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 5%

---

# AssetContextStateUpdate{#assetcontextstateupdate}

為與資產相關聯的發佈內容設定一組新的發佈狀態標幟。

**參數**

| 名稱 | 類型 | 說明 |
|---|---|---|
| `*`assetHandle`*` | `xsd:string` | 處理您要更新的資產。 |
| `*`contextStateUpdateArray`*` | `types:ContextStateUpdateArray` | 您要更新之資產的發佈連絡狀態陣列。 |
