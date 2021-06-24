---
description: HTTP協定基本語法如下。
solution: Experience Manager
title: 影像伺服HTTP通訊協定基本語法
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: ac75d6d0-a71e-45a0-89ee-b952a0202793
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '275'
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
  <td class="stentry"> <p>源對象說明符（影像路徑或影像目錄條目）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 修飾符</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 修飾詞</span>*[&amp;<span class="varname"> modifier</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 修飾詞</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph">命令|{$<span class="varname"> macro</span>$}|{。<span class="varname"> comment</span>}</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 命令</span> </span> </p> </td> 
  <td class="stentry"> <p>{<span class="varname"> cmdName</span>|{$<span class="varname"> var</span>}}[=<span class="varname"> value</span>] </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 宏</span> </span> </p> </td> 
  <td class="stentry"> <p>命令宏的名稱。</p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 註解</span> </span> </p></td> 
  <td class="stentry"> <p>注釋字串（由伺服器忽略）。</p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> cmdName</span> </span> </p></td> 
  <td class="stentry"> <p>支援的命令或屬性名稱之一。</p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> var</span> </span> </p> </td> 
  <td class="stentry"> <p>自訂變數的名稱。</p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> value</span> </span> </p></td> 
  <td class="stentry"> <p>命令或變數值。 </p></td> 
 </tr> 
</table>

*`server_address`*、  *`cmdName`*、  *`macro`*&#x200B;和 *`var`* 不區分大小寫。伺服器會保留所有其他字串值的大小寫。

*`value`* 是命令專屬的，可由一或多個值組成（以逗號分隔）。有關詳細資訊，請參閱各個命令的說明。

## 伺服器識別碼 {#section-926ae55ddba14b8d952147a5fd701e14}

所有對影像伺服的HTTP請求都需要[!DNL /is/image]根內容。

## HTTP解碼 {#section-20922baccd804d2d986b44ce9a183a7d}

影像伺服器會先從傳入的請求中擷取&#x200B;*`object`*&#x200B;和&#x200B;*`modifiers`*。 *`object`* 然後被分離為路徑元素，這些路徑元素被單獨HTTP解碼。將&#x200B;*`modifiers`*&#x200B;字串分為&#x200B;*`command`*= *`value`*&#x200B;對，然後在命令特定處理之前對&#x200B;*`value`*&#x200B;進行HTTP解碼。

>[!NOTE]
>
>除非檔案中另有說明，否則所有不安全字元都必須按照HTTP標準編碼。 如需詳細資訊，請參閱HTTP規格。

## 備註 {#section-69ef0be0f17a418c87a0eba21c2ddb00}

註解可隨處內嵌至要求字串，並以句點(.)識別 緊接在命令分隔符(&amp;)後面。 注釋由下次出現（未編碼）命令分隔符終止。 此功能可用來將資訊新增至非影像伺服使用的請求，例如時間戳記和資料庫ID。

## 另請參閱 {#section-d0b836568c31454b8dbeb136e6bbe0f0}

[資料類型](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/c-data-types.md#concept-49455c12df954bb5919cdd8d5ccc85fa), [HTTP/1.1規範](http://www.w3.org/Protocols/rfc2616/rfc2616.html)
