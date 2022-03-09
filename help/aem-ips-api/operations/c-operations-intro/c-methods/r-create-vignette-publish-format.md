---
description: 為視頻建立新發佈格式。
solution: Experience Manager
title: createVignettePublishFormat
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d58e1290-8a79-4129-99ce-776b919dea13
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '518'
ht-degree: 14%

---

# createVignettePublishFormat{#createvignettepublishformat}

為視頻建立新發佈格式。

Vignette格式指定已發佈的小格及其縮略圖的大小，以及從IPS發佈到影像呈現伺服器的主小格生成的小格的縮放級別、銳化參數和檔案格式版本。

較新的「影像渲染」伺服器版本可支援金字塔形小圖，因此無需為發佈定義特定的格式大小。

## 授權用戶類型 {#section-f5c563e3695c4dba8df41e2a965aace7}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 參數 {#section-3a368186ec1d4005bca056fc9d9bacc7}

**輸入(createVignettePublishFormatParam)**

<table id="table_4D5B2913FA784EC09190F25223C1A680"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 名稱 </th> 
   <th colname="col2" class="entry"> 類型 </th> 
   <th colname="col3" class="entry"> 必要 </th> 
   <th colname="col4" class="entry"> 說明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 公司句柄</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 把手給收信人所屬的公司。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 名稱</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 代碼短語 </span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 用於標識視頻發佈格式的名稱。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 目標寬度</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 代碼短語 </span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> <p>指定結果視圖的目標寬度（以像素為單位）。 </p> <p>使用零，使輸出視頻與主視頻的大小相同。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 目標高度</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 代碼短語 </span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 建立在影像演算伺服器進行縮放的最佳化的金字塔暈映。以目標暈映大小欄位設定的大小上限開始，這會在單一暈映輸出檔案中建立多個尺寸的檢視。每個後續的檢視大小都會減半，直到寬度與高度都在 128x128 像素以內。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 建立金字塔</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 代碼短語 </span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 指定每個結果縮略圖的寬度（以像素為單位）。此設定為可選。 對於沒有縮略圖檔案，保留為零。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 拇指寬度</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 代碼短語 </span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 指定已發佈小節的檔案格式。 如果給定了新版本的影像創作和較舊版本的影像呈現伺服器，則必須指定ImageRendering伺服器可以讀取的視頻版本。 如果指定更高版本，則影像呈現伺服器無法讀取已發佈的小節。 設定為零以在最新版本中發佈小寫。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 另存為版本</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 代碼短語 </span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 指定分隔視頻名稱和表示其寬度的尾碼的字元。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> sizeSuffixSeparator</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 代碼短語 </span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 指定分隔視頻名稱和表示其寬度的尾碼的字元。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 銳化</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 代碼短語 </span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 將銳化應用於每個小小的視頻尺寸的主視圖影像，可以補償縮放小格時的模糊。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> usm金額</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 代碼短語 </span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 數字消銳屏是增強銳度的靈活而有力的方法，特別是在掃描的影像中。 這控制每個超調量的大小（邊緣邊界變黑和變亮的程度）。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> usm半徑</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 代碼短語 </span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 影響要增強的邊的大小或邊緣邊緣邊緣的寬度，因此，較小的弧度會增強較小尺度的細節。 半徑值越大，邊緣處的半徑值越大。 細小細節需要較小的半徑，因為大小相同或小於半徑的細小細節丟失。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> usm閾值</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 代碼短語 </span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 控制要銳化的最小亮度變化或在濾鏡工作之前相鄰色調值必須相隔多遠。 此設定可銳化更銳化的邊緣，同時保持更微妙的邊緣不變。 閾值的允許範圍為0到255。 </td> 
  </tr> 
 </tbody> 
</table>

**輸出(createVignettePublishFormatReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| vignetteFormatHandle | `xsd:string` | 是 | 建立的視頻格式的句柄。 |

## 範例 {#section-0564752d439642b9bb8de2903db6de1e}

此代碼建立虛擬發佈格式。 建立請求指定名稱、目標寬度和高度以及其他必需值。

**請求**

```java
<createVignettePublishFormatParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <name>APIcreateVignettePublishFormat1</name>
   <targetWidth>1200</<targetWidth>
   <targetHeight>800</targetHeight>
   <createPyramid>true</createPyramid>
   <thumbWidth>400</thumbWidth>
   <saveAsVersion>0</saveAsVersion>
   <sizeSuffixSeparator>-</sizeSuffixSeparator>
   <sharpen>50</sharpen>
   <usmAmount>230.0</usmAmount>
   <usmRadius>1.1</usmRadius>
   <usmThreshold>130</usmThreshold>
</createVignettePublishFormatParam>
```

**回答**

```java
<createVignettePublishFormatReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <vignetteFormatHandle>v|21|282</vignetteFormatHandle>
</createVignettePublishFormatReturn>
```
