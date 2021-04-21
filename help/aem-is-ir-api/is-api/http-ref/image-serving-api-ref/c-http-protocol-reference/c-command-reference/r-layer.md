---
description: 選擇「圖層」。 在命令序列中選取一個層並啟動新的層定義段。
solution: Experience Manager
title: 圖層
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '388'
ht-degree: 1%

---


# 層{#layer}

選擇「圖層」。 在命令序列中選取一個層並啟動新的層定義段。

`layer= *`名`*|comp[, *`稱`*]`

`layer= *`名稱`*`

<table id="simpletable_22DE3365A6454949B0D30C6D7110476E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> n</span></span> </p></td> 
  <td class="stentry"> <p>要選擇的層數（0或更大的int）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> comp</span> </p></td> 
  <td class="stentry"> <p>選取合成影像。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 名稱</span></span> </p></td> 
  <td class="stentry"> <p>圖層名稱. </p></td> 
 </tr> 
</table>

層段內的所有命令都應用於指定的層。 層段由下一個`layer=`或`effect=`命令或請求的結尾終止。

指定`layer=comp`以選取複合影像（或檢視，針對某些命令）。

圖層編號有效地指定圖層的z順序。 編號較高的圖層會置於編號較低的圖層之上。

圖層編號不需要是連續的。 需要第0層。

可以將名稱分配給具有`layer= *`n`*, *`name`*`命令變體的層。 定義命名層後，即可使用` layer= *`name`*`引用該層，而無需知道層號。 可使用多個`layer= *`n`*, *`name`*`命令將多個名稱分配給同一層。

>[!NOTE]
>
>圖層0會決定合成畫布的整體大小。 在構建複合時，會裁切掉落在圖層0邊界以外的所有圖層部分。

## 屬性 {#section-499963ee52c14f2898f0d0f90c1d01be}

圖層命令。 `layer=`不支援替代變數參考。

`comp` 不允許使用字 *`name`* 串。如果相同的&#x200B;*`name`*&#x200B;被指派給多個圖層，或者某個圖層被先前未定義的&#x200B;*`name`*&#x200B;參考，則會傳回錯誤。

## 預設 {#section-091859a03f8048c2b7092f0fec9c1006}

`layer=comp`. 如果`layer=comp`，則許多命令和屬性都適用於第0層。

## 特殊情況{#section-e087cb2e3562473e8d391abfa3b9489f}

* 如果相同名稱已映射至多個圖層(例如：`layer=1,image&layer=2,image`)，發生錯誤。
* 如果相同名稱多次映射至單一圖層(例如：`layer=1,image&layer=1,image`)，範圍設定如常，無錯誤。
* 支援同一層的多個名稱。

   任一名稱都可用來參照圖層(例如：`layer=1,image&layer=1,picture`)。
* 如果參考名稱從未映射到圖層編號(例如：`layer=1,image&layer=picture`)，發生錯誤。
* 圖層修飾元不支援替代變數(例如：`layer=$image$`)。

   這不僅適用於圖層名稱，也適用於一般的圖層修飾元。

* 所有合併和覆寫規則應與多個來源（請求、前置或後置修飾詞目錄記錄、巨集等）參考相同圖層時完全相同。

## 範例 {#section-cc40de6a0a754178aa752601539c815b}

請參閱[Templates](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)中的範例。
