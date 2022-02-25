---
title: ZoomView.transition
description: ZoomView.transition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 3ae12e0a-0647-4cb1-9785-c854b4586c47
source-git-commit: 7eddc50fb9803eacdd1f513c6132380793b6f88d
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 3%

---

# ZoomView.transition{#zoomview-transition}

` [ZoomView.|<containerId>_zoomView.]transition= *`時間`*[, *`寬`*]`

<table id="table_9E7BB12BF371419F88DD4D24EF04632C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 時間</span> </span> </p> </td> 
   <td colname="col2"> <p> 指定單個縮放步驟操作的動畫所花費的時間（秒）。 </p> </td> 
  </tr>
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 寬</span> </span> </p> </td> 
   <td colname="col2"> <p> 建立加速或減速的假象，使過渡更自然。 可以將緩動設定為以下選項之一： </p> <p> 
     <ul id="ul_DA0D1CF2F2484410BFCCACA86661702E"> 
      <li id="li_93A2D53A53314D9594CEDC9EB20381D4">0（自動） </li> 
      <li id="li_AD6A1F03DE544959BC4AA0DD97494F8C"> 1（線性） </li> 
      <li id="li_816A3CE796E3415B9650DDA204412A6A"> 2（二次） </li> 
      <li id="li_EF00BF6CA2AA48FEB54015FFBA9F8DD4"> 3（立方） </li> 
      <li id="li_F3CB7F0821AF489C84A0CA155F5031A2"> 4（四分） </li> 
      <li id="li_F5B844DAF4CC453CA58BF09A660D139F"> 5（五次） </li> 
     </ul> </p> <p>禁用彈性縮放時，自動模式始終使用線性過渡（預設）。 否則，它適合基於過渡時間的其它緩動功能之一。 即過渡時間越短，緩動函式用於加速加速或減速效果越大。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-50bcd15223174bb79ce08b31ea03d682}

選填。

## 預設 {#section-7564169749ff4a4996049ea1148cb2a5}

`0.5,0`

## 範例 {#section-96e69b70365f461dae4399e49044ea2f}

`transition=2,2`
