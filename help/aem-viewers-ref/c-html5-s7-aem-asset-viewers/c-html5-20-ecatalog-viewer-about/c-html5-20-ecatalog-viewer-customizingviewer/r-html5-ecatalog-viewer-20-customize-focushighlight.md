---
title: 焦點反白顯示
description: 焦點檢視器使用者介面元素周圍所顯示的輸入焦點反白顯示。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 3d5737d7-1295-46a9-9b84-c43269e5a914
TQID: 'https://experienceleague.adobe.com/8xcQUHsvWwaKyz9-UA1cQbFhQmOpfiXGJ4EpERAJJow'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 74
ht-degree: 0%

---

# 焦點反白顯示{#focus-highlight}

焦點檢視器使用者介面元素周圍所顯示的輸入焦點反白顯示。

<!--<a id="section_E8B3D0BF9FF548F188F717D6EA65EC32"></a>-->

焦點反白顯示的外觀是由下列CSS類別選取器所控制：

```
.s7ecatalogviewer *:focus
```

焦點反白顯示的&#x200B;**CSS屬性**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">大綱</span> </p> </td> 
   <td colname="col2"> <p> 焦點反白顯示樣式。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例 — 若要停用所有檢視器使用者介面元素的預設瀏覽器焦點反白顯示，請將下列CSS選取器新增至檢視器的樣式表：

```
.s7ecatalogviewer *:focus { 
 outline: none; 
}
```
