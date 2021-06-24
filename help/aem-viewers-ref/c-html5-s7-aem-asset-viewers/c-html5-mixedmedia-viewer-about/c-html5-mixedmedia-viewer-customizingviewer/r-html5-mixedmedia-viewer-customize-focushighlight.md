---
description: 焦點檢視器UI元素周圍顯示的輸入焦點醒目提示，是由CSS類別選取器控制。
solution: Experience Manager
title: 焦點醒目提示
feature: Dynamic Media Classic，檢視器，SDK/API，混合媒體集
role: Developer,Business Practitioner
exl-id: 7d29dab2-6f01-4328-9e92-0c370acaa2d6
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 1%

---

# 焦點醒目提示{#focus-highlight}

焦點檢視器UI元素周圍顯示的輸入焦點醒目提示，是由CSS類別選取器控制。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS屬性**

使用以下CSS類選擇器控制外觀：

```
.s7mixedmediaviewer *:focus
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
.s7mixedmediaviewer *:focus { 
 outline: none; 
}
```
