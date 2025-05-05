---
title: 影像演算HTTP通訊協定基本語法
description: 本節說明Dynamic Media影像轉譯HTTP通訊協定的基本語法。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8bf5920a-7ada-4db5-9796-05c5a17532c8
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 0%

---

# 影像演算HTTP通訊協定基本語法{#image-rendering-http-protocol-basic-syntax}

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
   <td colname="col1"> <p><span class="varname">個請求</span> </p> </td> 
   <td colname="col2"> <p>http://<span class="varname">伺服器</span>/ir/render[/<span class="varname">暈映</span> ] [ ？<span class="varname">修飾元</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname">伺服器</span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> server_address</span> [ ：<span class="varname">連線埠</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname">暈映</span> </p> </td> 
   <td colname="col2"> <p>暈映規範（相對檔案路徑或暈映目錄專案）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname">修飾元</span> </p> </td> 
   <td colname="col2"> <p><span class="varname">修飾元</span> *[ &amp; <span class="varname">修飾元</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname">修飾元</span> </p> </td> 
   <td colname="col2"> <p><span class="varname">命令</span> | { $ <span class="varname">巨集</span> $ } | { .<span class="varname">註解</span> } </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname">命令</span> </p> </td> 
   <td colname="col2"> <p>&lbrace; <span class="varname"> cmdName</span> | { $<span class="varname"> var</span> } [ = <span class="varname">值</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname">巨集</span> </p> </td> 
   <td colname="col2"> <p>指令巨集的名稱。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname">註解</span> </p> </td> 
   <td colname="col2"> <p>註解字串（被伺服器忽略）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> cmdName </span> </p> </td> 
   <td colname="col2"> <p>命令或屬性的名稱。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname">變數</span> </p> </td> 
   <td colname="col2"> <p>自訂變數的名稱。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname">值</span> </p> </td> 
   <td colname="col2"> <p>命令或變數值。 </p> </td> 
  </tr> 
 </tbody> 
</table>

*`server`*、*`cmdName`*、*`macro`*&#x200B;和&#x200B;*`var`*&#x200B;不區分大小寫。 伺服器會保留所有其他字串值的大小寫。

**伺服器識別碼**

所有Image Rendering的HTTP要求都需要&#39;`/ir/render`&#39;根內容。

**個註解**

註解可內嵌於任何位置的要求字串中，並以句點(.)識別 緊接在命令分隔符號(&amp;)後面。 註解會在下次出現（未編碼）命令分隔符號時終止。 此功能可用來將資訊新增至不供「影像伺服」使用的請求，例如時間戳記和資料庫ID。

**HTTP解碼**

影像演算會先從傳入要求中擷取&#x200B;*`object`*&#x200B;和&#x200B;*`modifiers`*。 然後將&#x200B;*`object`*&#x200B;分隔成路徑元素，這些元素會個別進行HTTP解碼。 *`modifiers`*&#x200B;字串被分隔成&#x200B;*`command`*= *`value`*&#x200B;配對，然後在命令特定處理之前先將&#x200B;*`value`*&#x200B;進行HTTP解碼。
