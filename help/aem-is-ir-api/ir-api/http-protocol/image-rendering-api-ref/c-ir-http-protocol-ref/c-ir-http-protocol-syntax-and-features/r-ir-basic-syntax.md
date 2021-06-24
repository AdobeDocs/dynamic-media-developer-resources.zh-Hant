---
description: 本節說明Dynamic Media影像轉譯HTTP通訊協定的基本語法。
solution: Experience Manager
title: 影像呈現HTTP通訊協定基本語法
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 8bf5920a-7ada-4db5-9796-05c5a17532c8
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '228'
ht-degree: 3%

---

# 影像呈現HTTP通訊協定基本語法{#image-rendering-http-protocol-basic-syntax}

本節說明Dynamic Media影像轉譯HTTP通訊協定的基本語法。

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
   <td colname="col2"> <p>http://<span class="varname">伺服器</span>/ir/render[/<span class="varname">暈</span> ] [?<span class="varname"> 修飾元</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> 伺服器 </span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> server_address</span> [ :<span class="varname"> port</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> vignette  </span> </p> </td> 
   <td colname="col2"> <p>暈映說明符（相對檔案路徑或暈映目錄條目）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> 修飾元 </span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> 修飾詞</span> *[ &amp;  <span class="varname"> 修飾詞</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> 修飾元 </span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> 命令</span> | { $ <span class="varname"> macro</span> $ } | { 。<span class="varname"> comment</span> } </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> 命令  </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="varname"> cmdName</span> | { $<span class="varname"> var</span> } } [ = <span class="varname"> value&lt;a5/]</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> 宏  </span> </p> </td> 
   <td colname="col2"> <p>命令宏的名稱。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> 註解  </span> </p> </td> 
   <td colname="col2"> <p>注釋字串（由伺服器忽略）。 </p> </td> 
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
   <td colname="col1"> <p><span class="varname"> value  </span> </p> </td> 
   <td colname="col2"> <p>命令或變數值。 </p> </td> 
  </tr> 
 </tbody> 
</table>

*`server`*、  *`cmdName`*、  *`macro`*&#x200B;和 *`var`* 不區分大小寫。伺服器會保留所有其他字串值的大小寫。

**伺服器識別碼**

對於影像呈現的所有HTTP請求，都需要「 `/ir/render`」根上下文。

**備註**

註解可隨處內嵌至要求字串，並以句點(.)識別 緊接在命令分隔符(&amp;)後面。 注釋由下次出現（未編碼）命令分隔符終止。 此功能可用來將資訊新增至非影像伺服使用的請求，例如時間戳、資料庫ID等。

**HTTP解碼**

影像呈現會先從傳入的請求中擷取&#x200B;*`object`*&#x200B;和&#x200B;*`modifiers`*。 *`object`* 然後被分離為路徑元素，這些路徑元素被單獨HTTP解碼。將&#x200B;*`modifiers`*&#x200B;字串分為&#x200B;*`command`*= *`value`*&#x200B;對，然後在命令特定處理之前對&#x200B;*`value`*&#x200B;進行HTTP解碼。
