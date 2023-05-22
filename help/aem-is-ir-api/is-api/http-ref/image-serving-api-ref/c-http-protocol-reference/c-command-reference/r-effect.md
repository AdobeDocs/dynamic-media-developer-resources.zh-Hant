---
title: 影響
description: 選擇「效果層」(Effect Layer)。 在請求字串中選擇效果層並啟動與當前層關聯的新層段。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d1eaa38d-cfd3-44d4-92b1-04d72333f867
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 3%

---

# 影響{#effect}

選擇「效果層」(Effect Layer)。 在請求字串中選擇效果層並啟動與當前層關聯的新層段。

`effect= *`n`*`

<table id="simpletable_C48DABF486604D2B9F3CBC1CD01AC76D"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> n</span></span> </p> </td> 
  <td class="stentry"> <p>效果層號（int不等於0）。 </p></td> 
 </tr> 
</table>

新段內的所有命令都應用於指定的效果層。 效果層段由下一個 `layer=` 或 `effect=` 命令，或在請求結束時。

*`n`* 對於外層效果（即父層後面的效果），必須小於0；對於內層效果（即父層內的效果），必須大於0。 效果圖層編號不必是連續的。

如果同一父層存在多個效果層，則效果層編號指定z階。 編號較高的圖層放置在編號較低的圖層的頂部。

效果層可附連到 `layer=comp`。

## 屬性 {#section-e11f795deff345779ce280a82cf221ca}

效果圖層命令。 *`n`* 不能為0。

## 預設 {#section-84bbe1cfe7a94040827c994323ac59d4}

無。

## 範例 {#section-adf2fd8edb184803a2603d7b9a6db6da}

`…&layer=5&src=/myCat/myImage&size=200,200&effect=-1&$shadow$&…`

## 另請參閱 {#section-573273e9e0e64103a5764075f5e50180}

[層=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-layer.md)
