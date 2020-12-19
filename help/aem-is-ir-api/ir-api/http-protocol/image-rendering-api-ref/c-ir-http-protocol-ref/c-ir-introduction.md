---
description: 本檔案說明用於Scene7影像演算的HTTP通訊協定。
seo-description: 本檔案說明用於Scene7影像演算的HTTP通訊協定。
seo-title: 簡介
solution: Experience Manager
title: 簡介
topic: Scene7 Image Serving - Image Rendering API
uuid: d709f1d2-e7cc-4e9f-b039-aa333e517cbb
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '389'
ht-degree: 2%

---


# 簡介{#introduction}

本檔案說明用於Scene7影像演算的HTTP通訊協定。

只描述了該協定的公開可用方面。 伺服器可能支援其他保留供Scene7用戶端軟體使用的命令。

**目標讀者**

本文說明的對象為想要將Scene7影像演算運用於網站或自訂應用程式的資深程式設計人員和網站開發人員。

假設讀者熟悉Scene7 Image Authoring和Image Rendering、一般HTTP通訊協定標準和慣例，以及基本的影像術語。

**檔案慣例**

<table id="simpletable_E96BA470B3CE4266A9E6ED0440A56C40"> 
 <tr class="strow"> 
  <td class="stentry"> <p>常值 </p> </td> 
  <td class="stentry"> <p>在語法部分中，非斜體文本是常值；這不適用於空白字元和符號[ ] { } | *. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>'literal' </p> </td> 
  <td class="stentry"> <p>在描述性章節中，單引號中的非斜體文字為常值。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 參數 </span> </p> </td> 
  <td class="stentry"> <p>斜體表示要用實際值替換的變數或參數。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 屬性：:Item  </span> </p> </td> 
  <td class="stentry"> <p>前置有'attribute::'的名稱是指影像目錄屬性。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 目錄：:Item  </span> </p> </td> 
  <td class="stentry"> <p>前置詞為「目錄：:」的名稱是指物料目錄資料欄位。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> icc::Item  </span> </p> </td> 
  <td class="stentry"> <p>前置詞為「icc::」的名稱是指ICC色彩描述檔映射中的欄位。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 宏：:Item  </span> </p> </td> 
  <td class="stentry"> <p>前置有'macro::'的名稱是指巨集定義表格中的欄位。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 規則集：：項目  </span> </p> </td> 
  <td class="stentry"> <p>前置「規則集：:」的名稱是指URL預處理規則集中的元素。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 預設值：:Item  </span> </p> </td> 
  <td class="stentry"> <p>前置詞為'default::'的名稱是指預設影像目錄的屬性。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <span class="codeph"> 暈映：:Item  </span> </td> 
  <td class="stentry"> <p>前置有「暈映：:」的名稱是指暈映地圖中的欄位。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>[ <span class="varname">可選</span> ] </p> </td> 
  <td class="stentry"> <p>選用的語法元素以方括弧括住。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>*[ <span class="varname">可選</span> ] </p> </td> 
  <td class="stentry"> <p>可選語法元素可重複無或多次。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> item1  </span>|  <span class="varname"> item2  </span> </p> </td> 
  <td class="stentry"> <p>垂直清單示可使用左側的單一語法項目，或右側的項目。 必須只選取一個項目。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>{ <span class="varname"> 群組 </span> } </p> </td> 
  <td class="stentry"> <p>大括弧用於對語法元素進行分組。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>*{ <span class="varname"> 群組 </span> } </p> </td> 
  <td class="stentry"> <p>組內的語法元素可重複一或多次。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>空白 </p> </td> 
  <td class="stentry"> <p>HTTP請求中不允許空格（空格或標籤）。 本檔案偶爾會在語法元素之間使用空格，僅能清楚說明。 </p> </td> 
 </tr> 
</table>

**常用詞語**

** *`MSS`* **材料規格部分：請求中兩個選擇命令之間的一組材料屬性。

** *`vignette`* **在Scene7影像製作中準備的影像，以搭配影像演算使用。
