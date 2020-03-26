---
description: 在焦點檢視器使用者介面元素周圍顯示的輸入焦點反白顯示。
seo-description: 在焦點檢視器使用者介面元素周圍顯示的輸入焦點反白顯示。
seo-title: 焦點反白顯示
solution: Experience Manager
title: 焦點反白顯示
topic: Dynamic media
uuid: 50411b68-8d01-4240-b548-a6c51374a8c6
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

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
   <td colname="col1"> <p> <span class="codeph"> 大綱 </span> </p> </td> 
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

