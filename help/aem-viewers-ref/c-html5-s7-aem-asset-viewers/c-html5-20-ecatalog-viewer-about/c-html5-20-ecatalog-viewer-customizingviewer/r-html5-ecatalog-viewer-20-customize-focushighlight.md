---
description: 聚焦查看器用戶介面元素周圍顯示的輸入焦點突出顯示。
solution: Experience Manager
title: 焦點醒目提示
feature: Dynamic Media Classic，檢視器，SDK/API,eCatalog
role: Developer,Business Practitioner
exl-id: 3d5737d7-1295-46a9-9b84-c43269e5a914
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '81'
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
