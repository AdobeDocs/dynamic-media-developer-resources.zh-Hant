---
title: 圖層
description: 選取圖層。 選取圖層並在指令序列中開始新的圖層定義區段。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f1200d86-d88c-4990-ae36-2ce96ae94343
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '387'
ht-degree: 0%

---

# 圖層{#layer}

選取圖層。 選取圖層並在指令序列中開始新的圖層定義區段。

`layer= *`n`*|comp[, *`名稱`*]`

`layer= *`名稱`*`

<table id="simpletable_22DE3365A6454949B0D30C6D7110476E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> n</span></span> </p></td> 
  <td class="stentry"> <p>要選取的圖層數目（0或大於int）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">元件</span> </p></td> 
  <td class="stentry"> <p>選取複合影像。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname">名稱</span></span> </p></td> 
  <td class="stentry"> <p>圖層名稱。 </p></td> 
 </tr> 
</table>

圖層區段內的所有指令都會套用到指定的圖層。 下一個`layer=`或`effect=`命令或要求的結尾會終止圖層區段。

指定`layer=comp`以選取複合影像（或某些命令的檢視）。

圖層編號會有效地指定圖層的z順序。 編號較高的圖層會放置在編號較低的圖層上。

圖層編號不需要連續。 需要圖層0。

可以將名稱指派給具有`layer= *`n`*, *`name`*`命令變體的圖層。 定義已命名的圖層後，可透過` layer= *`名稱`*`加以參照，而不需要知道圖層編號。 可以使用多個`layer= *`n`*, *`name`*`命令，將多個名稱指派給相同的圖層。

>[!NOTE]
>
>圖層0決定合成畫布的整體大小。 建立複合時，落在圖層0邊界以外的所有圖層部分都會被裁切。

## 屬性 {#section-499963ee52c14f2898f0d0f90c1d01be}

圖層指令。 `layer=`不支援替代變數參考。

不允許`comp`做為&#x200B;*`name`*&#x200B;字串。 如果將相同的&#x200B;*`name`*&#x200B;指派給一個以上的圖層，或某圖層由&#x200B;*`name`*&#x200B;所參照，而先前尚未定義該圖層，則會傳回錯誤。

## 預設 {#section-091859a03f8048c2b7092f0fec9c1006}

`layer=comp`。 如果`layer=comp`，許多命令和屬性會套用至圖層0。

## 特殊案例 {#section-e087cb2e3562473e8d391abfa3b9489f}

* 如果相同的名稱對應到多個圖層（例如： `layer=1,image&layer=2,image`），就會發生錯誤。
* 如果相同名稱多次對應至單一圖層（例如： `layer=1,image&layer=1,image`），則範圍會如常設定，不會發生錯誤。
* 支援相同圖層的多個名稱。

  任一名稱都可以用來參考圖層（例如： `layer=1,image&layer=1,picture`）。
* 如果參照的名稱從未對應到圖層編號（例如： `layer=1,image&layer=picture`），則會發生錯誤。
* 圖層修飾元中不支援替代變數（例如： `layer=$image$`）。

  這適用於所有排列，不僅適用於圖層名稱，而且適用於一般的圖層修飾元。

* 所有合併和覆寫規則的運作方式，應與在多個來源（請求、前置或後置修飾元目錄記錄、巨集等）中參考相同圖層時完全相同。

## 範例 {#section-cc40de6a0a754178aa752601539c815b}

檢視[範本](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)中的範例。
