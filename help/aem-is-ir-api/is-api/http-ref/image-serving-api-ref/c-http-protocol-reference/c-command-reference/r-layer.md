---
description: 選擇「圖層」。 在命令序列中選取一個層並啟動新的層定義段。
seo-description: 選擇「圖層」。 在命令序列中選取一個層並啟動新的層定義段。
seo-title: 圖層
solution: Experience Manager
title: 圖層
topic: Scene7 Image Serving - Image Rendering API
uuid: 882309b3-51d7-477e-bd09-068ce9e55eb5
translation-type: tm+mt
source-git-commit: 87164dbf805a179f7bdeecd7cc6140c3456b61bb

---


# layer{#layer}

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

層段內的所有命令都應用於指定的層。 圖層區段會由下一個或 `layer=` 命令 `effect=` 或請求結尾終止。

指定 `layer=comp` 以選取複合影像（或為某些命令檢視）。

圖層編號有效地指定圖層的z順序。 編號較高的圖層會置於編號較低的圖層之上。

圖層編號不需要是連續的。 需要第0層。

可以為具有name命令變體的層指 `layer= *``*, *`定名`*` 稱。 定義命名圖層後，即可使用名稱 ` layer= *`引用`*`，而不需知道圖層編號。 可以使用多個name命令將多個名稱分配給同 `layer= *``*, *`一層`*` 。

>[!NOTE]
>
>圖層0會決定合成畫布的整體大小。 在構建複合時，會裁切掉落在圖層0邊界以外的所有圖層部分。

## 屬性 {#section-499963ee52c14f2898f0d0f90c1d01be}

圖層命令。 中不支援替代變數引用 `layer=`。

`comp` 不允許使用字 *`name`* 串。 如果相同的圖層指派給多 *`name`* 個圖層，或某個圖層參考先前未定義的圖層，則 *`name`* 會傳回錯誤。

## 預設 {#section-091859a03f8048c2b7092f0fec9c1006}

`layer=comp`. 如果是，許多命令和屬性會應用到第0層 `layer=comp`。

## 特殊案例 {#section-e087cb2e3562473e8d391abfa3b9489f}

* 如果相同名稱已映射至多個圖層(例如： `layer=1,image&layer=2,image`)，發生錯誤。
* 如果相同名稱多次映射至單一圖層(例如： `layer=1,image&layer=1,image`)，範圍會照常設定，不會出現錯誤。
* 支援同一層的多個名稱。

   任一名稱都可用來參照圖層(例如： `layer=1,image&layer=1,picture`)。
* 如果參考名稱從未映射到圖層編號(例如： `layer=1,image&layer=picture`)，發生錯誤。
* 圖層修飾元不支援替代變數(例如： `layer=$image$`)。

   這不僅適用於圖層名稱，也適用於一般的圖層修飾元。

* 所有合併和覆寫規則應與多個來源（請求、前置或後置修飾詞目錄記錄、巨集等）參考相同圖層時完全相同。

## 範例 {#section-cc40de6a0a754178aa752601539c815b}

請參閱範本中的 [範例](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)。
