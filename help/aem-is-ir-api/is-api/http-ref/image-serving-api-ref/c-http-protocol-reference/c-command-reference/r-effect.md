---
description: 選擇「效果圖層」。 在請求字串中選取效果圖層，並啟動與目前圖層關聯的新圖層區段。
seo-description: 選擇「效果圖層」。 在請求字串中選取效果圖層，並啟動與目前圖層關聯的新圖層區段。
seo-title: 效果
solution: Experience Manager
title: 效果
topic: Scene7 Image Serving - Image Rendering API
uuid: 622dc7ca-55b8-4a82-b9a7-65588aee87d0
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# effect{#effect}

選擇「效果圖層」。 在請求字串中選取效果圖層，並啟動與目前圖層關聯的新圖層區段。

`effect= *`n`*`

<table id="simpletable_C48DABF486604D2B9F3CBC1CD01AC76D"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> n</span></span> </p> </td> 
  <td class="stentry"> <p>效果圖層編號（int不等於0）。 </p></td> 
 </tr> 
</table>

新段內的所有命令都會應用到指定的效果層。 效果層段由下一個或命 `layer=` 令或 `effect=` 請求結束終止。

*`n`* 對於外層效果（即父層後的效果）必須小於0，對於內層效果（即父層內的效果）則必須大於0。 效果圖層編號不必是連續的。

如果相同父層有多個效果圖層，效果圖層編號會指定z順序。 編號較高的圖層會置於編號較低的圖層之上。

效果層可以附著到 `layer=comp`。

## 屬性 {#section-e11f795deff345779ce280a82cf221ca}

效果圖層命令。 *`n`* 不得為0。

## 預設 {#section-84bbe1cfe7a94040827c994323ac59d4}

無。

## 範例 {#section-adf2fd8edb184803a2603d7b9a6db6da}

`…&layer=5&src=/myCat/myImage&size=200,200&effect=-1&$shadow$&…`

## 另請參閱 {#section-573273e9e0e64103a5764075f5e50180}

` [layer=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-layer.md#reference-0f8d7fbef64841dd855917bd8fc22e6d)`
