---
title: 簡介
description: 本檔案說明Dynamic Media影像轉譯的HTTP通訊協定。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c185e45b-a56c-4576-b05d-22cc0025a7c4
TQID: 'https://experienceleague.adobe.com/I21iWFmYP0Vwunf3evtnLAr3tslHOsTOB0sGWG6l-bc'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 387
ht-degree: 0%

---

# 簡介{#introduction}

本檔案說明Dynamic Media影像轉譯的HTTP通訊協定。

僅說明通訊協定的公開可用方面。 伺服器可支援保留供Dynamic Media使用者端軟體使用的其他命令。

**目標對象**

本檔案適用於有經驗的程式設計師和網站開發人員，協助他們將Dynamic Media影像演算用於網站或自訂應用程式。

假設讀者熟悉Dynamic Media影像製作和影像轉譯、一般HTTP通訊協定標準和慣例，以及基本影像術語。

**檔案慣例**

<table id="simpletable_E96BA470B3CE4266A9E6ED0440A56C40"> 
 <tr class="strow"> 
  <td class="stentry"> <p>常值 </p> </td> 
  <td class="stentry"> <p>在語法區段中，非斜體文字是常值；它不適用於空格和符號[ ] { } | *. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>'常值' </p> </td> 
  <td class="stentry"> <p>在描述性區段中，單引號中的非斜體文字是常值。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname">引數</span> </p> </td> 
  <td class="stentry"> <p>斜體表示變數或引數，以實際值取代。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph">屬性：：專案</span> </p> </td> 
  <td class="stentry"> <p>前置詞為'attribute：：'的名稱是指影像目錄屬性。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph">目錄：：專案</span> </p> </td> 
  <td class="stentry"> <p>前置詞為「catalog：：」的名稱是指材質目錄資料欄位。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> icc：：專案</span> </p> </td> 
  <td class="stentry"> <p>前置詞為「icc：：」的名稱是指ICC色彩設定檔地圖中的欄位。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph">巨集：：專案</span> </p> </td> 
  <td class="stentry"> <p>前置詞為'macro：：'的名稱是指巨集定義表格中的欄位。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph">規則集：：專案</span> </p> </td> 
  <td class="stentry"> <p>前置詞為「ruleset：：」的名稱是指URL前置處理規則集中的元素。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph">預設值：：專案</span> </p> </td> 
  <td class="stentry"> <p>前置詞為「default：：」的名稱是指預設影像目錄的屬性。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <span class="codeph">暈映：：專案</span> </td> 
  <td class="stentry"> <p>前置詞為「暈映：：」的名稱是指暈映對應中的欄位。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>[ <span class="varname">選用的</span> ] </p> </td> 
  <td class="stentry"> <p>選用的語法元素會以方括弧括住。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>*[ <span class="varname">選用的</span> ] </p> </td> 
  <td class="stentry"> <p>選用的語法元素可以重複無次或更多次。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname">專案1 </span>| <span class="varname">專案2 </span> </p> </td> 
  <td class="stentry"> <p>垂直列表示可以使用左邊的單一語法專案或右邊的專案。 只能選取一個專案。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>{ <span class="varname">群組</span> } </p> </td> 
  <td class="stentry"> <p>大括弧用於將語法元素分組。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>*{ <span class="varname">群組</span> } </p> </td> 
  <td class="stentry"> <p>群組內的語法元素可能會重複一次或多次。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>空格 </p> </td> 
  <td class="stentry"> <p>HTTP請求中不允許使用空白字元（空格或索引標籤）。 本檔案偶爾會在語法元素之間使用空白字元，目的僅為了清楚說明。 </p> </td> 
 </tr> 
</table>

**常用辭彙**

** *`MSS`* **材料規格區段：請求中兩個選取指令之間的材料屬性集。

** *`vignette`***在Dynamic Media影像製作中準備的影像，以搭配影像演算使用。
