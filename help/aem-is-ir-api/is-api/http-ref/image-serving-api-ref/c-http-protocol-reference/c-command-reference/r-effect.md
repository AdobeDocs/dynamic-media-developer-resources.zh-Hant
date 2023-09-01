---
title: 效果
description: 選取「效果圖層」。 選取效果圖層，並在要求字串中開始新的圖層區段（與目前圖層關聯）。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d1eaa38d-cfd3-44d4-92b1-04d72333f867
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 3%

---

# 效果{#effect}

選取「效果圖層」。 選取效果圖層，並在要求字串中開始新的圖層區段（與目前圖層關聯）。

`effect= *`n`*`

<table id="simpletable_C48DABF486604D2B9F3CBC1CD01AC76D"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> n</span></span> </p> </td> 
  <td class="stentry"> <p>效果圖層編號（int不等於0）。 </p></td> 
 </tr> 
</table>

新區段內的所有指令都會套用到指定的效果圖層。 效果圖層區段由下一個終止 `layer=` 或 `effect=` 命令或在要求結尾之前。

值 *`n`* 外部圖層效果（也就是父圖層後面的效果）必須小於0，而內部圖層效果（也就是父圖層內的效果）必須大於0。 效果圖層編號不一定要連續。

如果相同父圖層有多個效果圖層，則效果圖層編號會指定z順序。 編號較高的圖層會放置在編號較低的圖層上。

效果圖層可以附加至 `layer=comp`.

## 屬性 {#section-e11f795deff345779ce280a82cf221ca}

效果圖層指令。 值 *`n`* 不得為0。

## 預設 {#section-84bbe1cfe7a94040827c994323ac59d4}

無。

## 範例 {#section-adf2fd8edb184803a2603d7b9a6db6da}

`…&layer=5&src=/myCat/myImage&size=200,200&effect=-1&$shadow$&…`

## 另請參閱 {#section-573273e9e0e64103a5764075f5e50180}

[layer=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-layer.md)
