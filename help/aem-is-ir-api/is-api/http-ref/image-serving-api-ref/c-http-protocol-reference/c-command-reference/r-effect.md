---
description: 選擇「效果層」。 在請求字串中選取效果層並啟動與目前層相關聯的新層區段。
solution: Experience Manager
title: 效果
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: d1eaa38d-cfd3-44d4-92b1-04d72333f867
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 3%

---

# 效果{#effect}

選擇「效果層」。 在請求字串中選取效果層並啟動與目前層相關聯的新層區段。

`effect= *`n`*`

<table id="simpletable_C48DABF486604D2B9F3CBC1CD01AC76D"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> n</span></span> </p> </td> 
  <td class="stentry"> <p>效果層號（int不等於0）。 </p></td> 
 </tr> 
</table>

新段內的所有命令都將應用到指定的效果層。 效果層段由下一個`layer=`或`effect=`命令終止，或由請求結束終止。

*`n`* 對於外層效果（即父層後的效果），必須小於0，對於內層效果（即父層內的效果），則必須大於0。效果層數不必是連續的。

如果同一父層的多個效果層，則效果層號指定z順序。 編號較高的圖層放置在編號較低的圖層上。

效果層可附加到`layer=comp`。

## 屬性 {#section-e11f795deff345779ce280a82cf221ca}

效果層命令。 *`n`* 不得為0。

## 預設 {#section-84bbe1cfe7a94040827c994323ac59d4}

無。

## 範例 {#section-adf2fd8edb184803a2603d7b9a6db6da}

`…&layer=5&src=/myCat/myImage&size=200,200&effect=-1&$shadow$&…`

## 另請參閱 {#section-573273e9e0e64103a5764075f5e50180}

` [layer=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-layer.md#reference-0f8d7fbef64841dd855917bd8fc22e6d)`
