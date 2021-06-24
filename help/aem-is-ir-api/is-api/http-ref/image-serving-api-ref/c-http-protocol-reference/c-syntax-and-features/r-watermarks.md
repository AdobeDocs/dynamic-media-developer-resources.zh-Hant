---
description: 影像服務實現了簡單的視覺水印設備。
solution: Experience Manager
title: 浮水印
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: e744be3f-9753-4513-8f37-055fa03077cc
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '466'
ht-degree: 1%

---

# 浮水印{#watermarks}

影像服務實現了簡單的視覺水印設備。

水印通常是半透明影像，但可能是文本，或是更複雜的分層複合影像。 在應用所有視圖屬性(`wid=`、`hei=`、`align=`、`scl=`、`bgc=`)後，伺服器將在回復影像上覆蓋水印。

通過將`attribute::Watermark`設定為包含水印影像或模板的有效目錄條目來啟用水印。 如果`attribute::Watermark`設定在命名目錄中，伺服器會將浮水印新增至所有參考請求URL中目錄ID的影像請求。 如果設定了`default::Watermark`（在預設目錄中，為[!DNL default.ini]），則無論水印是否引用目錄，都會將水印應用到所有影像請求。

未對回應縮圖請求(`req=tmb`)和Dynamic Media檢視器特定請求而傳回的影像套用水印。

## 縮放和對齊 {#section-89ef9e5926ae438abbd8e70332749b76}

指定水印後，伺服器將首先生成需要應用水印的複合影像（*目標影像*）（在應用視圖轉換之前）。 然後，伺服器會像其他影像一樣為水印生成複合影像（*水印影像*）。

與標準影像不同，`sizeN=`可以為水印影像的layer=0或layer=comp指定。 這允許相對於目標影像縮放水印影像。 如果未指定`sizeN=`，則水印影像在與目標影像合併時將保持其像素大小。

請求命令（如`fmt=`）和視圖命令（如`wid=`）在水印記錄中被忽略，但`align=`除外。 `align=` 可用來相對於水印影像相對於目標影像定位水印影像。這允許水印相對於目標影像的角或邊緣的定位。

縮放和對齊後，伺服器將使用為水印影像的`layer=0`或`layer=comp`指定的`blendMode=`和`opac=`值，將水印影像層疊在目標影像上。 最後，應用為目標影像指定的請求和視圖命令來構造回復影像。

請注意，水印影像不會通過`wid=`和`hei=`命令擴展到回復影像中的任何空白空間。

## 範例 {#section-0408c977d7324d4cb0e76a91cdfa2acd}

典型的水印可能包含包含徽標或版權聲明的簡單RGBA影像。 我們將`catalog::Id`設定為`watermark`的影像目錄（或預設目錄）中建立記錄，並在`catalog::Path`中指定水印影像檔案。 我們希望將水印拉伸以適合視圖影像（而不使水印扭曲），同時保留一點額外的邊界，並將不透明度降低到原始水印的20%，因此我們將`catalog::Modifier`設定為`sizeN=0.9,0.9&opac=20`。 要激活水印，請在本示例中將`attribute::Watermark`設定為水印目錄項的ID，即「水印」。 我們可能想嘗試不同的`blendMode=`選項來達到不同的水印效果。

## 另請參閱 {#section-4d66713abacb42c7b6a0c93cbf966a97}

[屬性：：浮水印](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-watermark.md#reference-942b50acb2dd43a5ae498dc41ea9ac9b)
