---
description: 「影像伺服」提供一種機制，可將外部物件ID轉譯為地區設定的特定物件（目錄） ID。 主要應用程式用於提供地區設定特定內容以及在多個地區設定之間共用的內容，使用者端應用程式不需要知道地區設定特定物件ID。
solution: Experience Manager
title: 物件ID翻譯
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7a3bd6a1-2ad4-4da2-944c-489b7d18fdc1
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '694'
ht-degree: 2%

---

# 物件ID翻譯{#object-id-translation}

「影像伺服」提供一種機制，可將外部物件ID轉譯為地區設定的特定物件（目錄） ID。 主要應用程式用於提供地區設定特定內容以及在多個地區設定之間共用的內容，使用者端應用程式不需要知道地區設定特定物件ID。

只要使用全域物件ID即可編寫應用程式，而「影像伺服」會自動取代地區設定專用影像和其他可用內容。

*`locale`*&#x200B;是使用`locale=`命令在影像伺服要求中指定的。

>[!NOTE]
>
>物件ID轉譯僅適用於以目錄為基礎的「影像伺服」使用。 無法轉譯檔案名稱。

## 範圍 {#section-66fcd5bd467c4eeaa1574583cbe9756d}

對影像、SVG和靜態內容目錄中的專案的所有參照都會被視為翻譯字型，而ICC設定檔參照則不會翻譯。 除了[!DNL /is/image]和[!DNL /is/static requests]路徑中的&#x200B;*`object`*&#x200B;之外，這些命令和目錄屬性還須接受ID轉譯： `src=`、`mask=`、`template=`、`defaultImage=`、`attribute::DefaultImage`和`attribute::Watermark`。

## ID轉譯對應 {#section-9e417b352c314dfe94e831fdd62cddc8}

`attribute::LocaleMap`定義伺服器用來決定本地化內容識別碼的規則，以一般物件識別碼和`locale=`值作為輸入。

`attribute::LocaleMap`包含輸入&#x200B;*語言環境* （符合以`locale=`指定的值）的清單，每個語言環境尾碼都不含或超過輸出語言環境尾碼(`*`locSuffixes`*`)。

例如，`attribute::LocaleMap`可能如下所示：

`en,_E,|en_us,_E,|en_uk,_E,|fr,_F,|de,_D,|de_at,_D,|de_de,_D,|,_E,`

要求`/is/image/myCat/myImg?locale=de_de`會傳回與目錄專案`myCat/myImg_D`關聯的影像（假設此類目錄專案存在）。

如需詳細資訊，請參閱`attribute::LocaleMap`的說明。

## 翻譯程式 {#section-1f64db17e9f644d88e09853670e14a16}

根據上述範例，伺服器會先在ID轉譯對應中尋找&#x200B;*`locale`* &quot; `de_de`&quot;。 然後它會反複執行與此專案相關聯的&#x200B;*`locSuffixes`*，在此案例中是&quot; `_D`&quot;和&quot;&quot; （空白尾碼）。 對於每個反複專案，字尾會附加至影像ID，而產生的ID會根據目錄中的存在性進行測試。 如果找到，則會使用該目錄專案，否則會測試下一個目錄專案。 在此範例中，會檢查這些專案： `myCat/myImg_D`和`myCat/myImg`。 如果找不到相符專案，伺服器會傳回錯誤或預設影像（如果已設定）。

## 未知的語言環境 {#section-b2f3c83f2dc845d69b5908107b775537}

在上述範例中，`attribute::LocaleMap`包含定義預設轉譯規則的空白&#x200B;*`locale`*，用於未知`locale=`值（即未明確列在轉譯對映中的值）。 如果此轉譯對應已套用至要求`/is/image/myCat/myImg?locale=ja`，則會解析為`myCat/myImg_E` （如果存在）或`myCat/myImg`。

如果轉譯對應未指定預設轉譯規則，則會針對具有未知`locale=`值的所有請求傳回錯誤。

## 範例 {#section-cc40bb00ee9248bb8cb23e17d7a5984c}

**多重階層查詢**

將地區（例如，歐洲、中東、北美）分組以符合地區標準通常是值得的。 多階層查閱可達成此目的。

在此範例中，我們要支援西方和中東使用的系列。 這兩個集合都以通用影像集合為基礎，增加或修改了一些影像。然後針對特定地區設定進一步調整兩個集合（`m1`、`m2`適用於兩個中東變體，`w1`、`w2`和`w3`適用於三個西方地區設定），除了為`w1`和`w3`共用影像以外。 未知的地區設定僅對應至一般集合，無法存取地區設定特定的影像。

`attribute::LocaleMap: w1,-W,|w2,-W2,-W,|w3,-W,|m1,-M1,-M,|m2,-M2,-M,|,`

下表說明考慮的目錄專案，以及一般輸入ID `myImg`的考慮順序：

<table id="table_97EB13E3DB9B48D3A4184D5ECC8E9F86"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <i>地區設定</i> </b> </th> 
   <th class="entry"> <b>要搜尋的目錄ID</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> w1，w3 </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg-W， myImg </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> w2 </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg-W2， myImg-W， myImg </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> m1 </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg-M1、myImg-M、myImg </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> m2 </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg-M2、myImg-M、myImg </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>所有其他 </p> </td> 
   <td> <p> <span class="codeph"> myImg </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

**搜尋特定ID**

有些影像命名慣例在內部可能不支援一般影像ID。 要求中的通用ID必須一律對應至目錄中的特定ID；通常可能不知道確切的特定ID。

在此範例中，所有語言的影像都可能有`_1`、`_2`或`_3`尾碼。 法國地區設定的特定影像可能有`_22`或`_23`尾碼，而德國地區設定的特定影像可能有`_470`或`_480`尾碼。

`attribute::LocaleMap: ,_1,_2,_3|fr,_22,_23,_1,_2,_3|de,_470,_480,_1,_2,_3| de_at,_470,_480,_1,_2,_3| de_de,_470,_480,_1,_2,_3`

下表說明考慮的目錄專案，以及一般輸入ID `myImg`的考慮順序：

<table id="table_A7EE4AA0F1C24284B83CC4B40622D24F"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <i>地區設定</i> </b> </th> 
   <th class="entry"> <b>要搜尋的輸出識別碼</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> </span>的<span class="codeph"> </p> </td> 
   <td> <p> <span class="codeph"> myImg_22， myImg_23， myImg_1， myImg_2， myImg_3 </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> de </span>， <span class="codeph"> de_at </span>， <span class="codeph"> de_de </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg_470、myImg_480、myImg_1、myImg_2、myImg_3 </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>所有其他 </p> </td> 
   <td> <p> <span class="codeph"> myImg_1， myImg_2， myImg_3 </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 另請參閱 {#section-05893816c66a406d89f9bfd6ace8d47a}

[attribute：：LocaleMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localemap.md#reference-49bbf598f8ea47c3a563755cef306318) ， [attribute：：DefaultLocale](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultlocale.md#reference-69462ad9923f464f80c2c012342a6b6b)， [locale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb)， [req=xlate](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
