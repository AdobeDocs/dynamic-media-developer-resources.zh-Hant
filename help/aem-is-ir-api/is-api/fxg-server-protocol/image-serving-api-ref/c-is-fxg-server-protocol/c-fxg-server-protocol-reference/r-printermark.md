---
description: 顯示打印機標籤。 指定如何顯示打印機標籤。
solution: Experience Manager
title: printerMark
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 30%

---


# printerMark{#printermark}

顯示打印機標籤。 指定如何顯示打印機標籤。

` printerMark= *`修剪標`*, *`記出`*, *`血標籤注`*, *`冊標籤顏`*, *`色標籤信`*, *``*, *`息樣式線`*, *`加權圖嵌入`*`

可以關閉或開啟不同的標籤。 還可以控制打印機標籤的樣式。

以下是有效值：

<table id="simpletable_C84560940CAC46D8BE9D0EFEE5EBF323"> 
 <tr class="strow"> 
  <td class="stentry"> <p>trim marks= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>預設為 0。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>bleed marks= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>預設為 0。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>registration marks= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>預設為 0。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>color bars= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>預設為 0。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>page information= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>預設為 0。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>style= </p></td> 
  <td class="stentry"> <p>預設 </p> <p>InDesignJ1 </p> <p>InDesignJ2 </p> <p>Illustrator </p> <p>IllustratorJ </p> <p>QuarkXPress </p> </td> 
  <td class="stentry"> <p>預設為預設 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>線重= </p></td> 
  <td class="stentry"> <p>0.125 - 2.0範圍內的任何值，包括兩個值。 </p></td> 
  <td class="stentry"> <p>預設為 0.25。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>layer embed= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>預設為 1。 </p></td> 
 </tr> 
</table>

## 範例 {#section-d2e394ddabe14f4ea63af6dab233a163}

`&printerMark=1,1,1,1,1,Illustrator,.25,1`
