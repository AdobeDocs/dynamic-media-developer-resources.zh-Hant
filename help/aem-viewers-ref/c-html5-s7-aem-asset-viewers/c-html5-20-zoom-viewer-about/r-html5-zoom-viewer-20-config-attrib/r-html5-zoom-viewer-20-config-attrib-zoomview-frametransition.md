---
description: 'null'
seo-description: 'null'
seo-title: ZoomView.frametransition
solution: Experience Manager
title: ZoomView.frametransition
topic: Dynamic media
uuid: 28e283ca-51d8-4d6c-9b8a-d16da21f4da1
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ZoomView.frametransition{#zoomview-frametransition}

` [ZoomView.|<containerId>_zoomView.]frametransition=none|fade|slide[, *`持續`*[, *`時間`*]`

<table id="table_D5992FCFF26046079089652B211BB6C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|fade|slide </span> </p> </td> 
   <td colname="col2"> <p>指定影格變更所套用之效果的類型。 <span class="codeph"> 「無 </span> 」代表沒有轉場；影格變更會立即發生。 <span class="codeph"> 淡化 </span> 意指舊影格和新影格之間的交叉淡化轉換。 <span class="codeph"> slide </span> 會啟動轉換，舊影格會從檢視中滑出，而新影格則會滑入。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 持續時間 </span></span> </p> </td> 
   <td colname="col2"> <p>指定淡化或投影片轉場效果 <span class="codeph"> 的持 </span> 續時 <span class="codeph"> 間(秒 </span> )。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 間距 </span></span> </p> </td> 
   <td colname="col2"> <p>在滑動過渡中，相鄰 <span class="codeph"> 幀之 </span> 間的間距為0到 <span class="codeph"> 1之間，並 </span><span class="codeph"></span> 且相對於元件寬度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-1e637b22e8a44d759d588e47576891e6}

選填。

## 預設 {#section-71fb773f814649b2885aefee68073641}

無。

## 範例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`frametransition=fade,1`
