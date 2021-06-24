---
description: 漸進式JPEG掃描。 漸進式JPEG以這樣的方式顯示影像，使得它最初顯示整體的模糊/低質量照片。 隨著掃描通過繼續，隨著影像資料的更完整下載，會更清楚。 此參數可讓您設定整個影像要顯示所花費的掃描數（3、4或5）。
solution: Experience Manager
title: pscan
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 1afd3a60-e0b6-47d1-b7e4-98a3145782a2
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 2%

---

# pscan{#pscan}

漸進式JPEG掃描。 漸進式JPEG以這樣的方式顯示影像，使得它最初顯示整體的模糊/低質量照片。 隨著掃描通過繼續，隨著影像資料的更完整下載，會更清楚。 此參數可讓您設定整個影像要顯示所花費的掃描數（3、4或5）。

`pscan=auto|3|4|5`

每個掃描的實際速度取決於用戶系統和接收和解壓縮資料的電腦的傳輸速度。

`Auto` 使用由獨立JPEG庫計算並取決於顏色模型的掃描設定。`3`、`4`、`5`的值對應於將JPEG檔案另存為pjpeg（漸進式JPEG）時在Adobe Photoshop中找到的「掃描」設定。

如果未設定`pscan`，則預設值為`auto`。

## 屬性 {#section-e36aa3c63a974b969d9e4f43fe5a37ab}

要求屬性。 無論目前的層設定為何，都適用。 如果輸出格式不是漸進式JPEG，則忽略。

## 預設 {#section-01948f6cd7a2415091004cd7526436c7}

`pscan=auto`

## 範例 {#section-d51bc4d0e8a9473786f149cba9540506}

`http://localhost:8080/is/image/demo/bedroom.tif?wid=300&fmt=pjpeg&pscan=4`

## 另請參閱 {#section-2105c6441d2b42edb15c7abc4e20d7fc}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
