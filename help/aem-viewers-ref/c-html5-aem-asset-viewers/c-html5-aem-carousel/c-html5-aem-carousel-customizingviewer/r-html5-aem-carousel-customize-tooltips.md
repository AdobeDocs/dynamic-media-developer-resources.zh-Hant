---
description: 在案頭系統上，有些使用者介面元素（例如按鈕）的工具提示會顯示在滑鼠暫留狀態。
seo-description: 在案頭系統上，有些使用者介面元素（例如按鈕）的工具提示會顯示在滑鼠暫留狀態。
seo-title: 工具提示
solution: Experience Manager
title: 工具提示
topic: Dynamic media
uuid: c720c896-e540-4c1e-a0dc-31cc0300fea8
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Tooltips{#tooltips}

在案頭系統上，有些使用者介面元素（例如按鈕）的工具提示會顯示在滑鼠暫留狀態。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**主檢視器區域的CSS屬性**

工具提示的外觀由下列CSS類別選擇器控制：

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
   <td colname="col1"> <p> <span class="codeph"> 邊框半徑 </span> </p> </td> 
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
   <td colname="col2"> <p>文字色彩. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>文字字型名稱. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字型大小 </span> </p> </td> 
   <td colname="col2"> <p>文字字型大小。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>如果工具提示樣式是從內嵌網頁自訂，所有屬性都必須包含 `!IMPORTANT` 規則。 如果在檢視器的CSS檔案中自訂工具提示，則不需要這個提示。

範例——若要設定工具提示，其中灰色邊框的圓角半徑為3像素、黑色背景和Arial中的白色文字，大小為11像素：

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

