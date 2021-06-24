---
description: 選擇「圖層」。 選擇一個層，並在命令序列中啟動新的層定義段。
solution: Experience Manager
title: 層
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: f1200d86-d88c-4990-ae36-2ce96ae94343
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '385'
ht-degree: 1%

---

# 層{#layer}

選擇「圖層」。 選擇一個層，並在命令序列中啟動新的層定義段。

`layer= *``*|comp[, *`name`*]`

`layer= *`名稱`*`

<table id="simpletable_22DE3365A6454949B0D30C6D7110476E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> n</span></span> </p></td> 
  <td class="stentry"> <p>要選取的層數（0個或更大整數）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> comp</span> </p></td> 
  <td class="stentry"> <p>選取複合影像。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 名稱</span></span> </p></td> 
  <td class="stentry"> <p>圖層名稱. </p></td> 
 </tr> 
</table>

層段內的所有命令都應用到指定的層。 層段由下一個`layer=`或`effect=`命令或請求的結尾終止。

指定`layer=comp`以選擇複合影像（或查看某些命令）。

圖層編號有效地指定圖層的z階。 編號較高的圖層放置在編號較低的圖層上。

層號不需要連續。 需要0層。

可以為具有`layer= *`n`*, *`name`*`命令變體的層分配名稱。 定義命名層後，即可以` layer= *`name`*`引用該層，無需知道層號。 可使用多個`layer= *`n`*, *`name`*`命令將多個名稱分配給同一層。

>[!NOTE]
>
>第0層決定複合畫布的整體大小。 在構建複合材料時，脫落到層0界限之外的所有層的部分都會被截斷。

## 屬性 {#section-499963ee52c14f2898f0d0f90c1d01be}

圖層命令。 `layer=`中不支援替代變數引用。

`comp` 不允許設為字 *`name`* 串。如果將相同的&#x200B;*`name`*&#x200B;指派給多個層，或如果某個層被先前未定義的&#x200B;*`name`*&#x200B;引用，則返回錯誤。

## 預設 {#section-091859a03f8048c2b7092f0fec9c1006}

`layer=comp`. 如果`layer=comp`，則許多命令和屬性都適用於0層。

## 特殊案例 {#section-e087cb2e3562473e8d391abfa3b9489f}

* 如果同一名稱映射到多個層(例如：`layer=1,image&layer=2,image`)，發生錯誤。
* 如果同一名稱多次對應至單一層(例如：`layer=1,image&layer=1,image`)，則範圍設定如常，且無錯誤。
* 支援同一層的多個名稱。

   任一名稱都可用於參照圖層(例如：`layer=1,image&layer=1,picture`)。
* 如果引用的名稱從未映射到層號(例如：`layer=1,image&layer=picture`)，發生錯誤。
* 層修飾元中不支援替代變數(例如：`layer=$image$`)。

   這適用於所有排列，不僅適用於層名稱，而且適用於一般的層修飾符。

* 所有合併和覆寫規則應與多個來源參照相同層時（請求、前置或後置修飾詞目錄記錄、巨集等）完全相同。

## 範例 {#section-cc40de6a0a754178aa752601539c815b}

請參閱[範本](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)中的範例。
