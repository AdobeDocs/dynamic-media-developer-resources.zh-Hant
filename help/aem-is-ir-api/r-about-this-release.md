---
description: 此發行版本（「影像提供6.6.1」和「影像轉譯6.6.1」）取代「影像提供6.5.3」和「影像轉譯6.5.3」。
solution: Experience Manager
title: 關於此版本
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f837191b-1151-4c29-8059-b4d3e09e304e
TQID: 'https://experienceleague.adobe.com/Mv84kHB7jsBYAvY1j--l8Ly5VZtKwFq-SsNdz2TIQOE'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 130
ht-degree: 1%

---

# 關於此版本{#about-this-release}

此發行版本（「影像提供6.6.1」和「影像轉譯6.6.1」）取代「影像提供6.5.3」和「影像轉譯6.5.3」。

## 已知問題和行為變更 {#section-9dbc05206187477f926a78e8108a34e1}

* 不再支援在資產ID中使用問號字元，即使該字元已進行URL編碼亦然。
* 不再支援動態橫幅`/xfl/flash/`要求，現在會傳回HTTP 404錯誤碼。
* 不再支援W2P `/is/agm/`要求。
* 有些錯誤訊息不再轉譯為瀏覽器。 因此，您需要檢閱要偵錯的追蹤記錄。

## 新功能 {#section-b1386e36cb4544ebb79766a06b16842d}

* 智慧型色票
* 智慧型裁切

## 錯誤修正 {#section-58dff74d56f64edeadf8f8b97b7a4161}

* 修正`\qc` RTF選項後面接著空格導致要求無法轉譯的問題。
