---
description: 靜態內容類型篩選器。 為通過/is/content傳遞的靜態內容指定篩選器字串。
solution: Experience Manager
title: type
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9015d5f4-e42c-43e0-af85-fc9c278448e7
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 4%

---

# type{#type}

靜態內容類型篩選器。 為通過/is/content傳遞的靜態內容指定篩選器字串。

`type= *`谷`*`

<table id="simpletable_B66354A826434A678F3DBC686A0F1436"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 谷</span> </p> </td> 
  <td class="stentry"> <p>鍵入篩選器字串。 </p></td> 
 </tr> 
</table>

伺服器將將val與 `catalog::Type` 請求的靜態內容項。 如果值匹配（區分大小寫），則將將項目返回給客戶端，否則將返回錯誤。

## 屬性 {#section-529b088434a44a9f86a64ef548d2925b}

僅支援通過提供的靜態內容（非映像）請求。 如果忽略 `catalog::Type` 為空或未定義。

## 預設 {#section-e9e8f51d0a01452183ccb510efd87d46}

如果 `type=` 未指定或為空。

## 另請參閱 {#section-da60777a46a74f1bbfa5b2f3b240eb0f}

[為靜態（非影像）內容提供服務](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-serving-static-non-image-content.md#reference-cbe50e697fdf4c7bbb0084f98b7739da)。 [目錄：::UserType](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-usertype-cat.md)
