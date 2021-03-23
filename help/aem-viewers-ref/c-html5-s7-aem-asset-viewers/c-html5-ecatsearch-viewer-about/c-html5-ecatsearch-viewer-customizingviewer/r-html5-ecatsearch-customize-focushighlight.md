---
description: 在焦點檢視器使用者介面元素周圍顯示的輸入焦點反白顯示。
seo-description: 在焦點檢視器使用者介面元素周圍顯示的輸入焦點反白顯示。
seo-title: 焦點反白顯示
solution: Experience Manager
title: 焦點反白顯示
uuid: 0bd36795-e663-4f0e-8310-a57c2ffae4a2
feature: Dynamic Media經典，檢視器，SDK/API,eCatalog搜尋
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 0%

---


# 焦點反白顯示{#focus-highlight}

在焦點檢視器使用者介面元素周圍顯示的輸入焦點反白顯示。

<!--<a id="section_E8B3D0BF9FF548F188F717D6EA65EC32"></a>-->

焦點反白顯示的外觀由下列CSS類別選擇器控制：

```
.s7ecatalogviewer *:focus
```

**焦點反白顯示的CSS屬性**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 大綱  </span> </p> </td> 
   <td colname="col2"> <p> 焦點反白顯示樣式。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例——若要停用所有檢視器使用者介面元素的預設瀏覽器焦點反白顯示，請將下列CSS選擇器新增至檢視器的樣式表：

```
.s7ecatalogviewer *:focus { 
 outline: none; 
}
```

