---
title: 樣式
description: 樣式
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: a0547ada-3d8f-4ec2-a7e4-424fd1a78a28
source-git-commit: c99aac44711852d8ac661878e11ce0b19d3dbf60
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 7%

---

# 樣式{#style}

可以從URL查詢字串和配置中應用以下命令。 在URL查詢字串中應用的命令始終優先於配置中存在的相同命令。

`style= *`css路徑`*`

<table id="table_F800F787CF0342749B934DAEB600C0EB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> css路徑</span> </span> </p> </td> 
   <td colname="col2"> <p> 相對或絕對CSS位置。 </p> <p>指定自定義CSS檔案的位置。 如果 <span class="codeph"><span class="varname"> css路徑</span></span> 是相對的，它根據查看器HTML頁面位置和 <span class="codeph"> 內容URL=</span> 的下界。 </p> </td> 
  </tr> 
 </tbody> 
</table>

CSS檔案中的所有資產引用都根據CSS檔案位置而不是調用HTML頁的位置進行解析。

## 屬性 {#section-8ce2a4493d454d97a9975fc7f9f4eb2c}

選擇性.

## 預設 {#section-79a827f7a3bb4f36b3d72c309155059e}

無。

## 範例 {#section-f8a0c032979047a38041abfce3f7a70b}

`style=/skins/customStyle.css`

`style=etc/dam/presets/css/html5_interactiveimage.css`

`style=etc/dam/presets/css/html5_interactivevideo.css`

`style=etc/dam/presets/css/html5_carouselviewer_dotted_light.css`
