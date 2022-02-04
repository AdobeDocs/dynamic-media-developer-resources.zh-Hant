---
title: SpinView.maxloadradius
description: 表示SpinView空閒時在每個方向上要預載入的最大幀數。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: e64fcd95-9660-4c1f-91b2-3ffc5a7493ce
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 2%

---

# SpinView.maxloadradius{#spinview-maxloadradius}

表示SpinView空閒時在每個方向上要預載入的最大幀數。

` [SpinView.|<containerId>_spinView.]maxloadradius= *`值`*[, *`高Res`*]`

<table id="table_06BEA037FA82467CAA88D1CA62AE972E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 值</span></span> </p> </td> 
   <td colname="col2"> <p> 值 <span class="codeph"> -1</span> 預載集中的所有幀。 預載幀始終以SpinView最初載入的原始解析度顯示。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 高Res</span></span> </p> </td> 
   <td colname="col2"> <p> 控制預載幀的質量。 </p> <p>設定為時 <span class="codeph"> 1</span> 這些幀以高質量載入，與元件的大小相匹配。 </p> <p>設定為時 <span class="codeph"> 0</span> 只載入低解析度預覽平鋪。</p> <p>以高解析度預載入可改善用戶的體驗，特別是當啟用自動旋轉時。 同時，它會導致啟動時間較慢，網路消耗較高，因此應謹慎使用。 當使用高解析度預載時，預載幀始終處於初始載入元件時的原始解析度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-65be9301796240e38f31818229da7acc}

選填。

## 預設 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`6,0`

## 範例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`maxloadradius=12,1`
