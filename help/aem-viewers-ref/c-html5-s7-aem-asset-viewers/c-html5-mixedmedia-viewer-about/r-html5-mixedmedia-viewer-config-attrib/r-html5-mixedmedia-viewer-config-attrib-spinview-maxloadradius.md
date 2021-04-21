---
description: 表示當回轉視圖空閒時，要在每個方向上預載的幀數上限。
solution: Experience Manager
title: SpinView.maxloadradius
feature: Dynamic Media Classic,Viewers,SDK/API,Mix Media Sets
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 2%

---


# SpinView.maxloadradius{#spinview-maxloadradius}

表示當回轉視圖空閒時，要在每個方向上預載的幀數上限。

` [SpinView.|<containerId>_spinView.]maxloadradius= *``*[, *`valuehighRes`*]`

<table id="table_06BEA037FA82467CAA88D1CA62AE972E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 值</span></span> </p> </td> 
   <td colname="col2"> <p> 值<span class="codeph"> -1</span>預載集中的所有幀。 預先載入的影格一律以SpinView最初載入的原始解析度顯示。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> highRes</span></span> </p> </td> 
   <td colname="col2"> <p> 控制預先載入影格的品質。 </p> <p>設為<span class="codeph"> 1</span>時，畫格會以高品質載入，符合元件的大小。 </p> <p>當設為<span class="codeph"> 0</span>時，僅載入低解析度的預覽圖格。 </p> <p>以高解析度預載可改善使用者體驗，尤其是在啟用自動回轉時。 同時，它還導致啟動時間較慢，網路消耗較高，因此應謹慎使用。 當使用高解析度預載時，預載幀始終處於最初載入元件時的原始解析度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-65be9301796240e38f31818229da7acc}

選填。

## 預設 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`6,0`

## 範例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`maxloadradius=12,1`
