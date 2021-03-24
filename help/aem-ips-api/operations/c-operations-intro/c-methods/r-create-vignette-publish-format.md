---
description: 建立暈映的新發佈格式。
solution: Experience Manager
title: createVignettePublishFormat
feature: Dynamic Media經典，SDK/API
role: 開發人員、管理員
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '525'
ht-degree: 14%

---


# createVignettePublishFormat{#createvignettepublishformat}

建立暈映的新發佈格式。

暈映格式會指定已發佈的暈映大小及其縮圖，以及縮放等級、銳利化參數，以及從IPS發佈至影像演算伺服器的主要暈映所產生的暈映檔案格式版本。

較新的影像演算伺服器版本可支援金字塔暈映，因此不需要為發佈定義特定暈映格式大小。

## 授權用戶類型{#section-f5c563e3695c4dba8df41e2a965aace7}

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
   <td colname="col4"> 暈映所屬的公司的控制代碼。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 名稱</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 程式碼片語  </span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 用以識別暈映發佈格式的名稱。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> targetWidth</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 程式碼片語  </span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> <p>指定產生暈映檢視的目標寬度（以像素為單位）。 </p> <p>使用零，使輸出暈映的大小與主暈映大小相同。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> targetHeight</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 程式碼片語  </span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 建立在影像演算伺服器進行縮放的最佳化的金字塔暈映。以目標暈映大小欄位設定的大小上限開始，這會在單一暈映輸出檔案中建立多個尺寸的檢視。每個後續的檢視大小都會減半，直到寬度與高度都在 128x128 像素以內。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> createPyramid</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 程式碼片語  </span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 指定每個產生的縮圖寬度（以像素為單位）。此設定為選用。 若沒有縮圖檔案，請保留為零。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> thumbWidth</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 程式碼片語  </span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 指定已發佈暈映的檔案格式。 如果有新版的「影像製作」和舊版的「影像轉換伺服器」，您必須指定您的「影像轉換伺服器」可以讀取的暈映版本。 如果您指定較高的版本，「影像演算」伺服器將無法讀取已發佈的暈映。 設為零，以在最新版本發佈暈映。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> saveAsVersion</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 程式碼片語  </span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 指定分隔暈映名稱的字元和表示其寬度的字尾。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> sizeSuffixSeparator</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 程式碼片語  </span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 指定分隔暈映名稱的字元和表示其寬度的字尾。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 銳利化</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 程式碼片語  </span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 將銳利化套用至每個簡單明瞭的暈映大小的主檢視影像銳利化可補償縮放暈映時的模糊。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> usmAmount</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 程式碼片語  </span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 數位銳利化遮色片是提高銳利度（尤其是在掃描的影像中）的有彈性且強大的方式。 這可控制每個超調量的大小（邊界變深和變亮的程度）。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> usmRadius</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 程式碼片語  </span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 影響要增強的邊的大小或邊緣邊緣的寬度，因此較小的半徑可增強較小尺寸的細節。 半徑值越大，邊處的光暈就會出現。 細部細節需要較小的半徑，因為大小相同或小於半徑的細部細節會丟失。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> usmThreshold</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 程式碼片語  </span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 控制要銳化的最小亮度變化，或相鄰色調值在濾鏡工作之前必須相距多遠。 此設定可銳利化更銳利的邊緣，同時保留更細微的邊緣不變。 允許的閾值範圍為0到255。 </td> 
  </tr> 
 </tbody> 
</table>

**輸出(createVignettePublishFormatReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`vignetteFormatHandle`*` | `xsd:string` | 是 | 已建立暈映格式的控制代碼。 |

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

