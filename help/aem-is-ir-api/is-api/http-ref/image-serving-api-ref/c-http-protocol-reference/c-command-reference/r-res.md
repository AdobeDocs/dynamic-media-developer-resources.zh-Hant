---
description: 以解析度為基礎的影像縮放。 將影像縮放至要求的解析度。
solution: Experience Manager
title: res
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '331'
ht-degree: 1%

---


# res{#res}

以解析度為基礎的影像縮放。 將影像縮放至要求的解析度。

` res= *`val`*`

<table id="simpletable_E69F3709266749C4A165C90FF18FF5AA"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val  </span> </p> </td> 
  <td class="stentry"> <p>目標解析度；通常以每英吋像素（實數）為單位。 </p> </td> 
 </tr> 
</table>

比例因子是通過將&#x200B;*`val`*&#x200B;除以`catalog::Resolution`來計算的。 請注意，此命令不會影響回覆影像的列印解析度。

要使用此功能，必須已知原始源影像的解析度並在`catalog::Resolution`中設定。 視應用程式而定，解析度單位可能不同。 對於可重複的2D紋理或材質色票（例如桌布或結構），解析度可以表示為像素／英吋或像素／毫米。 航拍照片和地圖可能更符合像素／英里或像素／公里。 無論如何，`catalog::Resolution`使用的單位必須與`res=`使用的單位相同。

除了以精確的解析度取得影像外，`res=`還可用來以相同的解析度結合多張影像，使這些影像中可見的項目彼此成正確比例。

>[!NOTE]
>
>通常，合成映像在返回到客戶機之前會調整到目標視圖大小（由`wid=`、`hei=`或`attribute::DefaultPix`指定）。 為防止調整大小並獲得具有`res=`所指定精確解析度的影像，可能需要通過顯式指定`scl=1`禁用視圖縮放。 這會指示伺服器將合成影像裁切為目標檢視大小，而非縮放影像。

## 屬性 {#section-fdbd16e59cff4952a3717146bc91412e}

來源影像／遮色片屬性。 未被與源影像或蒙版關聯的圖層忽略。 已為`layer=comp`指定應用到層0。 如果為同一層指定`scale=`或`size=`，則忽略。

## 預設 {#section-c5f1ba6fe53d46eca32e7d0588dcdf3d}

如果未指定，`scale=`或`size=`會決定比例系數，或者，如果未指定比例，則會使用影像而不進行縮放。

## 範例 {#section-eb06f333e08e4247971fb1b18922597b}

以12像素／英吋的物件解析度擷取紋理影像，以便與「影像演算」或「影像製作」搭配使用。 我們指定無損的PNG格式和更佳的品質重新取樣，以提供最佳品質，

` http:// *`伺服器`*/myTexture?res=12&fmt=png&resMode=sharp`

## 另請參閱 {#section-1f8a8f11772e493ca803c4511f397a11}

[catalog:::Resolution](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-resolution-cat.md#reference-de489f5f36b64bd0831749546f8728e1) ,  [attribute::DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1), [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc), [fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
