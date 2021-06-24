---
description: 焦點檢視器使用者介面元素周圍顯示的輸入焦點醒目提示，是由CSS類別選取器控制。
solution: Experience Manager
title: 焦點醒目提示
feature: Dynamic Media Classic，檢視器，SDK/API，輪播橫幅
role: Developer,Business Practitioner
exl-id: f9343055-9fd9-4b19-bba3-1f742acb6193
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 1%

---

# 焦點醒目提示{#focus-highlight}

焦點檢視器使用者介面元素周圍顯示的輸入焦點醒目提示，是由CSS類別選取器控制。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS屬性**

使用以下CSS類選擇器控制外觀：

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
   <td colname="col2"> <p>焦點突出顯示樣式。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例：若要停用所有檢視器使用者介面元素的預設瀏覽器焦點醒目提示，請將下列CSS選取器新增至檢視器的樣式表：

```
.s7carouselviewer *:focus { 
 outline: none; 
}
```
