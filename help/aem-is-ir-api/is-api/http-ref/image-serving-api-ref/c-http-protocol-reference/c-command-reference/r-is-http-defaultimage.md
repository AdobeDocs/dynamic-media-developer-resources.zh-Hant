---
title: 預設影像
description: 預設回覆影像。 指定找不到影像時要使用的影像或目錄專案。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 741833b5-e858-4aa5-96c1-bb06539deef3
TQID: 'https://experienceleague.adobe.com/48NrVSWIy5golPIibmMEc9FeoE24MtwxfEiYV35k7k4'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 219
ht-degree: 1%

---

# 預設影像{#defaultimage}

預設回覆影像。 指定找不到影像時要使用的影像或目錄專案。

` defaultImage= *`物件`*`

<table id="simpletable_C1FC14B7D9AE476DB2B10EB402944335"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname">物件</span> </span> </p> </td> 
  <td class="stentry"> <p>影像物件。 </p> </td> 
 </tr> 
</table>

*`object`*&#x200B;可以是目錄專案（包括範本）或簡單的影像檔案路徑。 可用來以預設影像取代遺失的影像。 此值會覆寫對應目錄`attribute::DefaultImage`的值。 空白值( `defaultImage=`)會停用預設影像處理。

>[!NOTE]
>
>預設影像機制不適用於SVG物件。 如果找不到請求中指定的SVG物件，則會傳回錯誤。

如果`attribute::DefaultImageMode=0`，*`object`*&#x200B;會取代整個原始要求，即使多影像組合中只有一個影像遺失亦然。 從原始請求保留的命令只有： `wid=`、`hei=`、`fmt=`、`qlt=`。

如果`attribute::DefaultImageMode=1`，物件只會取代遺失的圖層影像；會套用遺失圖層的屬性，並照常處理及傳回複合影像。

## 屬性 {#section-d30923d8dc4042eba10989212dd70887}

要求屬性。 不論目前的圖層設定為何，皆會套用。 如果`req=`不是`img`或`tmb`，則忽略。

## 限制 {#section-30df31bc8cac41cd917f1e45196779c2}

預設影像機制未涵蓋外部影像來源；如果外部影像來源無效，則會傳回錯誤。

巢狀影像轉譯或FXG轉譯要求失敗時，「影像伺服」會回覆為`DefaultImageMode=0`。

## 預設 {#section-0676c66b233c46a3a3a1517da4ace998}

`attribute::DefaultImage`.

## 另請參閱 {#section-745392143c3747a2955e1ae561f58e5f}

[attribute：：DefaultImageMode](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultimagemode.md#reference-8a996af162f84e46bbe9e6e0d4e26782) ， [attribute：： DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433)， [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1)， [*`object`*](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0)
