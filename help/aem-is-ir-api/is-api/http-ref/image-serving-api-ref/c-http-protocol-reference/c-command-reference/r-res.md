---
description: 基於解析度的影像縮放。 將影像縮放到請求的解析度。
solution: Experience Manager
title: 雷
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e8ed7b00-7bb3-463e-9aaa-47f77bd4b45e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '323'
ht-degree: 1%

---

# 雷{#res}

基於解析度的影像縮放。 將影像縮放到請求的解析度。

` res= *`谷`*`

<table id="simpletable_E69F3709266749C4A165C90FF18FF5AA"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 谷 </span> </p> </td> 
  <td class="stentry"> <p>目標解決；通常以像素/英吋（實數）表示。 </p> </td> 
 </tr> 
</table>

比例因子通過除法計算 *`val`* 按 `catalog::Resolution`。 請注意，此命令不影響回復影像的打印解析度。

要使用此功能，必須已知原始源影像的解析度並在中進行設定 `catalog::Resolution`。 根據應用程式的不同，解析度單位可能有所不同。 對於可重複的2D紋理或材料色板（如牆紙或織物），解析度可以表示為像素/英吋或像素/毫米。 空中照片和地圖可以按像素/英里或像素/公里提供更好的服務。 無論如何， `catalog::Resolution` 必須與使用的單位相同 `res=`。

除了以精確的解析度獲取影像外， `res=` 還可用於以相同解析度組合多個影像，以便這些影像中可見的項目彼此成準確比例。

>[!NOTE]
>
>通常，複合影像的大小會調整為目標視圖大小(由 `wid=`。 `hei=`或 `attribute::DefaultPix`)。 防止此調整大小並獲取具有由指定的精確解析度的影像 `res=`，可能需要通過顯式指定來禁用視圖縮放 `scl=1`。 這將指示伺服器將複合影像裁剪為目標視圖大小，而不是縮放它。

## 屬性 {#section-fdbd16e59cff4952a3717146bc91412e}

源影像/蒙版屬性。 被未與源影像或蒙版關聯的層忽略。 已為指定應用於層0 `layer=comp`。 忽略 `scale=` 或 `size=` 為同一層指定。

## 預設 {#section-c5f1ba6fe53d46eca32e7d0588dcdf3d}

如果未指定， `scale=` 或 `size=` 確定比例因子，或者，如果未指定，則使用影像而不進行縮放。

## 範例 {#section-eb06f333e08e4247971fb1b18922597b}

以12像素/英吋對象解析度檢索紋理影像，以便與「影像渲染」或「影像創作」一起使用。 我們指定無損PNG格式和更好的重採樣質量，以獲得盡可能好的質量。

` http:// *`伺服器`*/myTexture?res=12&fmt=png&resMode=sharp`

## 另請參閱 {#section-1f8a8f11772e493ca803c4511f397a11}

[目錄：：解析](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-resolution-cat.md#reference-de489f5f36b64bd0831749546f8728e1) 。 [屬性：:DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1)。 [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc)。 [fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
