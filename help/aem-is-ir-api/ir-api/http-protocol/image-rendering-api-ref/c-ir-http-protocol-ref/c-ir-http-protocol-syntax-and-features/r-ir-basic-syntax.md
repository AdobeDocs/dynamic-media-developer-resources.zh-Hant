---
description: 本節介紹Dynamic Media影像渲染HTTP協定的基本語法。
solution: Experience Manager
title: 影像轉換HTTP通訊協定基本語法
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 3%

---


# 影像轉換HTTP通訊協定基本語法{#image-rendering-http-protocol-basic-syntax}

本節介紹Dynamic Media影像渲染HTTP協定的基本語法。

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
   <td colname="col2"> <p>http://<span class="varname"> server</span>/ir/render[/<span class="varname">暈映</span> ] [ ?<span class="varname"> 修飾元</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> 伺服器 </span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> server_address</span> [ :<span class="varname"> port</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> vignette  </span> </p> </td> 
   <td colname="col2"> <p>暈映指定符（相對檔案路徑或暈映目錄項目）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> 修飾元 </span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> 修飾</span> 元*[ &amp;修飾 <span class="varname"> 元</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> 修飾元 </span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> command</span> | { $  <span class="varname"> macro</span> $ } | {<span class="varname"> comment</span> } </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> 命令  </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="varname"> cmdName</span> | { $<span class="varname"> var</span> } [ = <span class="varname"> value</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> 宏  </span> </p> </td> 
   <td colname="col2"> <p>命令宏的名稱。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> 評論  </span> </p> </td> 
   <td colname="col2"> <p>注釋字串（伺服器忽略）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> cmdName  </span> </p> </td> 
   <td colname="col2"> <p>命令或屬性的名稱。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> var </span> </p> </td> 
   <td colname="col2"> <p>自訂變數的名稱。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> 值  </span> </p> </td> 
   <td colname="col2"> <p>命令或變數值。 </p> </td> 
  </tr> 
 </tbody> 
</table>

*`server`*、 *`cmdName`*、 *`macro`*&#x200B;和 *`var`* 不區分大小寫。伺服器會保留所有其他字串值的大小寫。

**伺服器識別碼**

所有對影像演算的HTTP要求都需要「 `/ir/render`」根內容。

**備註**

注釋可以嵌入到任意位置的請求字串中，並由句點(.)標識 緊接在命令分隔符(&amp;)後面。 注釋由下次出現（未編碼）命令分隔符終止。 此功能可用來新增非影像伺服使用之要求的資訊，例如時間戳記、資料庫ID等。

**HTTP解碼**

「影像演算」會先從傳入的請求中擷取&#x200B;*`object`*&#x200B;和&#x200B;*`modifiers`*。 *`object`* 然後，將其分割為路徑元素，這些元素會個別HTTP解碼。將&#x200B;*`modifiers`*&#x200B;字串分隔為&#x200B;*`command`*= *`value`*&#x200B;對，然後在指令特定處理之前對&#x200B;*`value`*&#x200B;進行HTTP解碼。
