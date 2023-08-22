---
title: res
description: 以解析度為基礎的影像縮放。 將影像縮放至要求的解析度。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e8ed7b00-7bb3-463e-9aaa-47f77bd4b45e
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '323'
ht-degree: 1%

---

# res{#res}

以解析度為基礎的影像縮放。 將影像縮放至要求的解析度。

` res= *`val`*`

<table id="simpletable_E69F3709266749C4A165C90FF18FF5AA"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val </span> </p> </td> 
  <td class="stentry"> <p>目標解析度；通常以每英吋畫素（實數）為單位。 </p> </td> 
 </tr> 
</table>

比例係數的計算方式為除以 *`val`* 作者： `catalog::Resolution`. 請注意，這個指令不會影響回覆影像的列印解析度。

若要使用此功能，必須知道原始來源影像的解析度，並設定於 `catalog::Resolution`. 視應用程式而定，解析度單位可能會有所不同。 對於可重複的2D紋理或材質色票（例如牆紙或織物），解析度可以表示為畫素/英吋或畫素/毫米。 以畫素/英里或畫素/公里提供航拍照片和地圖可能會更好。 無論如何，使用的單位 `catalog::Resolution` 必須與使用的單位相同 `res=`.

除了以精確解析度取得影像之外， `res=` 也可用來以相同解析度來組合多個影像，以便這些影像中的可見專案彼此保持精確比例。

>[!NOTE]
>
>一般而言，複合影像會調整大小至目標檢視大小(指定自 `wid=`， `hei=`，或 `attribute::DefaultPix`)，然後再傳回使用者端。 若要避免重新調整大小，並取得具有所指定之精確解析度的影像 `res=`，可能必須透過明確指定來停用檢視縮放 `scl=1`. 這會指示伺服器將複合影像裁切成目標檢視大小，而非加以縮放。

## 屬性 {#section-fdbd16e59cff4952a3717146bc91412e}

來源影像/遮色片屬性。 與來源影像或遮色片無關的圖層會略過。 套用至圖層0的指定對象 `layer=comp`. 已忽略，如果 `scale=` 或 `size=` 指定給相同圖層。

## 預設 {#section-c5f1ba6fe53d46eca32e7d0588dcdf3d}

若未指定， `scale=` 或 `size=` 決定縮放係數，或者如果未指定，則使用影像而不進行縮放。

## 範例 {#section-eb06f333e08e4247971fb1b18922597b}

以12畫素/英吋的物件解析度擷取紋理影像，以用於「影像演算」或「影像製作」。 我們指定無遺失的PNG格式和更高品質的重新取樣，以獲得最佳品質，

` http:// *`伺服器`*/myTexture?res=12&fmt=png&resMode=sharp`

## 另請參閱 {#section-1f8a8f11772e493ca803c4511f397a11}

[catalog：：Resolution](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-resolution-cat.md#reference-de489f5f36b64bd0831749546f8728e1) ， [attribute：：DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1)， [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc)， [fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
