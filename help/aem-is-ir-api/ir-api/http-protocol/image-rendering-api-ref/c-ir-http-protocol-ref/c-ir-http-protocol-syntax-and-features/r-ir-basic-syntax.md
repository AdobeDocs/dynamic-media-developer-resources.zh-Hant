---
title: 影像呈現HTTP協定基本語法
description: 本節介紹Dynamic Media影像呈現HTTP協定的基本語法。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8bf5920a-7ada-4db5-9796-05c5a17532c8
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 3%

---

# 影像呈現HTTP協定基本語法{#image-rendering-http-protocol-basic-syntax}

本節介紹Dynamic Media影像呈現HTTP協定的基本語法。

<table id="table_0A7D7207EE6D4B08B62BE8620EBE0B25"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>項目 </p> </th> 
   <th colname="col2" class="entry"> <p>定義 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> 請求</span> </p> </td> 
   <td colname="col2"> <p>http://<span class="varname"> 伺服器</span>/ir/render[/<span class="varname"> 維涅特</span> ] [<span class="varname"> 修飾元</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> 伺服器 </span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> 伺服器地址</span> [ :<span class="varname"> 埠</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> 維涅特 </span> </p> </td> 
   <td colname="col2"> <p>Vignette說明符（相對檔案路徑或Vignette目錄條目）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> 修飾元 </span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> 修飾</span> *[ &amp; <span class="varname"> 修飾</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> 修飾 </span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> 命令</span> | { $ <span class="varname"> 宏</span> $ } | {<span class="varname"> 注釋</span> } </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> 命令 </span> </p> </td> 
   <td colname="col2"> <p>{ 0} <span class="varname"> cmd名稱</span> | { $<span class="varname"> var</span> } [ = <span class="varname"> 值</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> 宏 </span> </p> </td> 
   <td colname="col2"> <p>命令宏的名稱。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> 注釋 </span> </p> </td> 
   <td colname="col2"> <p>注釋字串（被伺服器忽略）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> cmd名稱 </span> </p> </td> 
   <td colname="col2"> <p>命令或屬性的名稱。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> var </span> </p> </td> 
   <td colname="col2"> <p>自定義變數的名稱。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> 值 </span> </p> </td> 
   <td colname="col2"> <p>命令或變數值。 </p> </td> 
  </tr> 
 </tbody> 
</table>

*`server`*。 *`cmdName`*。 *`macro`*, *`var`* 不區分大小寫。 伺服器保留所有其他字串值的大小寫。

**伺服器標識符**

&#39; `/ir/render`&#39;對映像呈現的所有HTTP請求都需要根上下文。

**備註**

注釋可以嵌入到任何位置的請求字串中，並由句點(.)標識 緊跟在命令分隔符(&amp;)後。 注釋由（未編碼）命令分隔符的下一次出現終止。 此功能可用於向不用於影像服務的請求添加資訊，如時間戳和資料庫ID。

**HTTP解碼**

影像渲染首先提取 *`object`* 和 *`modifiers`* 從傳入的請求。 的 *`object`* 然後將其分離成路徑元素，這些路徑元素被逐個HTTP解碼。 的 *`modifiers`* 字串分隔成 *`command`*= *`value`* 對，和 *`value`* 然後在命令特定處理之前對HTTP進行解碼。
