---
description: 在影像和SVG資料檔案中可識別以下欄位。
solution: Experience Manager
title: Image_SVG資料
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 5392e08f-3614-4588-8846-4262d32f3ce1
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 3%

---

# Image_SVG資料{#image-svg-data}

在影像和SVG資料檔案中可識別以下欄位。

## 目錄管理 {#section-1056bcc3b6d04166b3aa6ec48913b6b2}

<table id="table_823F89CAD494441690D28F18005F774C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <a href="/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md" type="reference" format="dita" scope="local"> Id</a></span> </p> </td> 
   <td colname="col2"> <p>目錄記錄標識符（索引鍵）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 請求屬性 {#section-cfe69bcdcd4b4d129e99d11b9078ae4a}

<table id="table_C070C676835F49918E1B3BBF81471B09"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <a href="../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-digimarcinfo-cat.md#reference-4925764ed683466bb7af4b807c86f8ba" type="reference" format="dita" scope="local"> DigimarcInfo</a></span> </p> </td> 
   <td colname="col2"> <p>Digimarc內嵌的影像專屬資訊。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <a href="../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a" type="reference" format="dita" scope="local"> 過期</a></span> </p> </td> 
   <td colname="col2"> <p>回覆影像的快取過期（存留時間）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <a href="/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md" type="reference" format="dita" scope="local"> 修飾詞</a> </span> </p> </td> 
   <td colname="col2"> <p>前置詞請求修改量。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <a href="/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-postmodifier-cat.md" type="reference" format="dita" scope="local"> PostModifier</a> </span> </p> </td> 
   <td colname="col2"> <p>Postfix請求修飾元。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <a href="../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-timestamp-cat.md#reference-59a27b72f4cb4a53a3baba83214c4ded" type="reference" format="dita" scope="local"> TimeStamp</a></span> </p> </td> 
   <td colname="col2"> <p>檔案修改時間戳。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 影像屬性 {#section-74c4d124255d4218ade87d7d1677c76d}

<table id="table_F2A33C2EB17A4EACB00DDEF7FB1BB0D4"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <a href="/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-anchor-cat.md" type="reference" format="dita" scope="local"> 錨點</a></span> </p> </td> 
   <td colname="col2"> <p>影像錨點。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <a href="/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-maskpath-cat.md" type="reference" format="dita" scope="local"> 遮色片路徑</a></span> </p> </td> 
   <td colname="col2"> <p>遮罩檔案路徑。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <a href="/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md" type="reference" format="dita" scope="local"> 路徑</a></span> </p> </td> 
   <td colname="col2"> <p>影像/SVG檔案路徑。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <a href="../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-printresolution-cat.md#reference-4ebb2e136995470b84b7c5e10cb8e5f5" type="reference" format="dita" scope="local"> 打印解析度</a></span> </p> </td> 
   <td colname="col2"> <p>打印解析度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <a href="../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-resolution-cat.md#reference-de489f5f36b64bd0831749546f8728e1" type="reference" format="dita" scope="local"> 解析度</a></span> </p> </td> 
   <td colname="col2"> <p>對象解析度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <a href="/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-size-cat.md" type="reference" format="dita" scope="local"> 大小</a></span> </p> </td> 
   <td colname="col2"> <p>影像尺寸. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 縮圖屬性 {#section-c5ac27bcd4224a80b7f42ead249027b1}

<table id="table_E07909B6C16F4D9686ADA381A4178E25"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <a href="../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbres-cat.md#reference-eedb9991397347c3bed5bd0a785c4c69" type="reference" format="dita" scope="local"> ThumbRes</a></span> </p> </td> 
   <td colname="col2"> <p>縮圖解析度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <a href="../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbtype-cat.md#reference-41149ddffc8749cba2f8d9c8e2611e03" type="reference" format="dita" scope="local"> ThumbType</a></span> </p> </td> 
   <td colname="col2"> <p>縮圖類型。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 輔助資料 {#section-bff4e1f9af9d45f1872abac3b414a629}

<table id="table_B6A9A702F533494E85CEC1AD42EC728A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <a href="/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-assettype-cat.md" type="reference" format="dita" scope="local"> AssetType</a></span> </p> </td> 
   <td colname="col2"> <p>資產類型. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <a href="/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md" type="reference" format="dita" scope="local"> ImageSet</a></span> </p> </td> 
   <td colname="col2"> <p>影像集資料。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <a href="/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-map-cat.md" type="reference" format="dita" scope="local"> 地圖</a></span> </p> </td> 
   <td colname="col2"> <p>影像地圖資料。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <a href="/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-targets-cat.md" type="reference" format="dita" scope="local"> 目標</a></span> </p> </td> 
   <td colname="col2"> <p>縮放目標資料。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <a href="/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-userdata-cat.md" type="reference" format="dita" scope="local"> UserData</a></span> </p> </td> 
   <td colname="col2"> <p>使用者定義的資料。 </p> </td> 
  </tr> 
 </tbody> 
</table>
