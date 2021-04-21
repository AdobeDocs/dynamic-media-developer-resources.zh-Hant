---
description: HTTP協定基本語法如下。
solution: Experience Manager
title: 影像伺服HTTP通訊協定基本語法
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 1%

---


# 影像伺服HTTP通訊協定基本語法{#image-serving-http-protocol-basic-syntax}

HTTP協定基本語法如下：

<table id="simpletable_854C20D4C42247B99D9F123543C17E7C"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 請求</span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="filepath">http://<span class="varname"> server</span>/is/image[/<span class="varname"> object</span>][?<span class="varname"> 修飾元</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 伺服器  </span> </span> </p></td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> server_address</span>[:<span class="varname"> port</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 物件</span> </span> </p></td> 
  <td class="stentry"> <p>源對象指定符（影像路徑或影像目錄條目）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 修飾語</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 修飾詞</span>*[&amp;<span class="varname"> modifier</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 修飾詞</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph">command|{$<span class="varname"> macro</span>$}|{.<span class="varname"> comment</span>}</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 命令</span> </span> </p> </td> 
  <td class="stentry"> <p>{<span class="varname"> cmdName</span>|{$<span class="varname"> var</span>}}[=<span class="varname">值</span>] </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 宏</span> </span> </p> </td> 
  <td class="stentry"> <p>命令宏的名稱。</p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 評論</span> </span> </p></td> 
  <td class="stentry"> <p>注釋字串（伺服器忽略）。</p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> cmdName</span> </span> </p></td> 
  <td class="stentry"> <p>支援的命令或屬性名之一。</p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> var</span> </span> </p> </td> 
  <td class="stentry"> <p>自訂變數的名稱。</p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 值</span> </span> </p></td> 
  <td class="stentry"> <p>命令或變數值。 </p></td> 
 </tr> 
</table>

*`server_address`*、 *`cmdName`*、 *`macro`*&#x200B;和 *`var`* 不區分大小寫。伺服器會保留所有其他字串值的大小寫。

*`value`* 是命令專用的，可由一或多個值組成，並以逗號分隔。有關詳細資訊，請參閱各個命令的說明。

## 伺服器標識符{#section-926ae55ddba14b8d952147a5fd701e14}

對於對影像伺服的所有HTTP請求，都需要[!DNL /is/image]根內容。

## HTTP解碼{#section-20922baccd804d2d986b44ce9a183a7d}

「影像伺服」會先從傳入的請求中擷取&#x200B;*`object`*&#x200B;和&#x200B;*`modifiers`*。 *`object`* 然後，將其分割為路徑元素，這些元素會個別HTTP解碼。將&#x200B;*`modifiers`*&#x200B;字串分隔為&#x200B;*`command`*= *`value`*&#x200B;對，然後在指令特定處理之前對&#x200B;*`value`*&#x200B;進行HTTP解碼。

>[!NOTE]
>
>除非說明檔案另有說明，否則所有不安全的字元都必須依HTTP標準進行編碼。 如需詳細資訊，請參閱HTTP規格。

## 備註 {#section-69ef0be0f17a418c87a0eba21c2ddb00}

注釋可以嵌入到任意位置的請求字串中，並由句點(.)識別 緊接在命令分隔符(&amp;)後面。 注釋由下次出現（未編碼）命令分隔符終止。 此功能可用來新增非影像伺服使用的要求資訊，例如時間戳記和資料庫ID。

## 另請參閱 {#section-d0b836568c31454b8dbeb136e6bbe0f0}

[資料類型](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/c-data-types.md#concept-49455c12df954bb5919cdd8d5ccc85fa), [HTTP/1.1規範](http://www.w3.org/Protocols/rfc2616/rfc2616.html)
