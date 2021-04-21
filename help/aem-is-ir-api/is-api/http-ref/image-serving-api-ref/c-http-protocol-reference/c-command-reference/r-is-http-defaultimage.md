---
description: 預設回覆影像。 指定在找不到影像時要使用的影像或目錄項目。
solution: Experience Manager
title: defaultImage
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 2%

---


# defaultImage{#defaultimage}

預設回覆影像。 指定在找不到影像時要使用的影像或目錄項目。

` defaultImage= *`object`*`

<table id="simpletable_C1FC14B7D9AE476DB2B10EB402944335"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 物件  </span> </span> </p> </td> 
  <td class="stentry"> <p>影像物件。 </p> </td> 
 </tr> 
</table>

*`object`* 可以是目錄條目（包括模板）或簡單的影像檔案路徑。用預設影像取代遺失的影像非常實用。 此值覆蓋相應目錄`attribute::DefaultImage`的值。 空值(`defaultImage=`)會停用預設影像處理。

>[!NOTE]
>
>預設影像機制不適用於SVG物件。 如果找不到在請求中指定的SVG物件，則會傳回錯誤。

如果`attribute::DefaultImageMode=0`，則&#x200B;*`object`*&#x200B;會取代整個原始請求，即使多影像合成中只有一個影像遺失。 從原始請求保留的唯一命令是：`wid=`、`hei=`、`fmt=`、`qlt=`。

如果`attribute::DefaultImageMode=1`，則對象只替換丟失的圖層影像；會套用遺失圖層的屬性，並照常處理及傳回複合內容。

## 屬性 {#section-d30923d8dc4042eba10989212dd70887}

請求屬性。 不論目前的圖層設定為何，都適用。 如果`req=`不是`img`或`tmb`，則忽略。

## 限制{#section-30df31bc8cac41cd917f1e45196779c2}

外來影像源未被預設影像機制覆蓋；如果外來影像來源無效，則會傳回錯誤。

當巢狀影像轉譯或FXG轉譯請求失敗時，影像伺服會回復為`DefaultImageMode=0`。

## 預設 {#section-0676c66b233c46a3a3a1517da4ace998}

`attribute::DefaultImage`.

## 另請參閱 {#section-745392143c3747a2955e1ae561f58e5f}

[attribute::DefaultImageMode](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultimagemode.md#reference-8a996af162f84e46bbe9e6e0d4e26782) ,  [attribute:DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433),  [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1),  [ *`object`* ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0)
