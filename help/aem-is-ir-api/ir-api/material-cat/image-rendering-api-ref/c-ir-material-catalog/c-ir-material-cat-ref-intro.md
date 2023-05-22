---
description: 本文檔介紹Dynamic Media影像渲染的材料目錄。
solution: Experience Manager
title: 簡介
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1cdb9c45-329d-44df-92c3-8cba5b2b1339
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '328'
ht-degree: 2%

---

# 簡介{#introduction}

本文檔介紹Dynamic Media影像渲染的材料目錄。

**目標讀者**

本文檔針對的是希望將Dynamic Media影像渲染用於網站或自定義應用程式的經驗豐富的程式設計師和網站開發人員。

假定讀者熟悉Dynamic Media影像創作和影像渲染、一般HTTP協定標準和慣例以及基本的影像術語。

**文檔約定**

<table id="simpletable_E96BA470B3CE4266A9E6ED0440A56C40"> 
 <tr class="strow"> 
  <td class="stentry"> <p>文字 </p> </td> 
  <td class="stentry"> <p>在語法部分中，非斜體文本為文本；這不適用於空格和符號[ ] { } | *。 </p> </td> 
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
  <td class="stentry"> <span class="codeph"> 目錄：：物料 </span> </td> 
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
  <td class="stentry"> <p> <span class="codeph"> vignette::Item </span> </p> </td> 
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
  <td class="stentry"> <p>空白。 </p> </td> 
  <td class="stentry"> <p>HTTP請求中不允許使用空格（空格或制表符）。 本文檔偶爾會在語法元素之間使用空格，僅用於清晰。 </p> </td> 
 </tr> 
</table>
