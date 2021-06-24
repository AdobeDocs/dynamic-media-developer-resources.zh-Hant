---
description: 互動式視訊檢視器的設定屬性。
solution: Experience Manager
title: SocialShare.bearing
feature: Dynamic Media Classic，檢視器， SDK/API，互動式影片
role: Developer,Business Practitioner
exl-id: f34d6954-01c5-49e0-94d4-fd577c57956e
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 2%

---

# SocialShare.bearing{#socialshare-bearing}

互動式視訊檢視器的設定屬性。

`[SocialShare.|<containerId>_socialShare.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 上|下|左|右|fit-vertical|fit-lateral</span> </p> </td> 
   <td colname="col2"> <p> 指定按鈕容器的幻燈片動畫方向。 當設定為<span class="codeph"> up</span>、<span class="codeph"> down</span>、<span class="codeph"> left</span>或<span class="codeph"> right</span>時，面板沿指定方向滾動，無需進行任何附加界限檢查，這可能導致面板被外部容器夾住。 </p> <p>當設定為<span class="codeph"> fit-vertical</span>時，元件首先將基板位置移到SocialShare的底部，並嘗試從這樣的基位置沿以下方向之一展開面板：下，右，左。 每次嘗試時，元件都會檢查面板是否被外部容器修剪。 如果所有嘗試都失敗，則元件會嘗試將基板位置移到頂部，並從上、右和左方向重複滾出嘗試。 </p> <p>當設為<span class="codeph"> fit-lateral</span>時，元件使用類似的邏輯，但會先將底座右移，向右、向下和向上移動方向。 然後，它將底座向左移動，嘗試左、下、上移方向。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-1e637b22e8a44d759d588e47576891e6}

選填。

## 預設 {#section-71fb773f814649b2885aefee68073641}

`fit-vertical`

## 範例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
bearing=left
```
