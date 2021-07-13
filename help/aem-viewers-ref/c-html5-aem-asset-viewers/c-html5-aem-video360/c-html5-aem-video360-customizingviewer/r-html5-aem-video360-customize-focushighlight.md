---
description: 焦點檢視器使用者介面元素周圍顯示的輸入焦點醒目提示，是由CSS類別選取器控制。
solution: Experience Manager
title: 焦點醒目提示
feature: Dynamic Media Classic，檢視器，SDK/API,360 VR影片
role: Developer,User
exl-id: 05ac1a70-c20d-4ddf-942c-181f101cb1d8
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
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
.s7video360viewer *:focus
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
.s7video360viewer *:focus { 
 outline: none; 
}
```
