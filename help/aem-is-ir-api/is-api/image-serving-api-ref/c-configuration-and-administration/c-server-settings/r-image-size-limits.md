---
description: 使用這些伺服器設定來設定影像大小限制。
solution: Experience Manager
title: 影像大小限制
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 75ec58ee-8c98-46cb-96b2-79d1c32e576f
TQID: 'https://experienceleague.adobe.com/-xOEUXOC5tk9b9miYQWTmC73EsZbSo9Zzn8AedEksEI'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 233
ht-degree: 0%

---

# 影像大小限制{#image-size-limits}

使用這些伺服器設定來設定影像大小限制。

## IS：：MaxMessageSize — 回應大小限制 {#section-bd942385d4d144cd904003695d72c85e}

限制影像伺服器可傳送至[!DNL Platform Server]的資料大小。 實際上，這樣會限制「影像伺服」可以透過HTTP (MB)傳回給使用者端的編碼/壓縮回應影像大小。

## IS：：MaxRenderRgnPixels — 輸出影像大小限制 {#section-868ceb9764dd42dfb133ffeb72f9d3fb}

限制影像伺服器可產生的影像大小（不包括儲存至檔案的影像）。 大於0的整數值（百萬畫素）。 如果轉譯作業超過大小限制，則會傳回錯誤。 預設值為16。

## IS：：MaxSavePixels — 儲存至檔案的大小限制 {#section-d1547c4afa88467080ab08356f775e06}

使用`req=saveToFile`命令限制影像伺服器寫入檔案的影像大小。 大於0的整數值（百萬畫素）。 如果檔案儲存作業超過該限制，則會傳回錯誤。 預設值為1億畫素。

## IS：：MaxNonDsfSize — 非PTIFF輸入影像的大小限制 {#section-50de28a7158a436393cce5da0d1e4d46}

允許影像伺服器開啟且非PTIFF的影像大小上限（以畫素為單位）。 嘗試存取大於此限制的非PTIFF影像時，「影像伺服」會傳回錯誤。

>[!NOTE]
>
>將此值設定得太高，可能會造成影像伺服器的記憶體不足，並造成失敗，包括當機。
