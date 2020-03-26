---
description: 以解析度為基礎的影像縮放。 將影像縮放至要求的解析度。
seo-description: 以解析度為基礎的影像縮放。 將影像縮放至要求的解析度。
seo-title: res
solution: Experience Manager
title: res
topic: Scene7 Image Serving - Image Rendering API
uuid: ab0c8329-5d40-4233-a122-8cb8ca01b500
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# res{#res}

以解析度為基礎的影像縮放。 將影像縮放至要求的解析度。

` res= *`val`*`

<table id="simpletable_E69F3709266749C4A165C90FF18FF5AA"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val </span> </p> </td> 
  <td class="stentry"> <p>目標解析度；通常以每英吋像素（實數）為單位。 </p> </td> 
 </tr> 
</table>

比例因子是按除法計 *`val`* 算的 `catalog::Resolution`。 請注意，此命令不會影響回覆影像的列印解析度。

要使用此功能，必須已知原始源影像的解析度並在中設定 `catalog::Resolution`。 視應用程式而定，解析度單位可能不同。 對於可重複的2D紋理或材質色票（例如桌布或結構），解析度可以表示為像素／英吋或像素／毫米。 航拍照片和地圖可能更符合像素／英里或像素／公里。 在任何情況下，用於的單 `catalog::Resolution` 位必須與用於的單位相同 `res=`。

除了以精確的解析度取得影像外，還可以使用以相同的解析度來結合多個影像，使這些影像中可見的項目彼此精確成比例。 `res=`

>[!NOTE]
>
>通常，合成影像在傳回至用戶端之前，會調整為目標 `wid=`檢視大 `hei=`小(由、 `attribute::DefaultPix`或指定)。 為防止此調整大小並獲得具有指定的精確解析度的圖 `res=`像，可能需要通過顯式指定禁用視圖縮放 `scl=1`。 這會指示伺服器將合成影像裁切為目標檢視大小，而非縮放影像。

## 屬性 {#section-fdbd16e59cff4952a3717146bc91412e}

來源影像／遮色片屬性。 未被與源影像或蒙版關聯的圖層忽略。 已為指定應用到層0的 `layer=comp`。 如果為相 `scale=` 同圖 `size=` 層指定或，則忽略。

## 預設 {#section-c5f1ba6fe53d46eca32e7d0588dcdf3d}

如果未指定， `scale=` 或 `size=` 確定比例因子，或者，如果未指定，則不使用縮放來使用影像。

## 範例 {#section-eb06f333e08e4247971fb1b18922597b}

以12像素／英吋的物件解析度擷取紋理影像，以便與「影像演算」或「影像製作」搭配使用。 我們指定無損的PNG格式和更佳的品質重新取樣，以提供最佳品質，

` http:// *`伺服器`*/myTexture?res=12&fmt=png&resMode=sharp`

## 另請參閱 {#section-1f8a8f11772e493ca803c4511f397a11}

[catalog:::Resolution](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-resolution-cat.md#reference-de489f5f36b64bd0831749546f8728e1) , [attribute::DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1), [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc), [fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
