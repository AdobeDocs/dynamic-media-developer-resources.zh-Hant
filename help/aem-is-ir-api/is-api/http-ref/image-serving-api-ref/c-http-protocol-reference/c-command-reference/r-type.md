---
description: 靜態內容類型篩選。 指定透過/is/content傳送之靜態內容的篩選字串。
solution: Experience Manager
title: type
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 9015d5f4-e42c-43e0-af85-fc9c278448e7
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 5%

---

# type{#type}

靜態內容類型篩選。 指定透過/is/content傳送之靜態內容的篩選字串。

`type= *`val`*`

<table id="simpletable_B66354A826434A678F3DBC686A0F1436"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>輸入篩選字串。 </p></td> 
 </tr> 
</table>

伺服器將比較val與所請求靜態內容項的`catalog::Type`值。 如果值相符（區分大小寫），則返回項目給客戶端，否則返回錯誤。

## 屬性 {#section-529b088434a44a9f86a64ef548d2925b}

僅支援透過提供的靜態內容（非影像）要求。 如果`catalog::Type`為空或未定義，則忽略。

## 預設 {#section-e9e8f51d0a01452183ccb510efd87d46}

如果未指定`type=`或為空，則不會應用類型匹配。

## 另請參閱 {#section-da60777a46a74f1bbfa5b2f3b240eb0f}

[提供靜態（非影像）內容](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-serving-static-non-image-content.md#reference-cbe50e697fdf4c7bbb0084f98b7739da), [目錄：::UserType](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-usertype-cat.md)
