---
description: 本檔案說明用於Dynamic Media影像轉譯的HTTP通訊協定。
solution: Experience Manager
title: 簡介
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c185e45b-a56c-4576-b05d-22cc0025a7c4
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '389'
ht-degree: 1%

---

# 簡介{#introduction}

本檔案說明用於Dynamic Media影像轉譯的HTTP通訊協定。

只描述了該協定的公開可用方面。 伺服器可支援保留供Dynamic Media客戶端軟體使用的其他命令。

**目標讀者**

本文記錄的對象為想要將Dynamic Media影像轉譯用於網站或自訂應用程式的資深程式設計師和網站開發人員。

假設讀者熟悉Dynamic Media影像製作和影像轉譯、一般HTTP通訊協定標準和慣例，以及基本影像術語。

**檔案慣例**

<table id="simpletable_E96BA470B3CE4266A9E6ED0440A56C40"> 
 <tr class="strow"> 
  <td class="stentry"> <p>常值 </p> </td> 
  <td class="stentry"> <p>在語法章節中，非斜體文字為常值；這不適用於空白字元和符號[ ] { } | *。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>'literal' </p> </td> 
  <td class="stentry"> <p>在描述性章節中，單引號中的非斜體文字為常值。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 參數 </span> </p> </td> 
  <td class="stentry"> <p>斜體表示要替換為實際值的變數或參數。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 屬性：:Item  </span> </p> </td> 
  <td class="stentry"> <p>前置詞為「attribute:：」的名稱代表影像目錄屬性。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 目錄：：項目  </span> </p> </td> 
  <td class="stentry"> <p>前置詞為「catalog:：」的名稱是指物料目錄資料欄位。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> icc:：項目  </span> </p> </td> 
  <td class="stentry"> <p>前置詞為「icc:：」的名稱是指ICC顏色配置檔案映射中的欄位。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 宏：：項目  </span> </p> </td> 
  <td class="stentry"> <p>前置詞為「macro:：」的名稱是指巨集定義表格中的欄位。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 規則集：：項目  </span> </p> </td> 
  <td class="stentry"> <p>前置詞為「ruleset:：」的名稱是指URL預先處理規則集中的元素。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 預設值：:Item  </span> </p> </td> 
  <td class="stentry"> <p>前置詞為「default::：」的名稱代表預設影像目錄的屬性。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <span class="codeph"> 暈映：：項目  </span> </td> 
  <td class="stentry"> <p>前置詞為「暈映：：」的名稱是指暈映地圖中的欄位。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>[ <span class="varname">可選</span> ] </p> </td> 
  <td class="stentry"> <p>可選語法元素以方括弧括住。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>*[ <span class="varname">可選</span> ] </p> </td> 
  <td class="stentry"> <p>可選語法元素可以無重複或多次。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> item1  </span>|  <span class="varname"> item2  </span> </p> </td> 
  <td class="stentry"> <p>垂直條指示左側的單一語法項目或右側的項目可以使用。 必須只選取一個項目。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>{ <span class="varname"> 群組 </span> } </p> </td> 
  <td class="stentry"> <p>大括弧用於分組語法元素。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>*{ <span class="varname"> 群組 </span> } </p> </td> 
  <td class="stentry"> <p>組內的語法元素可以重複一次或多次。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>空白 </p> </td> 
  <td class="stentry"> <p>HTTP要求中不允許使用空白字元（空格或索引標籤）。 本文檔偶爾會在語法元素之間使用空白字元，以便清晰明瞭。 </p> </td> 
 </tr> 
</table>

**常用詞語**

** *`MSS`* **物料規格段：請求中兩個選擇命令之間的一組材料屬性。

** *`vignette`* **在Dynamic Media影像製作中準備的影像，以便用於影像轉譯。
