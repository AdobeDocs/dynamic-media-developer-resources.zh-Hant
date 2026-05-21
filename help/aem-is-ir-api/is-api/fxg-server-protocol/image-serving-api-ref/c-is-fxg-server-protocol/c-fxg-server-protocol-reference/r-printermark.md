---
description: 顯示印表機標籤。 指定如何顯示印表機標籤。
solution: Experience Manager
title: printerMark
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f61c7311-a2e9-4eb7-ae05-276a4eec980b
TQID: 'https://experienceleague.adobe.com/tit-a3stXGj0fZoMgi15lPIk-MtZSvUDOqlcayfNlwk'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 123
ht-degree: 24%

---

# printerMark{#printermark}

顯示印表機標籤。 指定如何顯示印表機標籤。

` printerMark= *`修剪標籤`*, *`出血標籤`*, *`註冊標籤`*, *`色條`*, *`頁面資訊`*, *`樣式`*, *`線寬`*, *`圖層內嵌`*`

可以關閉或開啟不同的標籤。 也可以控制印表機標籤的樣式。

以下是有效值：

<table id="simpletable_C84560940CAC46D8BE9D0EFEE5EBF323"> 
 <tr class="strow"> 
  <td class="stentry"> <p>修剪標籤= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>預設為 0。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>出血標籤= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>預設為 0。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>註冊標籤= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>預設為 0。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>色條= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>預設為 0。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>頁面資訊= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>預設為 0。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>style= </p></td> 
  <td class="stentry"> <p>預設 </p> <p>InDesignJ1 </p> <p>InDesignJ2 </p> <p>Illustrator </p> <p>IllustratorJ </p> <p>QuarkXPress </p> </td> 
  <td class="stentry"> <p>預設為預設 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>線條寬度= </p></td> 
  <td class="stentry"> <p>0.125 - 2.0範圍內的任何值，包括這兩個值。 </p></td> 
  <td class="stentry"> <p>預設值為0.25。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>圖層嵌入= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>預設值為1。 </p></td> 
 </tr> 
</table>

## 範例 {#section-d2e394ddabe14f4ea63af6dab233a163}

`&printerMark=1,1,1,1,1,Illustrator,.25,1`
