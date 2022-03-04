---
description: 影像服務實現了簡單的視覺水印工具。
solution: Experience Manager
title: 浮水印
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e744be3f-9753-4513-8f37-055fa03077cc
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '460'
ht-degree: 1%

---

# 浮水印{#watermarks}

影像服務實現了簡單的視覺水印工具。

水印通常是半透明影像，但可能是文本或更複雜的分層複合影像。 伺服器將在所有視圖屬性( `wid=`。 `hei=`。 `align=`。 `scl=`。 `bgc=`)。

通過設定啟用水印 `attribute::Watermark` 到包含水印影像或模板的有效目錄條目。 如果 `attribute::Watermark` 在命名目錄中設定，伺服器將向引用請求URL中的目錄ID的所有影像請求添加水印。 如果 `default::Watermark` 設定(在預設目錄中， [!DNL default.ini])，水印將應用於所有影像請求，而不管它們是否引用目錄。

水印不會應用於響應縮略圖請求而返回的影像( `req=tmb`以及Dynamic Media觀眾的一些要求。

## 縮放和對齊 {#section-89ef9e5926ae438abbd8e70332749b76}

指定水印後，伺服器將首先生成複合影像( *目標影像*)，在應用視圖轉換之前，需要將水印應用到此。 然後，伺服器會像其他影像一樣為水印生成複合影像( *水印影像*)。

與標準影像不同， `sizeN=` 可以為水印影像的layer=0或layer=comp指定。 這允許相對於目標影像縮放水印影像。 如果 `sizeN=` 未指定，當與目標影像合併時，水印影像將保留其像素大小。

請求命令(如 `fmt=`)和查看命令(如 `wid=`)在水印記錄中被忽略，但 `align=`。 `align=` 可用於相對於水印影像相對於目標影像定位水印影像。 這允許水印相對於目標影像的角或邊緣的定位。

縮放和對齊後，伺服器將使用 `blendMode=` 和 `opac=` 指定的值 `layer=0` 或 `layer=comp` 的下界。 最後，應用為目標影像指定的請求和視圖命令來構造應答影像。

請注意，水印影像永遠不會擴展到由 `wid=` 和 `hei=` 的雙曲餘切值。

## 範例 {#section-0408c977d7324d4cb0e76a91cdfa2acd}

典型水印可能由包含徽標或版權聲明的簡單RGBA影像組成。 我們在映像目錄（或預設目錄）中建立記錄 `catalog::Id` 設定為 `watermark` 並在中指定水印影像檔案 `catalog::Path`。 我們希望在保留少量額外邊距的同時，將水印拉伸以適合視圖影像（不扭曲水印），並將不透明度降低到原始水印的20%，因此我們設定 `catalog::Modifier` 至 `sizeN=0.9,0.9&opac=20`。 要激活水印，請設定 `attribute::Watermark` 到水印目錄條目的id，在此示例中為&quot;watermark&quot;。 我們可能想嘗試不同 `blendMode=` 選擇以獲得不同的水印效果。

## 另請參閱 {#section-4d66713abacb42c7b6a0c93cbf966a97}

[屬性：：水印](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-watermark.md#reference-942b50acb2dd43a5ae498dc41ea9ac9b)
