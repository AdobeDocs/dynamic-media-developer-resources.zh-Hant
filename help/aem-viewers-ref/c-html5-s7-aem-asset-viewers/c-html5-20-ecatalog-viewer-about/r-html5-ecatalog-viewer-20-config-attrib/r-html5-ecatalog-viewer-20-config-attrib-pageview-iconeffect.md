---
title: PageView.iconEffect
description: PageView.iconEffect
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: cdd96e58-d805-47d6-bf26-9ebd90afd535
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 5%

---

# PageView.iconEffect{#pageview-iconeffect}

` [PageView.|<containerId>_pageView.]iconeffect=0|1[, *`計數`*][, *`淡出`*][, *`autoHide`*]`

<table id="table_DD66FFC263A34220876DD204BFE62D49"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> 啟用 <span class="codeph"> 像效</span> 當影像處於重設狀態時，顯示在影像的頂端，並提示可與影像互動的可用動作。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 計數</span></span> </p> </td> 
   <td colname="col2"> <p> 指定 <span class="codeph"> 像效</span> 出現並重新出現。 值 <span class="codeph"> -1</span> 指出圖示一律會無限期地重新顯示。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 淡出</span></span> </p> </td> 
   <td colname="col2"> <p>指定顯示或隱藏動畫的持續時間（以秒為單位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> autoHide</span></span> </p> </td> 
   <td colname="col2"> <p>設定 <span class="codeph"> 像效</span> 在自動隱藏前保持完全可見。 即，淡出動畫完成之後、淡出動畫開始之前的時間。 設定 <span class="codeph"> 0</span> 停用自動隱藏行為。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-b6e5e52698d4492f9d6350e7e312bb1b}

選填。

## 預設 {#section-7d0fc8fa09b34c288ed32ef7faa84604}

`1,1,0.3,3`

## 範例 {#section-95db1bfcccf241089654363203b19977}

`iconeffect=0`
