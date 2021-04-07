---
description: 使用CSS類別選擇器控制顯示在焦點檢視器使用者介面元素周圍的輸入焦點反白顯示。
solution: Experience Manager
title: 焦點反白顯示
feature: Dynamic Media經典，檢視器，SDK/API，轉盤橫幅
role: 開發人員，商業從業人員
exl-id: f9343055-9fd9-4b19-bba3-1f742acb6193
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 1%

---

# 焦點反白顯示{#focus-highlight}

使用CSS類別選擇器控制顯示在焦點檢視器使用者介面元素周圍的輸入焦點反白顯示。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS屬性**

外觀是使用下列CSS類別選取器來控制：

```
.s7carouselviewer *:focus
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
.s7carouselviewer *:focus { 
 outline: none; 
}
```
