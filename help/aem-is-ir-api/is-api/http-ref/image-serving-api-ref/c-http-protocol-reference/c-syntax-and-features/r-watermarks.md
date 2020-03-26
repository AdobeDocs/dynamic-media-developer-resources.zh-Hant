---
description: 影像服務實現了簡單的視覺水印功能。
seo-description: 影像服務實現了簡單的視覺水印功能。
seo-title: 浮水印
solution: Experience Manager
title: 浮水印
topic: Scene7 Image Serving - Image Rendering API
uuid: b2bbaa59-dad9-4be3-bb92-142ed44f6d65
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 浮水印{#watermarks}

影像服務實現了簡單的視覺水印功能。

水印通常是半透明影像，但可能是文字，或是更複雜的圖層複合影像。 在套用所有檢視屬性(、、、、、 `wid=`)後，伺服器會將浮水印 `hei=`層 `align=``scl=``bgc=`層於回覆影像上。

水印的啟用方式是將 `attribute::Watermark` 水印項目設為包含水印影像或範本的有效目錄項目。 如果 `attribute::Watermark` 在命名目錄中設定，伺服器會將浮水印新增至所有參照請求URL中目錄ID的影像請求。 如果 `default::Watermark` 已設定(在預設目錄中 [!DNL default.ini])，則水印將套用至所有影像要求，不論這些要求是否參考目錄。

水印不會套用至回應縮圖要求( `req=tmb`)和Scene7檢視器的特定要求而傳回的影像。

## 縮放和對齊 {#section-89ef9e5926ae438abbd8e70332749b76}

指定水印後，伺服器會先產生需要套用水印的複合影像( *目標影像*)（套用檢視變形之前）。 然後，伺服器會像其他影像（水印影像）一樣，為水印產生 *合成影像*。

與標準影像不 `sizeN=` 同，可以為水印影像的layer=0或layer=comp指定。 這允許相對於目標影像縮放水印影像。 如果 `sizeN=` 未指定，水印影像在與目標影像合併時將保持其像素大小。

在水印記錄中，請 `fmt=`求命令（如）和視圖命令( `wid=`如)將被忽略，但水印記錄除外 `align=`。 `align=` 可用於相對於水印影像相對於目標影像定位水印影像。 這允許水印相對於目標影像的角或邊緣定位。

縮放和對齊後，伺服器會使用為水印影像或水印影像指定的 `blendMode=` 和 `opac=` 值，將水 `layer=0` 印影像 `layer=comp` 圖層在目標影像上。 最後，應用為目標影像指定的請求和視圖命令來構造回覆影像。

請注意，水印影像不會透過和指令延伸到回覆影像的任何空白 `wid=` 空 `hei=` 間。

## 範例 {#section-0408c977d7324d4cb0e76a91cdfa2acd}

典型的水印可能由包含標誌或版權聲明的簡單RGBA影像組成。 我們會在影像目錄（或預設目錄）中建立記錄，並 `catalog::Id` 將其設 `watermark` 為，並指定水印影像檔 `catalog::Path`。 我們想要延伸浮水印以符合檢視影像（而不會使浮水印扭曲），同時保留一點額外的邊界，並將不透明度降低至原始浮水印的20%，所以我們設 `catalog::Modifier` 定 `sizeN=0.9,0.9&opac=20`為 若要啟動浮水印， `attribute::Watermark` 請在此範例中設定浮水印目錄項目的id為「watermark」。 我們可能會嘗試不同的選 `blendMode=` 擇來達到不同的水印效果。

## 另請參閱 {#section-4d66713abacb42c7b6a0c93cbf966a97}

[屬性：:Watermark](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-watermark.md#reference-942b50acb2dd43a5ae498dc41ea9ac9b)
