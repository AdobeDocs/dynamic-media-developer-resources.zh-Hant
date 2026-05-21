---
title: PageView.transition
description: PageView.transition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: aa12a210-88d9-4b96-b598-6967496ac668
TQID: 'https://experienceleague.adobe.com/zsCMR3hoGnEbFG1wapFyvB1oKROPcgP9yifLH-wtwPQ'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 107
ht-degree: 2%

---

# PageView.transition{#pageview-transition}

` [PageView.|<containerId>_pageView.]transition= *`時間`*[, *`加/減速`*]`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname">次</span></span> </p> </td> 
   <td colname="col2"> <p> 指定單一縮放步階動作動畫所需的時間（秒）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname">加/減速</span></span> </p> </td> 
   <td colname="col2"> <p> 建立加速或減速的幻覺，使轉接看起來更自然。 您可以將加/減速設定為下列其中一項： </p> <p> 
     <ul id="ul_DA0D1CF2F2484410BFCCACA86661702E"> 
      <li id="li_93A2D53A53314D9594CEDC9EB20381D4">0 （自動） </li> 
      <li id="li_AD6A1F03DE544959BC4AA0DD97494F8C"> 1 （線性） </li> 
      <li id="li_816A3CE796E3415B9650DDA204412A6A"> 2 （二次方） </li> 
      <li id="li_EF00BF6CA2AA48FEB54015FFBA9F8DD4"> 3 （立方） </li> 
      <li id="li_F3CB7F0821AF489C84A0CA155F5031A2"> 4 （四次方） </li> 
      <li id="li_F5B844DAF4CC453CA58BF09A660D139F"> 5 （五次方） </li> 
     </ul> </p> <p>當彈性縮放被停用（預設）時，「自動」模式一律使用線性轉換。 否則，它會根據轉接時間來配合其他加/減速功能之一。 也就是說，轉場時間越短，用於加速加速或減速效果的加/減速函式就越高。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-ebfd9162c8504666bf0e4485bf3b1383}

選擇性.

## 預設 {#section-9f91ce6567384ab691e4d4f8a7015455}

`0.5,0`

## 範例 {#section-cb6b8793ee9946b8bf1cfddab8612db5}

`transition=2,2`
