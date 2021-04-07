---
description: 互動式視訊檢視器的設定屬性。
solution: Experience Manager
title: SocialShare.bearing
feature: Dynamic Media經典，檢視器，SDK/API，互動式視訊
role: 開發人員，商業從業人員
exl-id: f34d6954-01c5-49e0-94d4-fd577c57956e
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '198'
ht-degree: 2%

---

# SocialShare.bearing{#socialshare-bearing}

互動式視訊檢視器的設定屬性。

`[SocialShare.|<containerId>_socialShare.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> up|down|left|right|fit-vertical|fit-lateral</span> </p> </td> 
   <td colname="col2"> <p> 指定按鈕容器的投影片動畫方向。 當設定為<span class="codeph"> up</span>、<span class="codeph"> down</span>、<span class="codeph"> left</span>或<span class="codeph"> right</span>時，面板沿指定方向滾出，而不需進行任何額外的邊界檢查，這可能導致面板被外部容器夾住。 </p> <p>當設為<span class="codeph"> fit-vertical</span>時，元件會先將基板位置移至SocialShare的底部，並嘗試從此基本位置沿下列其中一個方向展開面板：下，右，左。 每次嘗試時，元件都會檢查面板是否被外部容器剪裁。 如果所有嘗試都失敗，元件會嘗試將基板位置移至頂端，並從頂端、右側和左側重複推出嘗試。 </p> <p>當設為<span class="codeph"> fit-lateral</span>時，元件會使用類似的邏輯，但會先將底座向右移動、向右移動、向下移動和向上移動方向。 然後，它將基座向左移動，嘗試左、下和上移方向。 </p> </td> 
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
