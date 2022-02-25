---
title: 聚焦突出顯示
description: 在聚焦查看器使用介面元素周圍顯示的輸入焦點高亮由CSS類選擇器控制。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 74ff9669-d56b-4731-9d4a-dda7c831e162
source-git-commit: 7eddc50fb9803eacdd1f513c6132380793b6f88d
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 1%

---

# 聚焦突出顯示{#focus-highlight}

在聚焦查看器使用介面元素周圍顯示的輸入焦點高亮由CSS類選擇器控制。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

外觀由以下CSS類選擇器控制：

```
.s7basiczoomviewer *:focus
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
   <td colname="col2"> <p>聚焦突出顯示樣式。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 要禁用所有查看器用戶介面元素的預設瀏覽器焦點突出顯示，請將以下CSS選擇器添加到查看器的樣式表：

```
.s7basiczoomviewer *:focus { 
 outline: none; 
}
```
