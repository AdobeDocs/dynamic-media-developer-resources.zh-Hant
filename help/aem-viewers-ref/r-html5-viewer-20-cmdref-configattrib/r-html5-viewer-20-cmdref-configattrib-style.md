---
description: 樣式
solution: Experience Manager
title: 樣式
feature: Dynamic Media Classic，檢視器，SDK/API
role: Developer,User
exl-id: a0547ada-3d8f-4ec2-a7e4-424fd1a78a28
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 7%

---

# 樣式{#style}

您可以同時從URL查詢字串和設定套用下列命令。 套用至URL查詢字串的命令一律優先於設定中出現的相同命令。

`style= *`cssPath`*`

<table id="table_F800F787CF0342749B934DAEB600C0EB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> cssPath</span> </span> </p> </td> 
   <td colname="col2"> <p> 相對或絕對CSS位置。 </p> <p>指定自訂CSS檔案的位置。 如果<span class="codeph"><span class="varname"> cssPath</span></span>是相對的，則會針對檢視器HTML頁面位置和<span class="codeph"> contentUrl=</span>參數的值進行解析。 </p> </td> 
  </tr> 
 </tbody> 
</table>

CSS檔案內的所有資產參考都會根據CSS檔案位置而非呼叫HTML頁面的位置來解析。

## 屬性 {#section-8ce2a4493d454d97a9975fc7f9f4eb2c}

選填。

## 預設 {#section-79a827f7a3bb4f36b3d72c309155059e}

無。

## 範例 {#section-f8a0c032979047a38041abfce3f7a70b}

`style=/skins/customStyle.css`

`style=etc/dam/presets/css/html5_interactiveimage.css`

`style=etc/dam/presets/css/html5_interactivevideo.css`

`style=etc/dam/presets/css/html5_carouselviewer_dotted_light.css`
