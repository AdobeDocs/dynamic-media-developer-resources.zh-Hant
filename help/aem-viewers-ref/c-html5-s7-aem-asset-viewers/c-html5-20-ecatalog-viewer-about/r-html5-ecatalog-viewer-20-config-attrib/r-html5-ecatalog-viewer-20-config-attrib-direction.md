---
title: 方向
description: 指定頁面在主檢視和縮圖中的顯示方式。 它也會指定使用者與檢視器使用者介面的互動方式，以在目錄框架之間變更。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: d7d3df37-3e8b-438f-8b24-035b6982dc14
TQID: 'https://experienceleague.adobe.com/uP4fUmV4KEFWLzfhN-68CZexuApogdpf2MxIPd12FNs'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 232
ht-degree: 2%

---

# 方向{#direction}

`direction=auto|left|right`

<table id="table_1D425B7685D448459CD3FE8D683C813C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">自動|靠左|靠右</span> </p> </td> 
   <td colname="col2"> <p>指定頁面在主檢視和縮圖中的顯示方式。 它也會指定使用者與檢視器使用者介面的互動方式，以在目錄框架之間變更。 </p> <p>使用<span class="codeph">左側</span>時，它會設定初始頁面的右對齊方式，以及最後一頁的左對齊方式。 它會以由左至右的呈現順序來拼接個別頁面子影像。 它也會設定主檢視，以使用由右至左的投影片動畫來推進目錄（如果<span class="codeph"> PageView.frametransition </span>設定為投影片）。 最後，縮圖會設定為由左至右的填入順序。 </p> <p>同樣地，使用<span class="codeph">右</span>時，它會設定初始頁面的左對齊方式，以及最後一頁的右對齊方式。 它會以由右至左的轉譯順序來拼接個別頁面子影像。 它也會設定主檢視，以使用由左至右的投影片動畫來推進目錄（如果<span class="codeph"> PageView.frametransition </span>設定為投影片）。 最後，這會反轉縮圖順序，讓縮圖檢視以由右至左、由上到下的方向填入。 </p> <p>設定<span class="codeph">自動</span>時，當地區設定設為<span class="codeph"> ja時，檢視器套用<span class="codeph">右</span>模式；</span>否則，它使用<span class="codeph">左</span>模式。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-a66ce10d6c0b449883f654e7e0657e2c}

選擇性.

## 預設 {#section-2879062cee1d4030b43ba3b19693f4f8}

`auto`

## 範例 {#section-798e4fc8dd9b4b059171b41a608a96ce}

`direction=right`
