---
description: 層視圖屬性。
solution: Experience Manager
title: 層視圖資訊
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 25199c86-1df0-41af-b210-e7668a60295e
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '47'
ht-degree: 12%

---

# 層視圖資訊{#layerviewinfo}

層視圖屬性。

語法

## 參數 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名稱 | 類型 | 說明 |
|---|---|---|
| url | `xsd:string` | 表示模板的影像伺服器URL。 組合 `urlModifier` 和 `urlPostAp- plyModifier` 的子菜單。 |
| url修飾符 | `xsd:string` | 在請求或 `urlPostApplyModifier` 的雙曲餘切值。 |
| urlPostApplyModifier | `xsd:string` | 在以下時間後應用的影像服務協定命令 `urlModifier` 命令。 |
