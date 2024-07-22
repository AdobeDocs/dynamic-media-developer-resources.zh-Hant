---
title: 暈映
description: 暈映檔案。 指定用於要求的暈映。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8419d68d-7579-4e62-abbd-7dc0a736ae23
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 3%

---

# 暈映{#vignette}

暈映檔案。 指定用於要求的暈映。

`vignette=[ *`catId`*/] *`recId`*|[catId/] *`檔案`*`

<table id="simpletable_432EC5501CA3431B83A762C3EE4E8DD2"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> catId</span> </p> </td> 
  <td class="stentry"> <p>材質目錄ID （符合<span class="codeph">屬性：：RootId</span>）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> recId</span> </p></td> 
  <td class="stentry"> <p>暈映識別碼（符合<span class="codeph">暈映：：Id</span>）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname">檔案</span> </p></td> 
  <td class="stentry"> <p>相對暈映檔案路徑與名稱。 </p></td> 
 </tr> 
</table>

可以指定暈映對應專案或暈映檔案。 不允許遠端URL。

`vignette=`可用來作為在請求URL路徑中指定暈映的替代方式。 用來透過範本中的變數指定暈映。

如果未指定&#x200B;*`catId`*，則會使用工作階段目錄。

## 屬性 {#section-f58661fc78d7496e8e3d0fb98b945c4b}

可能發生在請求中的任何位置。 覆寫以要求URL路徑指定的暈映。

## 預設 {#section-db0618d48bc84dc8abcc989550349ccc}

無。

## 另請參閱 {#section-dc2668cc2cd54a74b08cff68a12d4edd}

[材質目錄](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-http-material-catalogs/c-ir-http-material-catalogs.md#concept-772742c1688f420a88a56f5136ad1db2)，[自訂變數](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-custom-variables/c-ir-custom-variables.md#concept-8a1d9a50d09a4b7b97b8c83365971f96)
