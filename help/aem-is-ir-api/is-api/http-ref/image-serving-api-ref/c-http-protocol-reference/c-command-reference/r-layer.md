---
title: 層
description: 選擇「圖層」。 在命令序列中選取一個圖層並啟動一個新的圖層定義段。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f1200d86-d88c-4990-ae36-2ce96ae94343
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '380'
ht-degree: 1%

---

# 層{#layer}

選擇「圖層」。 在命令序列中選取一個圖層並啟動一個新的圖層定義段。

`layer= *`n`*|comp[, *`名稱`*]`

`layer= *`名稱`*`

<table id="simpletable_22DE3365A6454949B0D30C6D7110476E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> n</span></span> </p></td> 
  <td class="stentry"> <p>要選擇的層數（0或更大的int）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> 元件</span> </p></td> 
  <td class="stentry"> <p>選擇複合影像。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 名稱</span></span> </p></td> 
  <td class="stentry"> <p>圖層名稱. </p></td> 
 </tr> 
</table>

層段內的所有命令都應用於指定的層。 層段由下一個 `layer=` 或 `effect=` 命令或請求的結尾。

指定 `layer=comp` 的子菜單。

層號有效地指定層的z階。 編號較高的圖層放置在編號較低的圖層的頂部。

層號不必是連續的。 第0層是必填項。

可以將名稱分配給具有 `layer= *`n`*, *`名稱`*` 命令變數。 定義命名層後，可以使用 ` layer= *`名稱`*`，不需要知道層號。 可以使用多個名稱為同一層分配多個名稱 `layer= *`n`*, *`名稱`*` 的雙曲餘切值。

>[!NOTE]
>
>第0層確定合成畫布的總體大小。 在構建複合材料時，將裁剪掉位於層0邊界之外的所有層。

## 屬性 {#section-499963ee52c14f2898f0d0f90c1d01be}

層命令。 中不支援替代變數引用 `layer=`。

`comp` 不允許作為 *`name`* 的下界。 如果相同，則返回錯誤 *`name`* 指定給多個層，或者如果某個層由 *`name`* 之前沒有定義過。

## 預設 {#section-091859a03f8048c2b7092f0fec9c1006}

`layer=comp`. 如果 `layer=comp`。

## 特殊案例 {#section-e087cb2e3562473e8d391abfa3b9489f}

* 如果同一名稱映射到多個層(例如： `layer=1,image&layer=2,image`)，出現錯誤。
* 如果同一名稱多次映射到單個層(例如： `layer=1,image&layer=1,image`)，範圍設定為正常，無錯誤。
* 支援同一層的多個名稱。

   任一名稱都可用於引用層(例如： `layer=1,image&layer=1,picture`)。
* 如果引用的名稱從未映射到層號(例如： `layer=1,image&layer=picture`)，出現錯誤。
* 層修飾符中不支援替代變數(例如： `layer=$image$`)。

   這適用於所有排列，不僅適用於圖層名稱，而且適用於一般的圖層修飾符。

* 所有合併和覆蓋規則應與在多個源（請求、前或後修飾符目錄記錄、宏等）中引用同一層時完全一樣。

## 範例 {#section-cc40de6a0a754178aa752601539c815b}

請參閱中的示例 [模板](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)。
