---
description: 「影像伺服」提供將外部對象ID轉譯為地區特定對象（目錄）ID的機制。 主應用程式用於提供在多個語言環境中共用的語言環境特定內容和內容，而客戶應用程式不需要知道語言環境特定對象ID。
solution: Experience Manager
title: 物件ID轉譯
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 7a3bd6a1-2ad4-4da2-944c-489b7d18fdc1
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '703'
ht-degree: 9%

---

# 物件ID轉譯{#object-id-translation}

「影像伺服」提供將外部對象ID轉譯為地區特定對象（目錄）ID的機制。 主應用程式用於提供在多個語言環境中共用的語言環境特定內容和內容，而客戶應用程式不需要知道語言環境特定對象ID。

只能使用全局對象ID寫入應用程式，而「影像服務」將自動替換特定於區域設定的影像和可用的其他內容。

*`locale`*&#x200B;在影像伺服請求中使用`locale=`命令指定。

>[!NOTE]
>
>物件ID轉譯僅適用於以目錄為基礎的影像伺服使用。 無法翻譯檔案名。

## 範圍 {#section-66fcd5bd467c4eeaa1574583cbe9756d}

對影像、SVG和靜態內容目錄中條目的所有引用都被視為翻譯字型，而ICC配置檔案引用不被翻譯。 除了[!DNL /is/image]和[!DNL /is/static requests]路徑中的&#x200B;*`object`*&#x200B;外，這些命令和目錄屬性還要經過ID轉換：`src=`、`mask=`、`template=`、`defaultImage=`、`attribute::DefaultImage`和`attribute::Watermark`。

## ID翻譯對應 {#section-9e417b352c314dfe94e831fdd62cddc8}

`attribute::LocaleMap` 會定義伺服器用來判斷本地化內容ID的規則，只要輸入一般物件ID和 `locale=` 值。

`attribute::LocaleMap` 包含輸入地區 *設定* (與指定的值相符 `locale=`)的清單，每個區域設定尾碼都沒有或更多輸出地區 `*`尾碼(`*`locSuffix)。

例如， `attribute::LocaleMap`可能如下所示：

`en,_E,|en_us,_E,|en_uk,_E,|fr,_F,|de,_D,|de_at,_D,|de_de,_D,|,_E,`

請求`/is/image/myCat/myImg?locale=de_de`將返回與目錄項`myCat/myImg_D`關聯的影像（假定存在此類目錄項）。

有關詳細資訊，請參閱`attribute::LocaleMap`的說明。

## 翻譯程式 {#section-1f64db17e9f644d88e09853670e14a16}

根據上述範例，伺服器會先在ID轉譯對映中尋找&#x200B;*`locale`* &quot; `de_de`&quot;。 然後，它會反覆到與此項目相關聯的&#x200B;*`locSuffixes`*，在此例中為「 `_D`」和「」（空尾碼）。 對於每個迭代，尾碼會附加至影像ID，以及測試目錄中是否存在的結果ID。 如果找到，則使用該目錄項目，否則將測試下一個項目。 在此範例中，會檢查下列項目：`myCat/myImg_D`和`myCat/myImg`。 如果找不到相符項目，則伺服器會傳回錯誤或預設影像（如果已設定）。

## 未知地區 {#section-b2f3c83f2dc845d69b5908107b775537}

在上例中， `attribute::LocaleMap`包含一個空&#x200B;*`locale`*，它定義預設的轉換規則，用於未知的`locale=`值（即未明確列於轉換映射中的值）。 如果此翻譯對應套用至請求`/is/image/myCat/myImg?locale=ja`，則會解析為`myCat/myImg_E`（如果存在），或解析為`myCat/myImg`。

如果翻譯對應未指定預設的翻譯規則，則會為所有具有未知`locale=`值的請求傳回錯誤。

## 範例 {#section-cc40bb00ee9248bb8cb23e17d7a5984c}

**多層查閱**

通常最好將地區設定（例如歐洲、中東、北美）分組，以符合地區標準。 這可透過多層查詢來達成。

在此範例中，我們想支援西部和中東使用的集合。 這兩個集合都以通用影像集合為基礎，增加或修改了一些影像。然後，兩個集合會針對特定地區設定（`m1`、`m2`適用於兩個中東變體，`w1`、`w2`及`w3`適用於三個西方地區設定）進一步細化，但影像會共用給`w1`及`w3`除外。 不明地區只會對應至通用集合，且無權存取地區特定影像。

`attribute::LocaleMap: w1,-W,|w2,-W2,-W,|w3,-W,|m1,-M1,-M,|m2,-M2,-M,|,`

下表說明了將考慮哪些目錄條目，以及一般輸入ID `myImg`的考慮順序：

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

某些影像命名慣例可能不支援內部通用影像ID。 請求的一般ID必須一律對應至目錄中的特定ID;通常不會知道確切的特定ID。

在此範例中，所有語言的影像可能有`_1`、`_2`或`_3`尾碼。 法語地區設定的特定影像可能有`_22`或`_23`尾碼，而德語地區設定的特定影像可能有`_470`或`_480`尾碼。

`attribute::LocaleMap: ,_1,_2,_3|fr,_22,_23,_1,_2,_3|de,_470,_480,_1,_2,_3| de_at,_470,_480,_1,_2,_3| de_de,_470,_480,_1,_2,_3`

下表說明了要考慮哪些目錄條目，以及一般輸入ID `myImg`的考慮順序：

<table id="table_A7EE4AA0F1C24284B83CC4B40622D24F"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <i>地區設定</i> </b> </th> 
   <th class="entry"> <b>要搜索的輸出ID</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> fr </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg_22, myImg_23, myImg_1, myImg_2,myImg_3 </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> de  </span>,  <span class="codeph"> de_at  </span>,  <span class="codeph"> de_de  </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg_470, myImg_480, myImg_1, myImg_2,myImg_3 </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>所有其他 </p> </td> 
   <td> <p> <span class="codeph"> myImg_1, myImg_2, myImg_3 </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 另請參閱 {#section-05893816c66a406d89f9bfd6ace8d47a}

[attribute::LocaleMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localemap.md#reference-49bbf598f8ea47c3a563755cef306318) , attribute:: [DefaultLocale](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultlocale.md#reference-69462ad9923f464f80c2c012342a6b6b),  [locale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb),  [req=xlate](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
