---
description: 影像服務實現了簡單的視覺水印功能。
solution: Experience Manager
title: 浮水印
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '469'
ht-degree: 1%

---


# 浮水印{#watermarks}

影像服務實現了簡單的視覺水印功能。

水印通常是半透明影像，但可能是文字，或是更複雜的圖層複合影像。 在套用所有檢視屬性(`wid=`、`hei=`、`align=`、`scl=`、`bgc=`)後，伺服器會將浮水印圖層覆蓋在回覆影像上。

通過將`attribute::Watermark`設定為包含水印影像或模板的有效目錄條目來啟用水印。 如果`attribute::Watermark`已在命名目錄中設定，伺服器會將浮水印新增至所有參照請求URL中目錄ID的影像請求。 如果已設定`default::Watermark`（在預設目錄中，[!DNL default.ini]），則無論水印是否參考目錄，都會套用至所有影像請求。

水印不會套用至回應縮圖要求(`req=tmb`)和Dynamic Media檢視器的特定要求而傳回的影像。

## 縮放和對齊{#section-89ef9e5926ae438abbd8e70332749b76}

當指定水印時，伺服器會先產生需要套用水印的複合影像（*目標影像*）（在套用檢視變形之前）。 然後，伺服器為水印生成合成影像，就像其他影像（*水印影像*）一樣。

與標準影像不同，`sizeN=`可以為水印影像的layer=0或layer=comp指定。 這允許相對於目標影像縮放水印影像。 如果未指定`sizeN=`，則水印影像在與目標影像合併時將保持其像素大小。

除`align=`外，水印記錄中會忽略請求命令（如`fmt=`）和視圖命令（如`wid=`）。 `align=` 可用於相對於水印影像相對於目標影像定位水印影像。這允許水印相對於目標影像的角或邊緣定位。

縮放和對齊後，伺服器將使用為水印影像的`layer=0`或`layer=comp`指定的`blendMode=`和`opac=`值，將水印影像層疊在目標影像上。 最後，應用為目標影像指定的請求和視圖命令來構造回覆影像。

請注意，水印影像絕不會透過`wid=`和`hei=`命令延伸至回覆影像中新增的任何空白空間。

## 範例 {#section-0408c977d7324d4cb0e76a91cdfa2acd}

典型的水印可能由包含標誌或版權聲明的簡單RGBA影像組成。 我們會在影像目錄（或預設目錄）中建立記錄，並將`catalog::Id`設為`watermark`，然後在`catalog::Path`中指定浮水印影像檔案。 我們想要延伸浮水印以符合檢視影像（而不會使浮水印產生扭曲），同時保留一點額外的邊界，並將不透明度降低至原始浮水印的20%，因此我們將`catalog::Modifier`設為`sizeN=0.9,0.9&opac=20`。 要激活水印，請將`attribute::Watermark`設定為此示例中的水印目錄條目&quot;watermark&quot;的ID。 我們可能會想嘗試不同的`blendMode=`選項，以取得不同的浮水印效果。

## 另請參閱 {#section-4d66713abacb42c7b6a0c93cbf966a97}

[屬性：:Watermark](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-watermark.md#reference-942b50acb2dd43a5ae498dc41ea9ac9b)
