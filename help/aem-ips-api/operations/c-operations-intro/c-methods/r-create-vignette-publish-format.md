---
description: 為暈映建立新的發佈格式。
solution: Experience Manager
title: createVignettePublishFormat
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: d58e1290-8a79-4129-99ce-776b919dea13
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '523'
ht-degree: 14%

---

# createVignettePublishFormat{#createvignettepublishformat}

為暈映建立新的發佈格式。

暈映格式指定已發佈的暈映及其縮圖的大小，以及縮放等級、銳利化參數，以及從IPS發佈到影像呈現伺服器的主要暈映所產生暈映的檔案格式版本。

較新的影像轉譯伺服器版本可支援金字塔暈映，因此不需要為發佈定義特定暈映格式大小。

## 授權的使用者類型 {#section-f5c563e3695c4dba8df41e2a965aace7}

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 處理暈船所屬的公司。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 名稱</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 代碼片語  </span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 用於標識暈映發佈格式的名稱。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> targetWidth</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 代碼片語  </span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> <p>指定所產生暈映檢視的目標寬度（像素）。 </p> <p>使用零，使輸出暈映的大小與主暈映的大小相同。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> targetHeight</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 代碼片語  </span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 建立在影像演算伺服器進行縮放的最佳化的金字塔暈映。以目標暈映大小欄位設定的大小上限開始，這會在單一暈映輸出檔案中建立多個尺寸的檢視。每個後續的檢視大小都會減半，直到寬度與高度都在 128x128 像素以內。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> createPyramid</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 代碼片語  </span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 指定每個產生縮圖的寬度（像素）。此設定為選用。 保留為零，不保留縮圖檔案。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> thumbWidth</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 代碼片語  </span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 指定已發佈暈映的檔案格式。 給定新版本的影像創作和較舊版本的影像呈現伺服器，必須指定ImageRendering伺服器可讀取的暈映版本。 如果您指定較高的版本，影像呈現伺服器將無法讀取已發佈的暈映。 設為零，在最新版本發佈暈映。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> saveAsVersion</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 代碼片語  </span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 指定分隔暈映名稱的字元和表示其寬度的尾碼。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> sizeSuffixSeparator</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 代碼片語  </span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 指定分隔暈映名稱的字元和表示其寬度的尾碼。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 銳利化</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 代碼片語  </span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 將銳利化套用至每個曝光暈映大小的主檢視影像銳利化可補償縮放暈映時的模糊。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> usmAmount</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 代碼片語  </span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 數字銳利化遮色片是一種靈活且功能強大的方法，可提高銳利度，特別是在掃描的影像中。 這會控制每個超調量的大小（邊界變暗和亮的程度）。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> usmRadius</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 代碼片語  </span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 影響要增強的邊緣的大小或邊緣邊緣的寬度，因此，較小的半徑可增強較小的尺寸細節。 半徑值越大，邊緣處就會出現半徑。 精細細節需要較小的半徑，因為相同大小或小於半徑的細小細節丟失。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> usmThreshold</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 代碼片語  </span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 控制最小亮度變化為銳化，或在濾鏡工作之前相鄰色調值的距離。 此設定可銳化更銳利的邊緣，同時保持更細微的邊緣未變。 允許的閾值範圍為0到255。 </td> 
  </tr> 
 </tbody> 
</table>

**輸出(createVignettePublishFormatReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`vignetteFormatHandle`*` | `xsd:string` | 是 | 建立的暈映格式的句柄。 |

## 範例 {#section-0564752d439642b9bb8de2903db6de1e}

此程式碼會建立暈映發佈格式。 建立請求會指定名稱、目標寬度和高度，以及其他必要值。

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
