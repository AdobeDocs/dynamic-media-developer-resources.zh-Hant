---
description: 樣式
solution: Experience Manager
title: 樣式
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 7%

---


# style{#style}

您可從URL查詢字串和設定套用下列命令。 套用在URL查詢字串中的命令一律優先於設定中出現的相同命令。

`style= *`cssPath`*`

<table id="table_F800F787CF0342749B934DAEB600C0EB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> cssPath</span> </span> </p> </td> 
   <td colname="col2"> <p> 相對或絕對CSS位置。 </p> <p>指定自訂CSS檔案的位置。 如果<span class="codeph"><span class="varname"> cssPath</span></span>是相對的，則會針對檢視器HTML頁面位置和<span class="codeph"> contentUrl=</span>參數的值來解析它。 </p> </td> 
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
