---
title: 維涅特
description: Vignette檔案。 指定用於請求的視圖。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8419d68d-7579-4e62-abbd-7dc0a736ae23
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 4%

---

# 維涅特{#vignette}

Vignette檔案。 指定用於請求的視圖。

`vignette=[ *`貓ID`*/] *`recId`*|[catId/] *`檔案`*`

<table id="simpletable_432EC5501CA3431B83A762C3EE4E8DD2"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 貓ID</span> </p> </td> 
  <td class="stentry"> <p>物料目錄ID(匹配到 <span class="codeph"> 屬性：:RootId</span>)。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> recId</span> </p></td> 
  <td class="stentry"> <p>Vignette ID(匹配到 <span class="codeph"> vignette::Id</span>)。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> file</span> </p></td> 
  <td class="stentry"> <p>相對視頻檔案路徑和名稱。 </p></td> 
 </tr> 
</table>

可以指定視頻映射項或視頻檔案。 不允許遠程URL。

`vignette=` 可以用作在請求URL路徑中指定視圖的替代方法。 用於通過模板中的變數指定小圖。

如果 *`catId`* 未指定，則使用會話目錄。

## 屬性 {#section-f58661fc78d7496e8e3d0fb98b945c4b}

請求中的任何位置都可能發生。 覆蓋使用請求URL路徑指定的視圖。

## 預設 {#section-db0618d48bc84dc8abcc989550349ccc}

無。

## 另請參閱 {#section-dc2668cc2cd54a74b08cff68a12d4edd}

[物料目錄](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-http-material-catalogs/c-ir-http-material-catalogs.md#concept-772742c1688f420a88a56f5136ad1db2)。 [自定義變數](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-custom-variables/c-ir-custom-variables.md#concept-8a1d9a50d09a4b7b97b8c83365971f96)
