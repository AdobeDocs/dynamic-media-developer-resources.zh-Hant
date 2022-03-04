---
description: Image Serving提供一種機制，用於將外部對象ID轉換為特定於區域設定的對象（目錄）ID。 主應用程式用於提供在多個語言環境之間共用的語言環境特定的內容和內容，而不需要客戶端應用程式知道語言環境特定的對象ID。
solution: Experience Manager
title: 對象ID轉換
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7a3bd6a1-2ad4-4da2-944c-489b7d18fdc1
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '696'
ht-degree: 9%

---

# 對象ID轉換{#object-id-translation}

Image Serving提供一種機制，用於將外部對象ID轉換為特定於區域設定的對象（目錄）ID。 主應用程式用於提供在多個語言環境之間共用的語言環境特定的內容和內容，而不需要客戶端應用程式知道語言環境特定的對象ID。

只能使用全局對象ID編寫應用程式，影像服務將自動替換區域設定特定的影像和其他可用內容。

的 *`locale`* 在Image Serving請求中指定 `locale=` 的子菜單。

>[!NOTE]
>
>對象ID轉換僅適用於基於目錄的影像服務使用。 無法轉換檔案名。

## 範圍 {#section-66fcd5bd467c4eeaa1574583cbe9756d}

對影像、SVG和靜態內容目錄中條目的所有引用都被視為翻譯字型，並且ICC配置檔案引用不被翻譯。 除 *`object`* 在 [!DNL /is/image] 和 [!DNL /is/static requests]，這些命令和目錄屬性受ID轉換的約束： `src=`。 `mask=`。 `template=`。 `defaultImage=`。 `attribute::DefaultImage`, `attribute::Watermark`。

## ID轉換映射 {#section-9e417b352c314dfe94e831fdd62cddc8}

`attribute::LocaleMap` 定義伺服器用於確定本地化內容ID的規則，這些規則作為輸入輸入一般對象ID和 `locale=` 值。

`attribute::LocaleMap` 包含輸入清單 *區域* (與指定的值匹配 `locale=`)，每個都帶有無或更多輸出區域設定尾碼( `*`loc尾碼`*`)。

比如說， `attribute::LocaleMap` 可能是這樣的：

`en,_E,|en_us,_E,|en_uk,_E,|fr,_F,|de,_D,|de_at,_D,|de_de,_D,|,_E,`

請求 `/is/image/myCat/myImg?locale=de_de` 將返回與目錄條目關聯的影像 `myCat/myImg_D` （假定存在此類目錄條目）。

請參閱 `attribute::LocaleMap` 的雙曲餘切值。

## 翻譯流程 {#section-1f64db17e9f644d88e09853670e14a16}

在上例中，伺服器首先查找 *`locale`* &quot; `de_de`」。 然後它在 *`locSuffixes`* 與此條目關聯，在本例中為&quot; `_D`&quot;和&quot;&quot;（空尾碼）。 對於每個迭代，尾碼會附加到影像ID和測試目錄中是否存在的結果ID。 如果找到，則使用該目錄條目，否則將測試下一個目錄條目。 在此示例中，將選中以下條目： `myCat/myImg_D`, `myCat/myImg`。 如果找不到匹配項，伺服器將返回錯誤或預設映像（如果已配置）。

## 未知區域設定 {#section-b2f3c83f2dc845d69b5908107b775537}

在上例中， `attribute::LocaleMap` 包括空 *`locale`* 定義預設轉換規則，用於未知 `locale=` 值（即未在轉換映射中明確列出的值）。 如果此轉換映射已應用於請求 `/is/image/myCat/myImg?locale=ja`它會決心 `myCat/myImg_E`，或 `myCat/myImg`。

如果轉換映射未指定預設轉換規則，則所有未知請求都將返回錯誤 `locale=` 值。

## 範例 {#section-cc40bb00ee9248bb8cb23e17d7a5984c}

**多層查找**

通常最好將地區（如歐洲、中東、北美）分組以符合地區標準。 這可以通過多層查找來實現。

在此示例中，我們希望支援用於西部和中東的收藏。 這兩個集合都以通用影像集合為基礎，增加或修改了一些影像。然後，將針對特定區域設定( `m1`。 `m2` 兩種中東變種 `w1`。 `w2`, `w3` 3個西方語言環境)，但是 `w1` 和 `w3`。 不明地區只會對應至通用集合，且無權存取地區特定影像。

`attribute::LocaleMap: w1,-W,|w2,-W2,-W,|w3,-W,|m1,-M1,-M,|m2,-M2,-M,|,`

下表說明了考慮哪些目錄條目以及它們作為一般輸入ID的考慮順序 `myImg`:

<table id="table_97EB13E3DB9B48D3A4184D5ECC8E9F86"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <i>地區設定</i> </b> </th> 
   <th class="entry"> <b>要搜索的目錄ID</b> </th> 
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
   <td> <p>其他 </p> </td> 
   <td> <p> <span class="codeph"> myImg </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

**搜索特定ID**

某些映像命名約定可能不支援內部通用映像ID。 請求中的泛型ID必須始終映射到目錄中的特定ID;通常，可能不知道具體的ID。

對於本示例，所有語言的影像可能 `_1`。 `_2`或 `_3` 尾碼。 特定於法文語言環境的影像可能 `_22` 或 `_23` 尾碼，以及特定於德國語言環境的影像可能具有 `_470` 或 `_480` 尾碼。

`attribute::LocaleMap: ,_1,_2,_3|fr,_22,_23,_1,_2,_3|de,_470,_480,_1,_2,_3| de_at,_470,_480,_1,_2,_3| de_de,_470,_480,_1,_2,_3`

下表說明了考慮哪些目錄條目以及它們作為一般輸入ID的考慮順序 `myImg`:

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
   <td> <p> <span class="codeph"> 德 </span>。 <span class="codeph"> 取消 </span>。 <span class="codeph"> 取消 </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg_470, myImg_480, myImg_1, myImg_2,myImg_3 </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>其他 </p> </td> 
   <td> <p> <span class="codeph"> myImg_1, myImg_2, myImg_3 </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 另請參閱 {#section-05893816c66a406d89f9bfd6ace8d47a}

[屬性：:LocaleMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localemap.md#reference-49bbf598f8ea47c3a563755cef306318) 。 [屬性：:DefaultLocale](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultlocale.md#reference-69462ad9923f464f80c2c012342a6b6b)。 [區域設定=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb)。 [req=xlate](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
