---
description: 更新視頻發佈格式設定。
solution: Experience Manager
title: 更新VignettePublishFormat
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 7f199ed4-375f-4451-b66a-e50bcd55bf23
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '434'
ht-degree: 20%

---

# 更新VignettePublishFormat{#updatevignettepublishformat}

更新視頻發佈格式設定。

## 授權用戶類型 {#section-2f2ad136d2884dc9bfef6da008196ed0}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 參數 {#section-8c7ba8d2bce14071b21fccb11f44749f}

**輸入(updateVignettePublishFormatParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| 公司句柄 | `xsd:string` | 是 | 公司負責。 |
| vignetteFormatHandle | `xsd:string` | 是 | 發佈格式句柄。 |
| 名稱 | `xsd:string` | 否 | 發佈格式名稱。 |
| 目標寬度 | `xsd:int` | 是 | 指定結果視圖的目標寬度（以像素為單位）。 使用零，使輸出視頻與主視頻的大小相同。 |
| 目標高度 | `xsd:int` | 是 | 指定生成的視圖的目標高度（以像素為單位）。 使用零，使輸出視頻與主視頻的大小相同。 |
| 建立金字塔 | `xsd:boolean` | 是 | 建立在影像演算伺服器進行縮放的最佳化的金字塔暈映。以目標暈映大小欄位設定的大小上限開始，這會在單一暈映輸出檔案中建立多個尺寸的檢視。每個後續的檢視大小都會減半，直到寬度與高度都在 128x128 像素以內。 |
| 拇指寬度 | `xsd:int` | 是 | 指定每個結果縮略圖的寬度（以像素為單位）。此設定為可選。 對於沒有縮略圖檔案，保留為零。 |
| 另存為版本 | `xsd:int` | 是 | 指定已發佈小節的檔案格式。 如果是新版本的「影像創作」和舊版本的「影像呈現伺服器」，則必須指定ImageRendering伺服器可以讀取的視頻版本。 如果指定更高版本，則影像呈現伺服器無法讀取已發佈的小節。 設定為零以在最新版本中發佈小寫。 |
| sizeSuffixSeparator | `xsd:string` | 是 | 指定可將暈映名稱與代表其寬度之字尾分隔的字元。 |
| 銳化 | `xsd:int` | 否 | 將銳化應用於每個發佈視圖大小的主視圖影像。銳化可以補償縮放小角時的模糊。 |
| usm金額 | `xsd:double` | 是 | 數字消銳屏是增強銳度的靈活而有力的方法，特別是在掃描的影像中。 這控制每個超調量的大小（邊界變得更暗和更亮的程度）。 |
| usm半徑 | `xsd:double` | 是 | 影響要增強的邊的大小或邊緣邊緣的寬度，因此半徑越小，細節越小。 半徑值越大，邊緣處的半徑值越大。 細小細節需要較小的半徑，因為大小相同或小於半徑的細小細節丟失。 |
| usm閾值 | `xsd:int` | 是 | 控制要銳化的最小亮度變化或在濾鏡工作之前相鄰色調值必須相隔多遠。 此設定可銳化更銳化的邊緣，同時保持更微妙的邊緣不變。 允許的閾值範圍是0到255。 |

**輸出(updateVignettePublishFormatReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| vignetteFormatHandle | `xsd:string` | 是 | 處理更新的視頻發佈格式。 |

## 範例 {#section-fcba4bf2b7264786a676e315a35dbe43}

此代碼示例更新格式，並將句柄返回到更新的格式。

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
