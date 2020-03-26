---
description: 本節說明Scene7 Image Rendering HTTP通訊協定的基本語法。
seo-description: 本節說明Scene7 Image Rendering HTTP通訊協定的基本語法。
seo-title: 影像轉換HTTP通訊協定基本語法
solution: Experience Manager
title: 影像轉換HTTP通訊協定基本語法
topic: Scene7 Image Serving - Image Rendering API
uuid: e01314f0-6aaa-41ca-8c05-d5db3148a071
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 影像轉換HTTP通訊協定基本語法{#image-rendering-http-protocol-basic-syntax}

本節說明Scene7 Image Rendering HTTP通訊協定的基本語法。

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
   <td colname="col2"> <p>http://<span class="varname"> server</span>/ir/render[/<span class="varname"> vignette</span> ] [ ?<span class="varname"> 修飾元</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> 伺服器 </span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> server_address</span> [ :<span class="varname"> 埠</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> vignette </span> </p> </td> 
   <td colname="col2"> <p>暈映指定符（相對檔案路徑或暈映目錄項目）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> 修飾元 </span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> 修飾詞</span> *[ &amp;修飾 <span class="varname"> 詞</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> 修飾元 </span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> 命令</span> | { $ <span class="varname"> macro</span> $ }| {<span class="varname"> 注釋</span> } </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> 命令 </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="varname"> cmdName</span> | { $<span class="varname"> var</span> } } [ = <span class="varname"> value</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> 宏 </span> </p> </td> 
   <td colname="col2"> <p>命令宏的名稱。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> 評論 </span> </p> </td> 
   <td colname="col2"> <p>注釋字串（伺服器忽略）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> cmdName </span> </p> </td> 
   <td colname="col2"> <p>命令或屬性的名稱。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> var </span> </p> </td> 
   <td colname="col2"> <p>自訂變數的名稱。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> 值 </span> </p> </td> 
   <td colname="col2"> <p>命令或變數值。 </p> </td> 
  </tr> 
 </tbody> 
</table>

*`server`*、 *`cmdName`*、 *`macro`*&#x200B;和 *`var`* 不區分大小寫。 伺服器會保留所有其他字串值的大小寫。

**伺服器識別碼**

所有「影 `/ir/render`像演算」的HTTP要求都需要「」根內容。

**備註**

注釋可以嵌入到任意位置的請求字串中，並由句點(.)標識緊接在命令分隔符(&amp;)後面。 注釋由下次出現（未編碼）命令分隔符終止。 此功能可用來新增非影像伺服使用之要求的資訊，例如時間戳記、資料庫ID等。

**HTTP解碼**

「影像演算」會先擷 *`object`* 取傳入 *`modifiers`* 的請求並從中擷取。 *`object`* 然後，將其分割為路徑元素，這些元素會個別HTTP解碼。 字 *`modifiers`* 串會分成 *`command`*= *`value`* 對，然後在指令特定處理 *`value`* 前先進行HTTP解碼。
