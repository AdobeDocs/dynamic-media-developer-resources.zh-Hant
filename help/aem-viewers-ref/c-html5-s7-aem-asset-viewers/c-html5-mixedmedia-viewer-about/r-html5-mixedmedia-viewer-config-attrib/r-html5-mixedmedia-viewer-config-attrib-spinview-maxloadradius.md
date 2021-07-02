---
description: 表示當SpinView空閒時要在每個方向上預載入的幀數上限。
solution: Experience Manager
title: SpinView.maxloadradius
feature: Dynamic Media Classic，檢視器，SDK/API，混合媒體集
role: Developer,Business Practitioner
exl-id: e64fcd95-9660-4c1f-91b2-3ffc5a7493ce
source-git-commit: bfb350e68d9b7e86cec5ee75fe9280b12ce0e54e
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 2%

---

# SpinView.maxloadradius{#spinview-maxloadradius}

表示當SpinView空閒時要在每個方向上預載入的幀數上限。

` [SpinView.|<containerId>_spinView.]maxloadradius= *``*[, *`valuehighRes`*]`

<table id="table_06BEA037FA82467CAA88D1CA62AE972E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> value</span></span> </p> </td> 
   <td colname="col2"> <p> 值<span class="codeph"> -1</span>預載入集中的所有幀。 預載入的幀始終以SpinView最初載入的原始解析度顯示。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> highRes</span></span> </p> </td> 
   <td colname="col2"> <p> 控制預載入幀的質量。 </p> <p>當設定為<span class="codeph"> 1</span>時，幀會以高質量載入，與元件的大小匹配。 </p> <p>當設為<span class="codeph"> 0</span>時，只會載入低解析度預覽圖磚。 </p> <p>以高解析度預先載入可改善一般使用者體驗，尤其是啟用自動回轉時。 同時，它會導致啟動時間較慢，網路消耗也較高，因此應謹慎使用。 當使用高解析度預載入時，預載入幀始終處於元件初始載入時的原始解析度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-65be9301796240e38f31818229da7acc}

選填。

## 預設 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`6,0`

## 範例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`maxloadradius=12,1`
