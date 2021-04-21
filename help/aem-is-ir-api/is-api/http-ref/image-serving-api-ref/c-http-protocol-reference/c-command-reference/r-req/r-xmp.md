---
description: 中繼XMP資料。 傳回與XMP請求路徑中指定的影像相關聯的中繼資料。
solution: Experience Manager
title: xmp
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '183'
ht-degree: 6%

---


# xmp{#xmp}

中繼XMP資料。 傳回與XMP請求路徑中指定的影像相關聯的中繼資料。

`req=xmp`

其他命令將被忽略。 套用UTF-8編碼。 回應的格式為XML,MIME類型為`text/xml`。

HTTP響應基於`catalog::Expiration`可以與TTL進行快取。

## 屬性 {#section-0d26b6a56c844153ae5cea4880370d00}

請求屬性。 不論目前的圖層設定如何，都適用。

## 預設 {#section-1b2e089dce5d4e0ab664c62bf1be90dd}

如果URL不包含影像路徑或修飾元，則：

```
#S7Z OK 
#Mon Jul 25 17:28:32 PDT 2014 
copyright=Copyright (c) 1995-2014 Adobe Systems Incorporated. All rights reserved.
```

否則，`req=img`

## 範例 {#section-34213692deab4a0f9037d5844132ee14}

查詢影像檔案屬性。

` http:// *`伺服器`*/myPath/myImage.tif?req=imageprops`

查詢映像目錄屬性：

` http:// *`伺服器`*/myRootId?req=catalogprops`

從內嵌在HTML檔案中的用戶端JavaScript存取影像目錄項目的屬性：

```
<script language="JavaScript"> 
     //req=imageprops populates this object with properties: 
     var image = new Object; 
</script> 
<script src="http://server/myRootId/myImageId?req=imageprops,javascript"></script> 
<script> 
     alert("Image Size: " + image.width + " x " + image.height); 
</script>
```

擷取特定目錄項目的遮色片影像，縮放至原始大小的25%:

` http:// *`伺服器`*/myRootId/myImageId?req=mask&scale=0.25`

以八分之一的大小請求影像：

` http:// *`伺服器`*/myRootId/myImageId?scl=8`

這與：

` http:// *`伺服器`*/myRootId/myImageId?req=img&scl=8`

依賴影像目錄中指定的縮圖屬性，請求影像的縮圖：

` http:// *`伺服器`*/myRootId/myImageId?req=tmb&wid=64&hei=64`

傳送文字訊息至伺服器記錄檔：

` http:// *`伺服器`*/myRootId?req=message&message=This%20is%20the%20message`

## 另請參閱 {#section-80cb0892c9174681b640985a1a26e590}

[fmt=](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) , catalog::Targets [, ](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-targets-cat.md)catalog: UserData [, ](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-userdata-cat.md)Scaling Thumbnail [](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f) [](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-response-data/c-properties/c-properties.md#concept-49c609fd6de942cab422ee412353c9d9) [, Chambnail PropertiesMaps, Champs](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-image-maps.md#reference-ff7d1bac2a064104b0c508a81316fdab)
