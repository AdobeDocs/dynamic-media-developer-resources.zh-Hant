---
description: 逐行JPEG掃描。 逐行JPEG顯示影像，其方式是最初顯示整張模糊/低質量照片。 隨著掃描過程的繼續，隨著影像資料的下載更加完全，掃描過程變得更加清晰。 通過此參數，可以設定掃描（3、4或5）以顯示整個影像的次數。
solution: Experience Manager
title: 掃描
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1afd3a60-e0b6-47d1-b7e4-98a3145782a2
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 1%

---

# 掃描{#pscan}

逐行JPEG掃描。 逐行JPEG顯示影像，其方式是最初顯示整張模糊/低質量照片。 隨著掃描過程的繼續，隨著影像資料的下載更加完全，掃描過程變得更加清晰。 通過此參數，可以設定掃描（3、4或5）以顯示整個影像的次數。

`pscan=auto|3|4|5`

每個掃描的實際速度取決於用戶系統和接收和解壓縮資料的電腦的傳輸速度。

`Auto` 使用由獨立JPEG庫計算並取決於顏色模型的掃描設定。 值 `3`。 `4`。 `5` 與將JPEG檔案另存為pjpeg(漸進JPEG)時在Adobe Photoshop找到的掃描設定相對應。

如果 `pscan` 未設定，它預設為 `auto`。

## 屬性 {#section-e36aa3c63a974b969d9e4f43fe5a37ab}

請求屬性。 無論當前圖層設定如何都適用。 如果輸出格式不是累進JPEG，則忽略。

## 預設 {#section-01948f6cd7a2415091004cd7526436c7}

`pscan=auto`

## 範例 {#section-d51bc4d0e8a9473786f149cba9540506}

`http://localhost:8080/is/image/demo/bedroom.tif?wid=300&fmt=pjpeg&pscan=4`

## 另請參閱 {#section-2105c6441d2b42edb15c7abc4e20d7fc}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
