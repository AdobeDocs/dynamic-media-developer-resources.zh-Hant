---
title: pscan
description: 漸進式JPEG掃描。 漸進式JPEG顯示影像的方式，使其一開始會顯示整張模糊/低品質的像片。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1afd3a60-e0b6-47d1-b7e4-98a3145782a2
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 2%

---

# pscan{#pscan}

漸進式JPEG掃描。 漸進式JPEG顯示影像的方式，使其一開始會顯示整張模糊/低品質的像片。 隨著掃描過程繼續進行，影像的資料下載得越充分，掃描過程就越清晰。 此引數可讓您設定顯示整個影像所需的掃描次數（3、4或5）。

`pscan=auto|3|4|5`

每次掃描的實際速度取決於使用者系統與接收及解壓縮資料的電腦的傳輸速度。

`Auto` 會使用由獨立JPEG庫計算出的掃描設定，且視顏色模型而定。 下列專案的值 `3`， `4`， `5` 對應至將JPEG檔案儲存為pjpeg (漸進式JPEG)時，在Adobe Photoshop中找到的掃描設定。

如果 `pscan` 未設定，其預設為 `auto`.

## 屬性 {#section-e36aa3c63a974b969d9e4f43fe5a37ab}

要求屬性。 不論目前的圖層設定為何，皆會套用。 如果輸出格式不是漸進式JPEG，則忽略。

## 預設 {#section-01948f6cd7a2415091004cd7526436c7}

`pscan=auto`

## 範例 {#section-d51bc4d0e8a9473786f149cba9540506}

`http://localhost:8080/is/image/demo/bedroom.tif?wid=300&fmt=pjpeg&pscan=4`

## 另請參閱 {#section-2105c6441d2b42edb15c7abc4e20d7fc}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
