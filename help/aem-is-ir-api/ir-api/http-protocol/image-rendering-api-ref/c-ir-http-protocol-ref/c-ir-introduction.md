---
title: 簡介
description: 本文檔介紹用於Dynamic Media影像呈現的HTTP協定。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c185e45b-a56c-4576-b05d-22cc0025a7c4
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '384'
ht-degree: 1%

---

# 簡介{#introduction}

本文檔介紹用於Dynamic Media影像呈現的HTTP協定。

只描述了該協定的公開可用方面。 伺服器可支援保留供Dynamic Media客戶端軟體使用的附加命令。

**目標讀者**

本文檔面向希望將Dynamic Media影像渲染用於網站或自定義應用程式的經驗豐富的程式設計師和網站開發人員。

假定讀者熟悉Dynamic Media影像創作和影像渲染、一般HTTP協定標準和慣例以及基本的影像術語。

**文檔約定**

<table id="simpletable_E96BA470B3CE4266A9E6ED0440A56C40"> 
 <tr class="strow"> 
  <td class="stentry"> <p>文字 </p> </td> 
  <td class="stentry"> <p>在語法部分中，非斜體文本為文本；它不適用於空格和符號[ ] { } | *。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>「literal」 </p> </td> 
  <td class="stentry"> <p>在描述性部分中，單引號中的非斜體文本為文本。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 參數 </span> </p> </td> 
  <td class="stentry"> <p>斜體表示要用實際值替換的變數或參數。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 屬性：:Item </span> </p> </td> 
  <td class="stentry"> <p>前置詞為「attribute:：」的名稱是指影像目錄屬性。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 目錄：：物料 </span> </p> </td> 
  <td class="stentry"> <p>前置詞為「catalog:：」的名稱是指物料目錄資料欄位。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> icc:：項 </span> </p> </td> 
  <td class="stentry"> <p>前置詞為「icc:：」的名稱是指ICC顏色配置檔案映射中的欄位。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 宏：：項 </span> </p> </td> 
  <td class="stentry"> <p>前置詞為「macro:：」的名稱是指宏定義表中的欄位。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 規則集：：項 </span> </p> </td> 
  <td class="stentry"> <p>前置詞為「ruleset:：」的名稱指URL預處理規則集中的元素。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 預設值：：項 </span> </p> </td> 
  <td class="stentry"> <p>前置詞為「default:：」的名稱是指預設影像目錄的屬性。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <span class="codeph"> vignette::Item </span> </td> 
  <td class="stentry"> <p>前置詞為「vignette:：」的名稱是指vignette映射中的欄位。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>[ <span class="varname"> 可選 </span> ] </p> </td> 
  <td class="stentry"> <p>可選語法元素由方括弧括起來。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>*[ <span class="varname"> 可選 </span> ] </p> </td> 
  <td class="stentry"> <p>可選語法元素可重複無或多次。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 物料1 </span>| <span class="varname"> 物料2 </span> </p> </td> 
  <td class="stentry"> <p>竪條表示可以使用左側的單個語法項或右側的項。 必須只選擇一個項。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>{ <span class="varname"> 群組 </span> } </p> </td> 
  <td class="stentry"> <p>大括弧用於對語法元素進行分組。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>*{ <span class="varname"> 群組 </span> } </p> </td> 
  <td class="stentry"> <p>組內的語法元素可以重複一次或多次。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>白空間 </p> </td> 
  <td class="stentry"> <p>HTTP請求中不允許使用空格（空格或制表符）。 本文檔偶爾會在語法元素之間使用空格，僅用於清晰。 </p> </td> 
 </tr> 
</table>

**常用術語**

** *`MSS`* **物料規格段：請求中兩個選擇命令之間的一組材料屬性。

** *`vignette`* **在Dynamic Media影像創作中準備的用於影像渲染的影像。
