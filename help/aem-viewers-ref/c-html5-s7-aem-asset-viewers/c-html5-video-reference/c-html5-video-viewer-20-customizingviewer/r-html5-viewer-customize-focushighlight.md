---
description: 使用CSS類別選擇器控制顯示在焦點檢視器UI元素周圍的輸入焦點反白顯示。
seo-description: 使用CSS類別選擇器控制顯示在焦點檢視器UI元素周圍的輸入焦點反白顯示。
seo-title: 焦點反白顯示
solution: Experience Manager
title: 焦點反白顯示
topic: Dynamic Media
uuid: cf5acb11-168e-4303-a637-d959687a0548
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 1%

---


# 焦點反白顯示{#focus-highlight}

使用CSS類別選擇器控制顯示在焦點檢視器UI元素周圍的輸入焦點反白顯示。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS屬性**

外觀是使用下列CSS類別選取器來控制：

```
.s7videoviewer *:focus
```

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS屬性 </p> </th> 
   <th colname="col2" class="entry"> <p>說明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 大綱  </span> </p> </td> 
   <td colname="col2"> <p>焦點反白顯示樣式。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例——若要停用所有檢視器使用者介面元素的預設瀏覽器焦點反白顯示，請將下列CSS選取器新增至檢視器的樣式表：

```
.s7videoviewer *:focus { 
 outline: none; 
}
```

