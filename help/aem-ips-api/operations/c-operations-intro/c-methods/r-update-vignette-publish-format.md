---
description: 更新暈映發佈格式設定。
solution: Experience Manager
title: updateVignettePublishFormat
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: 7f199ed4-375f-4451-b66a-e50bcd55bf23
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '439'
ht-degree: 20%

---

# updateVignettePublishFormat{#updatevignettepublishformat}

更新暈映發佈格式設定。

## 授權的使用者類型 {#section-2f2ad136d2884dc9bfef6da008196ed0}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 參數 {#section-8c7ba8d2bce14071b21fccb11f44749f}

**輸入(updateVignettePublishFormatParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 公司負責人。 |
| `*`vignetteFormatHandle`*` | `xsd:string` | 是 | 發佈格式句柄。 |
| `*`名稱`*` | `xsd:string` | 否 | 發佈格式名稱。 |
| `*`targetWidth`*` | `xsd:int` | 是 | 指定所產生暈映檢視的目標寬度（像素）。 使用零，使輸出暈映的大小與主暈映的大小相同。 |
| `*`targetHeight`*` | `xsd:int` | 是 | 指定所產生暈映檢視的目標高度（像素）。 使用零，使輸出暈映的大小與主暈映的大小相同。 |
| `*`createPyramid`*` | `xsd:boolean` | 是 | 建立在影像演算伺服器進行縮放的最佳化的金字塔暈映。以目標暈映大小欄位設定的大小上限開始，這會在單一暈映輸出檔案中建立多個尺寸的檢視。每個後續的檢視大小都會減半，直到寬度與高度都在 128x128 像素以內。 |
| `*`thumbWidth`*` | `xsd:int` | 是 | 指定每個產生縮圖的寬度（像素）。此設定為選用。 保留為零，不保留縮圖檔案。 |
| `*`saveAsVersion`*` | `xsd:int` | 是 | 指定已發佈暈映的檔案格式。 給定新版本的影像創作和舊版的影像呈現伺服器，必須指定ImageRendering伺服器可讀取的暈映版本。 如果您指定較高的版本，影像呈現伺服器將無法讀取已發佈的暈映。 設為零，在最新版本發佈暈映。 |
| `*`sizeSuffixSeparator`*` | `xsd:string` | 是 | 指定可將暈映名稱與代表其寬度之字尾分隔的字元。 |
| `*`銳利化`*` | `xsd:int` | 否 | 對每個發佈暈映大小將銳利化套用至主檢視影像。縮放暈映時，銳利化可補償模糊。 |
| `*`usmAmount`*` | `xsd:double` | 是 | 數字銳利化遮色片是一種靈活且功能強大的方法，可提高銳利度，特別是在掃描的影像中。 這會控制每個超調量的大小（邊界變深和變亮的程度）。 |
| `*`usmRadius`*` | `xsd:double` | 是 | 影響要增強的邊的大小或邊緣邊緣的寬度，因此，半徑較小可增強較小的細節。 半徑值越大，邊緣處就會出現半徑。 精細細節需要較小的半徑，因為相同大小或小於半徑的細小細節丟失。 |
| `*`usmThreshold`*` | `xsd:int` | 是 | 控制最小亮度變化為銳化，或在濾鏡工作之前相鄰色調值的距離。 此設定可銳化更銳利的邊緣，同時保持更細微的邊緣未變。 允許的閾值範圍是0到255。 |

**輸出(updateVignettePublishFormatReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`vignetteFormatHandle`*` | `xsd:string` | 是 | 處理更新的暈映發佈格式。 |

## 範例 {#section-fcba4bf2b7264786a676e315a35dbe43}

此程式碼範例會更新暈映發佈格式，並將控制代碼傳回更新的格式。

**請求**

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

**回答**

```java
<updateVignettePublishFormatReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <vignetteFormatHandle>v|21|283</vignetteFormatHandle>
</updateVignettePublishFormatReturn>
```
