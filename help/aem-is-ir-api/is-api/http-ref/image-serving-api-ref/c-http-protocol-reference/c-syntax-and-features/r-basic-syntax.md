---
description: HTTP協定的基本語法如下所示。
solution: Experience Manager
title: Image Serving HTTP Protocol Basic語法
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ac75d6d0-a71e-45a0-89ee-b952a0202793
source-git-commit: 191d3e7cc4cd370e1e1b6ca5d7e27acd3ded7b6c
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 1%

---

# Image Serving HTTP Protocol Basic語法{#image-serving-http-protocol-basic-syntax}

HTTP協定的基本語法如下：

<table id="simpletable_854C20D4C42247B99D9F123543C17E7C"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 請求</span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="filepath">http://<span class="varname"> 伺服器</span>/is/image[/<span class="varname"> 對象</span>][?<span class="varname"> 修飾</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 伺服器 </span> </span> </p></td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 伺服器地址</span>[:<span class="varname"> 埠</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 對象</span> </span> </p></td> 
  <td class="stentry"> <p>源對象說明符（影像路徑或影像目錄條目）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 修飾</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 修飾</span>*[&amp;<span class="varname"> 修飾</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 修飾</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph">命令|{$<span class="varname"> 宏</span>$}|{<span class="varname"> 注釋</span>}</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 命令</span> </span> </p> </td> 
  <td class="stentry"> <p>{ 0}<span class="varname"> cmd名稱</span>|{$<span class="varname"> var</span>}[=<span class="varname"> 值</span>] </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 宏</span> </span> </p> </td> 
  <td class="stentry"> <p>命令宏的名稱。</p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 注釋</span> </span> </p></td> 
  <td class="stentry"> <p>注釋字串（被伺服器忽略）。</p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> cmd名稱</span> </span> </p></td> 
  <td class="stentry"> <p>支援的命令或屬性名稱之一。</p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> var</span> </span> </p> </td> 
  <td class="stentry"> <p>自定義變數的名稱。</p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 值</span> </span> </p></td> 
  <td class="stentry"> <p>命令或變數值。 </p></td> 
 </tr> 
</table>

*`server_address`*。 *`cmdName`*。 *`macro`*, *`var`* 不區分大小寫。 伺服器保留所有其他字串值的大小寫。

*`value`* 是命令特定的，可以由一個或多個值組成，這些值用逗號分隔。 有關詳細資訊，請參閱各個命令的說明。

## 伺服器標識符 {#section-926ae55ddba14b8d952147a5fd701e14}

的 [!DNL /is/image] 對Image Service的所有HTTP請求都需要根上下文。

## HTTP解碼 {#section-20922baccd804d2d986b44ce9a183a7d}

影像服務首先提取 *`object`* 和 *`modifiers`* 從傳入的請求。 *`object`* 然後將其分離成路徑元素，這些路徑元素被逐個HTTP解碼。 的 *`modifiers`* 字串分隔成 *`command`*= *`value`* 對，和 *`value`* 然後在命令特定處理之前對HTTP進行解碼。

>[!NOTE]
>
>除非文檔中另有說明，否則所有不安全字元必須按HTTP標準編碼。 有關詳細資訊，請參閱HTTP規範。

## 備註 {#section-69ef0be0f17a418c87a0eba21c2ddb00}

注釋可以嵌入到任何位置的請求字串中，並由句點(.)標識 緊跟在命令分隔符(&amp;)之後。 注釋由（未編碼）命令分隔符的下一次出現終止。 此功能可用於向不用於影像服務的請求添加資訊，如時間戳和資料庫ID。

## 另請參閱 {#section-d0b836568c31454b8dbeb136e6bbe0f0}

[資料類型](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/c-data-types.md#concept-49455c12df954bb5919cdd8d5ccc85fa)。 [HTTP/1.1規範](https://www.w3.org/Protocols/rfc2616/rfc2616.html)
