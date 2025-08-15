---
description: 更新暈映發佈格式設定。
solution: Experience Manager
title: updateVignettePublishFormat
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 7f199ed4-375f-4451-b66a-e50bcd55bf23
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '436'
ht-degree: 5%

---

# updateVignettePublishFormat{#updatevignettepublishformat}

更新暈映發佈格式設定。

## 授權的使用者型別 {#section-2f2ad136d2884dc9bfef6da008196ed0}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 參數 {#section-8c7ba8d2bce14071b21fccb11f44749f}

**輸入(updateVignettePublishFormatParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 公司控制代碼。 |
| vignetteFormatHandle | `xsd:string` | 是 | 發佈格式控制代碼。 |
| name | `xsd:string` | 否 | 發佈格式名稱。 |
| targetWidth | `xsd:int` | 是 | 指定所產生暈映檢視的目標寬度（畫素）。 使用零，讓輸出暈映的大小與主要暈映相同。 |
| targetHeight | `xsd:int` | 是 | 指定所產生暈映檢視的目標高度（畫素）。 使用零，讓輸出暈映的大小與主要暈映相同。 |
| createPyramid | `xsd:boolean` | 是 | 建立為影像演算伺服器上的縮放最佳化的金字塔暈映。 從目標暈映大小欄位設定的大小上限開始，這會在單一暈映輸出檔案中建立多個大小檢視。 每個後續的檢視大小都會減半，直到寬度和高度都在128x128畫素以內。 |
| thumbWidth | `xsd:int` | 是 | 指定每個所產生縮圖的寬度（畫素）。 此設定為選用。 保留為0，表示沒有縮圖檔案。 |
| saveAsVersion | `xsd:int` | 是 | 指定已發佈暈映的檔案格式。 如果您有新版的「影像製作」和舊版的「影像演算伺服器」，就必須指定ImageRendering伺服器可讀取的暈映版本。 如果您指定較高的版本，影像演算伺服器將無法讀取發佈的暈映。 設定為零可發佈最新版本的暈映。 |
| sizeSuffixSeparator | `xsd:string` | 是 | 指定可將暈映名稱與表示其寬度的字尾分隔的字元。 |
| 銳利化 | `xsd:int` | 否 | 針對每個發佈暈映大小的主檢視影像套用銳利化。 銳利化可在縮放暈映時補償模糊。 |
| usmAmount | `xsd:double` | 是 | 數位不銳利化遮色片是一種彈性且強大的方式，可增加銳利度，尤其是在掃描的影像中。 這會控制每個超調的大小（邊緣邊界會變暗和變亮的程度）。 |
| usmRadius | `xsd:double` | 是 | 影響要增強的邊的大小，或是邊框變得多寬，因此較小的半徑可以增強較小規模的細節。 較高的半徑值可能會在邊緣產生光暈。 細微細節需要較小的半徑，因為相同大小或小於半徑的微小細節會遺失。 |
| usmThreshold | `xsd:int` | 是 | 控制要銳利化的最小亮度變化，或相鄰色調值在濾鏡運作之前必須相距多遠。 此設定可以銳利化較銳利的邊緣，同時保持較輕微的邊緣不變。 允許的臨界值範圍是0到255。 |

**輸出(updateVignettePublishFormatReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| vignetteFormatHandle | `xsd:string` | 是 | 處理更新的暈映發佈格式。 |

## 範例 {#section-fcba4bf2b7264786a676e315a35dbe43}

此程式碼範例會更新暈映發佈格式，並將控制代碼傳回至更新後的格式。

**要求**

```java
<updateVignettePublishFormatParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <vignetteFormatHandle>v|21|283</vignetteFormatHandle>
   <name>APIcreateVignettePublishFormat2</name>
   <targetWidth>1000</targetWidth>
   <targetHeight>800</targetHeight>
   <createPyramid>false</createPyramid>
   <thumbWidth>100</thumbWidth>
   <saveAsVersion>0</saveAsVersion>
   <sizeSuffixSeparator>-</sizeSuffixSeparator>
   <sharpen>50</sharpen>
   <usmAmount>240.0</usmAmount>
   <usmRadius>3.1</usmRadius>
   <usmThreshold>150</usmThreshold>
</updateVignettePublishFormatParam>
```

**回應**

```java
<updateVignettePublishFormatReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <vignetteFormatHandle>v|21|283</vignetteFormatHandle>
</updateVignettePublishFormatReturn>
```
