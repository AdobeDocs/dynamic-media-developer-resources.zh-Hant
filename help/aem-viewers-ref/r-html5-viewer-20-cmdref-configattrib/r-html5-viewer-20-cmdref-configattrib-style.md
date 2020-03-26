---
description: 'null'
seo-description: 'null'
seo-title: 樣式
solution: Experience Manager
title: 樣式
topic: Dynamic media
uuid: 6320c8dd-4827-41dc-a621-6fdf22e55003
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4

---


# style{#style}

您可從URL查詢字串和設定套用下列命令。 套用在URL查詢字串中的命令一律優先於設定中出現的相同命令。

`style= *`cssPath`*`

<table id="table_F800F787CF0342749B934DAEB600C0EB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> css路徑</span></span> </p> </td> 
   <td colname="col2"> <p> 相對或絕對CSS位置。 </p> <p>指定自訂CSS檔案的位置。 如果 <span class="codeph"><span class="varname"> cssPath</span></span> 是相對的 <span class="codeph"> ，則會針對檢視器HTML頁面位置和contentUrl=參數值來解</span> 析它。 </p> </td> 
  </tr> 
 </tbody> 
</table>

CSS檔案中的所有資產參考都會根據CSS檔案位置而解析，而非呼叫HTML頁面的位置。

## 屬性 {#section-8ce2a4493d454d97a9975fc7f9f4eb2c}

選填。

## 預設 {#section-79a827f7a3bb4f36b3d72c309155059e}

無。

## 範例 {#section-f8a0c032979047a38041abfce3f7a70b}

`style=/skins/customStyle.css`

`style=etc/dam/presets/css/html5_interactiveimage.css`

`style=etc/dam/presets/css/html5_interactivevideo.css`

`style=etc/dam/presets/css/html5_carouselviewer_dotted_light.css`
