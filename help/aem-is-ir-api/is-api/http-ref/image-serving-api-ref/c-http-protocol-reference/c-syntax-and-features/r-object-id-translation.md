---
description: 「影像伺服」提供將外部物件ID轉譯為地區設定特定物件（目錄）ID的機制。 主要應用程式是提供地區特定的內容和在多個地區之間共用的內容，而用戶端應用程式則不需要知道地區特定的物件ID。
solution: Experience Manager
title: 物件ID轉譯
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '706'
ht-degree: 9%

---


# 物件ID轉換{#object-id-translation}

「影像伺服」提供將外部物件ID轉譯為地區設定特定物件（目錄）ID的機制。 主要應用程式是提供地區特定的內容和在多個地區之間共用的內容，而用戶端應用程式則不需要知道地區特定的物件ID。

只能使用全域物件ID來編寫應用程式，而影像伺服功能會自動取代地區設定特定的影像和其他可用內容。

*`locale`*&#x200B;在「影像伺服」請求中使用`locale=`命令指定。

>[!NOTE]
>
>物件ID轉譯僅適用於以目錄為基礎的影像伺服。 無法翻譯檔案名。

## 範圍 {#section-66fcd5bd467c4eeaa1574583cbe9756d}

所有對影像、SVG和靜態內容目錄中項目的參考都會視為翻譯字型，而ICC描述檔參考則不會翻譯。 除了[!DNL /is/image]和[!DNL /is/static requests]路徑中的&#x200B;*`object`*&#x200B;外，這些命令和目錄屬性還受ID轉換的約束：`src=`、`mask=`、`template=`、`defaultImage=`、`attribute::DefaultImage`和`attribute::Watermark`。

## ID轉換映射{#section-9e417b352c314dfe94e831fdd62cddc8}

`attribute::LocaleMap` 定義伺服器用來判斷本地化內容ID的規則，以輸入一般物件ID和 `locale=` 值。

`attribute::LocaleMap` 包含輸入地區設定 *清單* (與指定的值相符 `locale=`)，每個地區都包含無或多個輸出地區設定字尾( `*`locSuffix`*`)。

例如，`attribute::LocaleMap`可能如下所示：

`en,_E,|en_us,_E,|en_uk,_E,|fr,_F,|de,_D,|de_at,_D,|de_de,_D,|,_E,`

請求`/is/image/myCat/myImg?locale=de_de`會傳回與目錄條目`myCat/myImg_D`相關聯的影像（假設存在此類目錄條目）。

有關詳細資訊，請參閱`attribute::LocaleMap`的說明。

## 翻譯過程{#section-1f64db17e9f644d88e09853670e14a16}

在上述範例中，伺服器會先在ID轉換映射中尋找&#x200B;*`locale`* &quot; `de_de`&quot;。 然後，它會重複與此條目關聯的&#x200B;*`locSuffixes`*，在本例中為&quot; `_D`&quot;和&quot;&quot;（空尾碼）。 對於每個迭代，尾碼會附加到影像ID和測試在目錄中存在的結果ID。 如果找到，則使用該目錄條目，否則將測試下一個條目。 在此示例中，會檢查以下條目：`myCat/myImg_D`和`myCat/myImg`。 如果找不到相符項目，伺服器會傳回錯誤或預設影像（如果已設定）。

## 未知地區設定{#section-b2f3c83f2dc845d69b5908107b775537}

在上例中，`attribute::LocaleMap`包含一個空的&#x200B;*`locale`*，它定義了預設轉換規則，用於未知的`locale=`值（即未在轉換映射中明確列出的值）。 如果此轉換映射應用於請求`/is/image/myCat/myImg?locale=ja`，則它將解析為`myCat/myImg_E`（如果存在），否則將解析為`myCat/myImg`。

如果轉換映射未指定預設轉換規則，則對於具有未知`locale=`值的所有請求都將返回錯誤。

## 範例 {#section-cc40bb00ee9248bb8cb23e17d7a5984c}

**多層次查閱**

通常最好將地區（例如歐洲、中東、北美）分組，以符合地區標準。 這可透過多層次查閱來達成。

在此範例中，我們想支援西部和中東使用的系列。 這兩個集合都以通用影像集合為基礎，增加或修改了一些影像。然後，這兩個系列會針對特定地區(`m1`、`m2`（針對兩個中東地區變數）進一步調整，以及`w1`、`w2`和`w3`（針對三個西方地區設定），但影像會共用給`w1`和`w3`。 不明地區只會對應至通用集合，且無權存取地區特定影像。

`attribute::LocaleMap: w1,-W,|w2,-W2,-W,|w3,-W,|m1,-M1,-M,|m2,-M2,-M,|,`

下表說明了將考慮哪些目錄條目，以及它們被視為通用輸入ID `myImg`的順序：

<table id="table_97EB13E3DB9B48D3A4184D5ECC8E9F86"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <i>地區設定</i> </b> </th> 
   <th class="entry"> <b>要搜尋的目錄ID</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> w1, w3 </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg-W, myImg </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> w2 </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg-W2, myImg-W, myImg </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> m1 </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg-M1, myImg-M, myImg </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> m2 </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg-M2, myImg-M, myImg </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>所有其他 </p> </td> 
   <td> <p> <span class="codeph"> myImg  </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

**搜尋特定ID**

某些影像命名慣例可能不支援內部的一般影像ID。 請求的通用ID必須一律對應至目錄中的特定ID;通常，可能不知道確切的特定ID。

在此範例中，所有語言的影像可能有`_1`、`_2`或`_3`字尾。 法文地區的特定影像可能有`_22`或`_23`字尾，而德文地區的特定影像可能有`_470`或`_480`字尾。

`attribute::LocaleMap: ,_1,_2,_3|fr,_22,_23,_1,_2,_3|de,_470,_480,_1,_2,_3| de_at,_470,_480,_1,_2,_3| de_de,_470,_480,_1,_2,_3`

下表說明了哪些目錄條目被考慮，以及它們被視為通用輸入ID `myImg`的順序：

<table id="table_A7EE4AA0F1C24284B83CC4B40622D24F"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <i>地區設定</i> </b> </th> 
   <th class="entry"> <b>要搜尋的輸出ID</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> fr </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg_22, myImg_23, myImg_1, myImg_2,myImg_3 </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> de  </span>,  <span class="codeph"> de_at </span>,  <span class="codeph"> de_de  </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg_470, myImg_480, myImg_1, myImg_2,myImg_3 </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>所有其他 </p> </td> 
   <td> <p> <span class="codeph"> myImg_1, myImg_2, myImg_3 </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 另請參閱 {#section-05893816c66a406d89f9bfd6ace8d47a}

[attribute::LocaleMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localemap.md#reference-49bbf598f8ea47c3a563755cef306318) ,  [attribute::DefaultLocale](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultlocale.md#reference-69462ad9923f464f80c2c012342a6b6b),  [locale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb),  [req=xlate](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
