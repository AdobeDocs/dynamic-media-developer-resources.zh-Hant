---
description: 文本字串本地化允許影像目錄包含同一字串值的多個特定於區域設定的表示法。
solution: Experience Manager
title: 文本字串本地化
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f105c7f2-b544-4c08-bb91-4916e485572d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '666'
ht-degree: 3%

---

# 文本字串本地化{#text-string-localization}

文本字串本地化允許影像目錄包含同一字串值的多個特定於區域設定的表示法。

伺服器將與指定的區域設定匹配的表示形式返回到客戶端 `locale=`從而避免了客戶端本地化，並允許應用程式通過發送適當的語言環境來切換語言環境 `locale=` 值。

## 範圍 {#section-a03f48e3bc0e4ab281909a2bd441a3c2}

文本字串本地化應用於包括本地化令牌的所有字串元素 ` ^loc= *`locId`*^` 在以下目錄欄位中：

<table id="table_83344EFCB5B5418184E0A0B43D0B23F7"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>目錄欄位</b> </th> 
   <th class="entry"> <b>欄位中的字串元素</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> 目錄：:ImageSet </span> </p> </td> 
   <td> <p>包含可翻譯字串的任何子元素（由分隔符「，」「；」「：」和/或欄位的開始/結束的任意組合分隔）。 </p> <p> A <span class="codeph"> 0xrgbb </span> 可本地化欄位開頭的顏色值被排除在本地化之外，並且不經修改而通過。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 目錄：：映射 </span> </p> </td> 
   <td> <p>任何單引號或雙引號的屬性值， <span class="codeph"> 坐標= </span> 和 <span class="codeph"> 形狀= </span> 屬性。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 目錄：：目標 </span> </p> </td> 
   <td> <p>任何值 <span class="codeph"> 目標。*.label </span> 和 <span class="codeph"> 目標。*.用戶資料 </span> 屬性。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 目錄：:UserData </span> </p> </td> 
   <td> <p>任何屬性的值。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 字串語法 {#section-d12320edf300409f8e17565b143acafc}

啟用本地化 *`string`* 影像目錄中的元素由一個或多個本地化字串組成，每個字串前面都帶有本地化標籤。

<table id="simpletable_CEFDAE8395E6493E902D58A7E5A25BC7"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> stringElement </span> </span> </p> </td> 
  <td class="stentry"> <p>[ <span class="varname"> 預設字串 </span>]*{ <span class="varname"> 本地化令牌 </span> <span class="varname"> 本地化字串 </span>} </p> </td> 
 </tr> 
</table>

<table id="simpletable_0A687FA72C4C4C1AAFFCB43143C1AB3B"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 本地化令牌 </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> ^loc= <span class="varname"> locStr </span> ^ </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> locId </span> </span> </p> </td> 
  <td class="stentry"> <p>內部區域設定ID <span class="varname"> 本地化字串 </span> 遵循 <span class="varname"> 本地化令牌 </span>。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 本地化字串 </span> </span> </p> </td> 
  <td class="stentry"> <p>本地化字串。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 預設字串 </span> </span> </p> </td> 
  <td class="stentry"> <p>用於未知區域設定的字串。 </p> </td> 
 </tr> 
</table>

*`locId`* 必須是ASCII，並且不能包含「^」。

「^」可以在帶HTTP編碼或不帶HTTP編碼的子字串中出現。 伺服器與整個 *`localizationToken`* `^loc=locId^` 分離子字串。

*`stringElements`* 其中至少包括 *`localizationToken`* 不考慮本地化。

## 翻譯圖 {#section-f7ce3df91b724adf95cee44eac4915d4}

`attribute::LocaleStrMap` 定義伺服器用於確定 *`localizedStrings`* 返回客戶端。 它包含輸入清單 *`locales`* (與指定的值匹配 `locale=`)，每個都沒有或更多內部區域設定ID( *`locId`*)。 例如: 

`attribute::LocaleStrMap= en,E|nl,N|de,D|,`

空 *`locId`* 值表示 *`defaultString`* 應返回。

請參閱 `attribute::LocaleStrMap` 的雙曲餘切值。

## 翻譯流程 {#section-a2a8a3e5850f4f7c9d2318267afe98a2}

給出上面的示例翻譯映射和請求 `/is/image/myCat/myItem?req=&locale=nl`，伺服器首先查找「 `nl`中。 匹配項 `nl,N` 表示每個 *`stringElement`*，也請參見Wiki頁。 *`localizedString`* 標籤為 `^loc=N^` 應返回。 如果 *`localizationToken`* 不在 *`stringElement`*，返回空值。

假設 `catalog::UserData` 為 `myCat/myItem` 包含以下內容（為了清晰起見，插入換行符）:

`val1=111?? str1=Default1^loc=N^Dutch1^loc=D^German1?? val2=value2?? str2=^loc=E^English2^loc=N^Dutch2^loc=D^German2?? str3=Default3^loc=N^Dutch3^loc=D^German3`

伺服器將返回以下內容以響應示例請求：

`val1=111 str1=Dutch1 val2=value2 str2=Dutch2 str3=Dutch3`

## 未知區域設定 {#section-26dfeefbd60345de94bbfeaaf7741223}

在上例中， `attribute::LocaleStrMap` 有一個空條目 *`locale`* 值。 伺服器使用此條目處理所有 `locale=` 在轉換映射中未顯式指定的值。

示例轉換映射指定在這種情況下， *`defaultString`* 應返回。 因此，如果將此翻譯圖應用於請求，將返回以下內容 `/is/image/myCat/myItem?req=&locale=ja`:

`val1=111 str1=Default1 val2=value2 str2= str3=Default3`

## 範例 {#section-ae6ff7fb90754b839f04ed08aadffa3f}

**語系**

多重 *`locId`* 值可與每個值關聯 *`locale`* 的下界。 這允許支援特定國家/地區或地區的變體（例如，美國英語與英國英語），以供選擇 *`stringElements`* 同時處理大多數具有常用基本語言環境（如國際英語）的內容。

例如，我們希望添加對特定於美國的英語( `*`locId`* EUS`)和英語( `*`locId`* EUK`)，支援偶爾的替代拼寫。 如果EUK或EUS不存在，我們將返回E。同樣，奧地利特有的德語變體( `DAT`)可在返回普通德語時根據需要提供 *`localizedStrings`* (標籤為 `D`)大部分時間。

`attribute::LocaleStrMap` 會是這樣的：

`en,E|en_us,EUS,E|en_uk,EUK,E|de,D|de_at,DAT,D|de_de,D`

下表介紹了某些代表的輸出 *`stringElement`* 和 *`locale`* 組合：

<table id="table_A6B67587C5F44B5E9CD0E7ED29A81198"> 
 <thead> 
  <tr> 
   <th class="entry"> <i>stringElement</i> </th> 
   <th class="entry"> <i>地區設定</i> </th> 
   <th class="entry"> <p>輸出字串 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> ^loc=E^英語^loc=D^德語 </span> </p> </td> 
   <td> <p> en,en_us, en_uk </p> <p> de, de_at, de_de </p> <p>其他 </p> </td> 
   <td> <p>英語 </p> <p>德文 </p> <p>- </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> ^loc=E^English^loc=UKE^UK-English^loc=D^German^loc=DAT^奧地利 </span> </p> </td> 
   <td> <p> en, enus </p> <p> en_uk </p> <p> de,dede </p> <p>取消 </p> <p>其他 </p> </td> 
   <td> <p>英語 </p> <p>英語 </p> <p>德文 </p> <p>奧地利 </p> <p>- </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> ^ loc=en^english^loc=USE^US-English^loc=D^German^loc=DDE^Deutsch </span> </p> <p> 請注意，對於本示例， <span class="varname"> locId </span> DDE不存在於 <span class="codeph"> 屬性：:LocaleStrMap </span>，因此與此關聯的子字串 <span class="varname"> locId </span> 的子菜單。 </p> </td> 
   <td> <p> en, enuk </p> <p> en_us </p> <p> de, de_at, de_de </p> <p>其他 </p> </td> 
   <td> <p>英語 </p> <p>美英語 </p> <p>德文 </p> <p>- </p> </td> 
  </tr> 
 </tbody> 
</table>
