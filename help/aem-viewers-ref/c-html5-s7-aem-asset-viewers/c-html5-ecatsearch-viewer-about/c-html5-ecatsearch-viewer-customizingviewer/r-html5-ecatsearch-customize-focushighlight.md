---
description: 聚焦查看器用戶介面元素周圍顯示的輸入焦點突出顯示。
solution: Experience Manager
title: 焦點醒目提示
feature: Dynamic Media Classic，檢視器，SDK/API,eCatalog搜尋
role: Developer,User
exl-id: 949b8a8b-5f59-415e-acc1-bf8cea77cbd9
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 0%

---

# 焦點醒目提示{#focus-highlight}

聚焦查看器用戶介面元素周圍顯示的輸入焦點突出顯示。

<!--<a id="section_E8B3D0BF9FF548F188F717D6EA65EC32"></a>-->

焦點醒目提示的外觀由下列CSS類別選取器控制：

```
.s7ecatalogviewer *:focus
```

**焦點醒目提示的CSS屬性**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 大綱  </span> </p> </td> 
   <td colname="col2"> <p> 焦點突出顯示樣式。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例：若要停用所有檢視器使用者介面元素的預設瀏覽器焦點醒目提示，請將下列CSS選取器新增至檢視器的樣式表：

```
.s7ecatalogviewer *:focus { 
 outline: none; 
}
```
