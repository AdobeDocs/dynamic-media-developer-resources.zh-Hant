---
title: 焦點醒目提示
description: 焦點檢視器UI元素周圍顯示的輸入焦點醒目提示，是由CSS類別選取器控制。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: 9968c67b-02cc-4ac0-8ab1-c7eda565912d
source-git-commit: b6ebc938f55117c4144ff921bed7f8742cf3a8a7
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 1%

---

# 焦點醒目提示{#focus-highlight}

焦點檢視器UI元素周圍顯示的輸入焦點醒目提示，是由CSS類別選取器控制。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS屬性**

使用以下CSS類選擇器控制外觀：

```
.s7smartcropvideoviewer *:focus
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
   <td colname="col1"> <p> <span class="codeph"> 大綱 </span> </p> </td> 
   <td colname="col2"> <p>焦點突出顯示樣式。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例：若要停用所有檢視器使用者介面元素的預設瀏覽器焦點醒目提示，請將下列CSS選取器新增至檢視器的樣式表：

```
.s7smartcropvideoviewer *:focus { 
 outline: none; 
}
```
