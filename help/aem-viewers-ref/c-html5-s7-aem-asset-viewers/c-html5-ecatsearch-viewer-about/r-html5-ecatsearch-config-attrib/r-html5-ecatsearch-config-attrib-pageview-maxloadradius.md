---
description: PageView.maxloadradius
solution: Experience Manager
title: PageView.maxloadradius
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: cf769b2d-be4e-4d93-9620-00a438157693
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '65'
ht-degree: 4%

---

# PageView.maxloadradius{#pageview-maxloadradius}

[!DNL `[PageView.|<containerId>_pageView.]maxloadradius=-1|0| *`預載入br`*`]

<table id="table_985ADD6C9BD04C629A84C9C625CCCFEB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph">-1|0|<span class="varname"> 預載入br</span></span> </p> </td> 
   <td colname="col2"> <p>指定元件預載入行為。 </p> <p>設定為時 <span class="codeph"> -1</span> 元件在空閒狀態下預載所有目錄幀。 </p> <p> 設定為時 <span class="codeph"> 0</span> 該元件僅載入當前可見的幀、上一幀和下一幀。 </p> <p>設定 <span class="codeph"><span class="varname"> 預載入br</span></span> 定義當前顯示的幀周圍以空閒狀態預載的不可見幀的數量。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-4b7952997f9240e581d21bcdb173f9af}

選擇性.

## 預設 {#section-f0d5211aa2494f27a5a85e4a54b24ea2}

[!DNL `1`]

## 範例 {#section-4e27dfc1e2ce4dd7a4996dc575ab7a93}

[!DNL `maxloadradius=0`]
