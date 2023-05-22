---
title: 工具提示
description: 在案頭系統上，一些用戶介面元素（如按鈕）具有滑鼠懸停時顯示的工具提示。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: bbf8e8f0-eb1c-49fa-a501-4c7ed7827595
source-git-commit: cdc85af782ebc492ae2303469a7f4f54b5bc09c8
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 2%

---

# 工具提示{#tooltips}

在案頭系統上，一些用戶介面元素（如按鈕）具有滑鼠懸停時顯示的工具提示。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**主查看器區域的CSS屬性**

工具提示的外觀由以下CSS類選擇器控制：

```
.s7tooltip
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
   <td colname="col1"> <p> <span class="codeph"> 邊界半徑 </span> </p> </td> 
   <td colname="col2"> <p> 背景邊框半徑。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 邊框顏色 </span> </p> </td> 
   <td colname="col2"> <p> 背景邊框顏色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景色 </span> </p> </td> 
   <td colname="col2"> <p> 背景顏色. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>文本顏色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字型系列 </span> </p> </td> 
   <td colname="col2"> <p>文本字型名稱。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字型大小 </span> </p> </td> 
   <td colname="col2"> <p>文本字型大小。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>如果工具提示樣式是從嵌入網頁中自定義的，則所有屬性必須包含 `!IMPORTANT` 規則。 如果在查看器的CSS檔案中自定義了工具提示，則不需要此規則。

示例 — 要設定具有3像素角半徑的灰色邊框、黑色背景和用Arial®書寫的白色文本的工具提示，大小為11像素：

```
.s7tooltip { 
 border-radius: 3px 3px 3px 3px; 
 border-color: #999999; 
 background-color: #000000; 
 color: #FFFFFF; 
 font-family: Arial, Helvetica, sans-serif; 
 font-size: 11px; 
}
```
