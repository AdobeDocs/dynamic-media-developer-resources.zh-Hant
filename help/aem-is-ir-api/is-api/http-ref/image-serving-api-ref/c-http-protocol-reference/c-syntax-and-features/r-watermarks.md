---
description: 「影像伺服」實作簡單的視覺浮水印功能。
solution: Experience Manager
title: 浮水印
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e744be3f-9753-4513-8f37-055fa03077cc
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '455'
ht-degree: 0%

---

# 浮水印{#watermarks}

「影像伺服」實作簡單的視覺浮水印功能。

浮水印通常為半透明影像，但也可能為文字，或更複雜、分層的複合影像。 伺服器會在所有檢視屬性( `wid=`， `hei=`， `align=`， `scl=`， `bgc=`)已套用。

浮水印可透過設定啟用 `attribute::Watermark` 至包含浮水印影像或範本的有效目錄專案。 如果 `attribute::Watermark` 設定於具名目錄中，伺服器會將浮水印新增至所有參照請求URL中目錄ID的影像請求。 如果 `default::Watermark` 已設定(在預設目錄中， [!DNL default.ini])，則浮水印會套用至所有影像要求，無論其是否參考目錄。

浮水印不會套用至回應縮圖要求時傳回的影像( `req=tmb`)和Dynamic Media檢視器的特定請求。

## 縮放和對齊 {#section-89ef9e5926ae438abbd8e70332749b76}

當指定浮水印時，伺服器會先產生複合影像( *目標影像*)套用浮水印（在套用檢視轉換之前）。 然後，伺服器會像其他影像一樣，為浮水印產生複合影像( *浮水印影像*)。

不同於標準影像， `sizeN=` 可以為浮水印影像的layer=0或layer=comp指定。 這允許浮水印影像相對於目標影像縮放。 如果 `sizeN=` 未指定，水印影像與目標影像合併時會保留其畫素大小。

要求命令(例如 `fmt=`)和檢視命令(例如 `wid=`)會在浮水印記錄中忽略，但 `align=`. `align=` 可用來相對於浮水印影像與目標影像定位浮水印影像。 如此可讓浮水印相對於目標影像的角落或邊緣定位。

縮放和對齊之後，伺服器會使用 `blendMode=` 和 `opac=` 為指定的值 `layer=0` 或 `layer=comp` 浮水印影像的。 最後，會套用為目標影像指定的要求和檢視指令來建構回覆影像。

請注意，浮水印影像絕不會延伸至由新增至回覆影像的任何空白處。 `wid=` 和 `hei=` 命令。

## 範例 {#section-0408c977d7324d4cb0e76a91cdfa2acd}

典型的浮水印可能包含包含包含標誌或版權宣告的簡單RGBA影像。 我們使用在影像目錄（或預設目錄）中建立記錄 `catalog::Id` 設為 `watermark` 並指定中的浮水印影像檔案 `catalog::Path`. 我們想要拉伸浮水印以符合檢視影像（不扭曲浮水印），同時留下一些額外的邊界，並將不透明度降低為原始浮水印的20%，因此我們設定 `catalog::Modifier` 至 `sizeN=0.9,0.9&opac=20`. 若要啟用浮水印，請設定 `attribute::Watermark` 至浮水印目錄專案的ID，在此範例中為「浮水印」。 我們可能會想要實驗不同的 `blendMode=` 可取得不同浮水印效果的選擇。

## 另請參閱 {#section-4d66713abacb42c7b6a0c93cbf966a97}

[屬性：：浮水印](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-watermark.md#reference-942b50acb2dd43a5ae498dc41ea9ac9b)
