---
description: XMP中繼資料。 傳回與請求路徑中所指定影像相關聯的XMP中繼資料。
solution: Experience Manager
title: xmp
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 91e252dd-22e2-4c4e-bc92-67762114c2ce
TQID: 'https://experienceleague.adobe.com/yPJzG9VRk975dHWzRc6o-OX5njAccH8CcwpR-J--uHk'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 179
ht-degree: 2%

---

# xmp{#xmp}

XMP中繼資料。 傳回與請求路徑中所指定影像相關聯的XMP中繼資料。

`req=xmp`

其他指令會被忽略。 UTF-8編碼適用。 回應格式為MIME型別`text/xml`的XML。

HTTP回應可使用以`catalog::Expiration`為基礎的TTL進行快取。

## 屬性 {#section-0d26b6a56c844153ae5cea4880370d00}

要求屬性。 不論目前的圖層設定為何，皆適用。

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

查詢影像目錄屬性：

` http:// *`伺服器`*/myRootId?req=catalogprops`

從內嵌於HTML檔案中的使用者端JavaScript存取影像目錄專案的屬性：

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

擷取特定目錄專案的遮色片影像，縮放為原始大小的25%：

` http:// *`伺服器`*/myRootId/myImageId?req=mask&scale=0.25`

以八分之一大小請求影像：

` http:// *`伺服器`*/myRootId/myImageId?scl=8`

這與：

` http:// *`伺服器`*/myRootId/myImageId?req=img&scl=8`

根據影像目錄中指定的縮圖屬性，要求影像的縮圖：

` http:// *`伺服器`*/myRootId/myImageId?req=tmb&wid=64&hei=64`

傳送文字訊息至伺服器記錄檔：

` http:// *`伺服器`*/myRootId?req=message&message=This%20is%20the%20message`

## 另請參閱 {#section-80cb0892c9174681b640985a1a26e590}

[fmt=](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)，[目錄：：Targets](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-targets-cat.md)，[目錄：：UserData](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-userdata-cat.md)，[縮圖縮放](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f)，[屬性](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-response-data/c-properties/c-properties.md#concept-49c609fd6de942cab422ee412353c9d9)，[影像地圖](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-image-maps.md#reference-ff7d1bac2a064104b0c508a81316fdab)
