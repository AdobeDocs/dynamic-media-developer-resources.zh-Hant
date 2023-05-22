---
title: 聚焦突出顯示
description: 在聚焦查看器用戶介面元素周圍顯示輸入焦點突出顯示。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 949b8a8b-5f59-415e-acc1-bf8cea77cbd9
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '74'
ht-degree: 0%

---

# 聚焦突出顯示{#focus-highlight}

在聚焦查看器用戶介面元素周圍顯示輸入焦點突出顯示。

<!--<a id="section_E8B3D0BF9FF548F188F717D6EA65EC32"></a>-->

焦點突出顯示的外觀由以下CSS類選擇器控制：

```
.s7ecatalogviewer *:focus
```

**焦點突出顯示的CSS屬性**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 大綱 </span> </p> </td> 
   <td colname="col2"> <p> 聚焦突出顯示樣式。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 要禁用所有查看器用戶介面元素的預設瀏覽器焦點突出顯示，請將以下CSS選擇器添加到查看器的樣式表：

```
.s7ecatalogviewer *:focus { 
 outline: none; 
}
```
