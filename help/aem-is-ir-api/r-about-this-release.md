---
description: 此發行版本（「影像提供6.6.1」和「影像轉譯6.6.1」）取代「影像提供6.5.3」和「影像轉譯6.5.3」。
solution: Experience Manager
title: 關於此版本
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f837191b-1151-4c29-8059-b4d3e09e304e
source-git-commit: 97fbf820590b53de5a1e6ce904e44d6b0ef9a214
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 1%

---

# 關於此版本{#about-this-release}

此發行版本（「影像提供6.6.1」和「影像轉譯6.6.1」）取代「影像提供6.5.3」和「影像轉譯6.5.3」。

## 已知問題和行為變更 {#section-9dbc05206187477f926a78e8108a34e1}

* 不再支援在資產ID中使用問號字元，即使該字元已進行URL編碼亦然。
* 動態橫幅 `/xfl/flash/` 不再支援要求，現在會傳回HTTP 404錯誤碼。
* W2P `/is/agm/` 不再支援要求。
* 有些錯誤訊息不再轉譯為瀏覽器。 因此，您需要檢閱要偵錯的追蹤記錄。

## 新功能 {#section-b1386e36cb4544ebb79766a06b16842d}

* 智慧型色票
* 智慧型裁切

## 錯誤修正 {#section-58dff74d56f64edeadf8f8b97b7a4161}

* 修正的問題： `\qc` RTF選項後面接著空格，導致要求無法轉譯。
