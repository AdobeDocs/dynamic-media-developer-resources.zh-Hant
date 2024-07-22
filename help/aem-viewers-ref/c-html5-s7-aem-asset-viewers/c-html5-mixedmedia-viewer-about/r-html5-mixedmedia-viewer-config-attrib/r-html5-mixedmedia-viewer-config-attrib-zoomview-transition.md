---
title: ZoomView.transition
description: ZoomView.transition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: bb00a1c9-aa6f-428f-8d57-241ee1efa082
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 2%

---

# ZoomView.transition{#zoomview-transition}

` [ZoomView.|<containerId>_zoomView.]transition= *`時間`*[, *`加/減速`*]`

<table id="table_9E7BB12BF371419F88DD4D24EF04632C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname">次</span></span> </p> </td> 
   <td colname="col2"> <p> 指定單一縮放步階動作動畫所需的時間（秒）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname">加/減速</span></span> </p> </td> 
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

## 屬性 {#section-65be9301796240e38f31818229da7acc}

選擇性.

## 預設 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0.5,0`

## 範例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`transition=2,2`
