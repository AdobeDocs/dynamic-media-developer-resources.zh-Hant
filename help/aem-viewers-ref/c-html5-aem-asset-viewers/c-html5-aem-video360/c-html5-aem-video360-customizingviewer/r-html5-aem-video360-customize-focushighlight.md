---
title: 聚焦突出顯示
description: 使用CSS類選擇器控制聚焦查看器用戶介面元素周圍顯示的輸入焦點突出顯示。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 05ac1a70-c20d-4ddf-942c-181f101cb1d8
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 1%

---

# 聚焦突出顯示{#focus-highlight}

使用CSS類選擇器控制聚焦查看器用戶介面元素周圍顯示的輸入焦點突出顯示。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS屬性**

外觀由以下CSS類選擇器控制：

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
   <td colname="col1"> <p> <span class="codeph"> 大綱 </span> </p> </td> 
   <td colname="col2"> <p>聚焦突出顯示樣式。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 要禁用所有查看器用戶介面元素的預設瀏覽器焦點突出顯示，請將以下CSS選擇器添加到查看器的樣式表：

```
.s7video360viewer *:focus { 
 outline: none; 
}
```
