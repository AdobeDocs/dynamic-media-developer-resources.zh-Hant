---
description: 預設回覆影像。 指定在找不到影像時要使用的影像或目錄條目。
solution: Experience Manager
title: defaultImage
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 741833b5-e858-4aa5-96c1-bb06539deef3
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '223'
ht-degree: 2%

---

# defaultImage{#defaultimage}

預設回覆影像。 指定在找不到影像時要使用的影像或目錄條目。

` defaultImage= *`object`*`

<table id="simpletable_C1FC14B7D9AE476DB2B10EB402944335"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 物件  </span> </span> </p> </td> 
  <td class="stentry"> <p>影像物件。 </p> </td> 
 </tr> 
</table>

*`object`* 可以是目錄項（包括模板）或簡單的影像檔案路徑。用預設影像替換缺少的影像很實用。 此值將覆蓋相應目錄`attribute::DefaultImage`的值。 空值(`defaultImage=`)禁用預設影像處理。

>[!NOTE]
>
>預設影像機制不適用於SVG對象。 如果找不到請求中指定的SVG物件，則會傳回錯誤。

如果`attribute::DefaultImageMode=0`，則&#x200B;*`object`*&#x200B;會替換整個原始請求，即使多影像合成中只缺少一個影像亦然。 從原始請求保留的唯一命令是：`wid=`、`hei=`、`fmt=`、`qlt=`。

若`attribute::DefaultImageMode=1`，物件僅會取代遺失的圖層影像；會套用遺漏圖層的屬性，並照常處理複合內容並傳回。

## 屬性 {#section-d30923d8dc4042eba10989212dd70887}

要求屬性。 無論目前的層設定為何，都適用。 如果`req=`不是`img`或`tmb`，則忽略。

## 限制 {#section-30df31bc8cac41cd917f1e45196779c2}

預設影像機制不覆蓋外部影像源；如果外來影像源無效，則返回錯誤。

巢狀影像轉譯或FXG轉譯請求失敗時，影像伺服會回復為`DefaultImageMode=0`。

## 預設 {#section-0676c66b233c46a3a3a1517da4ace998}

`attribute::DefaultImage`.

## 另請參閱 {#section-745392143c3747a2955e1ae561f58e5f}

[屬性：:DefaultImageMode](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultimagemode.md#reference-8a996af162f84e46bbe9e6e0d4e26782) ，屬 [性：DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433),  [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1),  [ *`object`* ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0)
