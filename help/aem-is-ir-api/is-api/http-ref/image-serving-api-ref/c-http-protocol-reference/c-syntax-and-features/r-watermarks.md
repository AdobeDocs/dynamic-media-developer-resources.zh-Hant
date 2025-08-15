---
description: 「影像伺服」實作簡單的視覺浮水印功能。
solution: Experience Manager
title: 浮水印
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e744be3f-9753-4513-8f37-055fa03077cc
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '457'
ht-degree: 0%

---

# 浮水印{#watermarks}

「影像伺服」實作簡單的視覺浮水印功能。

浮水印通常為半透明影像，但也可能為文字，或更複雜、分層的複合影像。 伺服器會在套用所有檢視屬性( `wid=`， `hei=`， `align=`， `scl=`， `bgc=`)之後，在回覆影像上加上浮水印。

將`attribute::Watermark`設定為包含浮水印影像或範本的有效目錄專案，即可啟用浮水印。 如果在具名目錄中設定`attribute::Watermark`，伺服器會將浮水印新增至所有參照要求URL中目錄ID的影像要求。 如果已設定`default::Watermark` （在預設的目錄[!DNL default.ini]中），無論影像要求是否參考目錄，浮水印都會套用至所有影像要求。

浮水印不會套用至回應縮圖要求( `req=tmb`)和Dynamic Media檢視器特定要求而傳回的影像。

## 縮放和對齊 {#section-89ef9e5926ae438abbd8e70332749b76}

指定浮水印時，伺服器會先產生需要套用浮水印的複合影像（*目標影像*） （在套用檢視轉換之前）。 然後，伺服器就會產生浮水印的複合影像，就像任何其他影像（*浮水印影像*）一樣。

與標準影像不同，可以為浮水印影像的layer=0或layer=comp指定`sizeN=`。 這允許浮水印影像相對於目標影像縮放。 如果未指定`sizeN=`，則浮水印影像與目標影像合併時會保留其畫素大小。

浮水印記錄中會忽略要求命令（例如`fmt=`）和檢視命令（例如`wid=`），但`align=`除外。 `align=`可用來相對於相對於目標影像的浮水印影像定位浮水印影像。 如此可讓浮水印相對於目標影像的角落或邊緣定位。

縮放和對齊之後，伺服器會使用為浮水印影像的`blendMode=`或`opac=`指定的`layer=0`和`layer=comp`值，將浮水印影像棧疊在目標影像上。 最後，會套用為目標影像指定的要求和檢視指令來建構回覆影像。

請注意，浮水印影像絕不會延伸`wid=`和`hei=`命令新增至回覆影像的任何空白區域。

## 範例 {#section-0408c977d7324d4cb0e76a91cdfa2acd}

典型的浮水印可能包含包含包含標誌或版權宣告的簡單RGBA影像。 我們在影像目錄（或預設目錄）中建立記錄，並將`catalog::Id`設定為`watermark`，並在`catalog::Path`中指定浮水印影像檔案。 我們想要延伸浮水印以符合檢視影像（不扭曲浮水印），同時留下一些額外的邊界，並將不透明度降低為原始浮水印的20%，因此我們將`catalog::Modifier`設定為`sizeN=0.9,0.9&opac=20`。 若要啟用浮水印，請將`attribute::Watermark`設定為浮水印目錄專案的識別碼，此範例中為「浮水印」。 我們可能會嘗試使用不同的`blendMode=`選項來達到不同的浮水印效果。

## 另請參閱 {#section-4d66713abacb42c7b6a0c93cbf966a97}

[屬性：：浮水印](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-watermark.md#reference-942b50acb2dd43a5ae498dc41ea9ac9b)
