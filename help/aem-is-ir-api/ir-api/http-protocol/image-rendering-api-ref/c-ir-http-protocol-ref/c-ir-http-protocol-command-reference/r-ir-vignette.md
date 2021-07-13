---
description: 暈映檔案。 指定用於此請求的暈映。
solution: Experience Manager
title: vignette
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8419d68d-7579-4e62-abbd-7dc0a736ae23
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 4%

---

# vignette{#vignette}

暈映檔案。 指定用於此請求的暈映。

`vignette=[ *``*/] *``*|[catId/] *`catIdrecIdfile`*`

<table id="simpletable_432EC5501CA3431B83A762C3EE4E8DD2"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> catId</span> </p> </td> 
  <td class="stentry"> <p>材料目錄ID（與<span class="codeph">屬性：:RootId</span>匹配）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> recId</span> </p></td> 
  <td class="stentry"> <p>暈映ID（與<span class="codeph">暈映：:Id</span>相符）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> file</span> </p></td> 
  <td class="stentry"> <p>相對暈映檔案路徑和名稱。 </p></td> 
 </tr> 
</table>

可以指定暈映映射條目或暈映檔案。 不允許使用遠端URL。

`vignette=` 可作為在請求URL路徑中指定暈映的替代方式。主要透過範本中的變數指定暈映。

如果未指定&#x200B;*`catId`*，則使用會話目錄。

## 屬性 {#section-f58661fc78d7496e8e3d0fb98b945c4b}

可能發生在要求內的任何位置。 覆寫以請求URL路徑指定的暈映。

## 預設 {#section-db0618d48bc84dc8abcc989550349ccc}

無。

## 另請參閱 {#section-dc2668cc2cd54a74b08cff68a12d4edd}

[材料目錄](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-http-material-catalogs/c-ir-http-material-catalogs.md#concept-772742c1688f420a88a56f5136ad1db2)、自 [訂變數](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-custom-variables/c-ir-custom-variables.md#concept-8a1d9a50d09a4b7b97b8c83365971f96)
