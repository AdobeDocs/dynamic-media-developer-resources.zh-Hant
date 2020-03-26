---
description: 文字字串本地化可讓影像目錄包含相同字串值的多個地區特定表示法。
seo-description: 文字字串本地化可讓影像目錄包含相同字串值的多個地區特定表示法。
seo-title: 文字字串本地化
solution: Experience Manager
title: 文字字串本地化
topic: Scene7 Image Serving - Image Rendering API
uuid: bdff2403-e3bb-4b3f-a8d7-bb108c1fbee8
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 文字字串本地化{#text-string-localization}

文字字串本地化可讓影像目錄包含相同字串值的多個地區特定表示法。

伺服器會將符合所指定地區的表示法傳回用戶端 `locale=`，以避免用戶端本地化，並允許應用程式只透過IS文字要求傳送適當的值來 `locale=` 切換地區。

## 範圍 {#section-a03f48e3bc0e4ab281909a2bd441a3c2}

文字字串本地化套用至所有字串元素，其中包含下列目錄欄 ` ^loc= *`位中的本地化Token`*^` locId:

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
   <td> <p>任何包含可翻譯字串的子元素（由分隔符',' ';' ':'和／或欄位開始／結束的任意組合所分隔）。 </p> <p> 在可 <span class="codeph"> 本地化 </span> 欄位的開頭處的0xrrggbb顏色值被排除在本地化之外，並且不經修改而通過。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 目錄：:Map </span> </p> </td> 
   <td> <p>任何單引號或雙引號屬性值，但coords= <span class="codeph"> 和shape=屬 </span> 性 <span class="codeph"> 的值除外 </span> 。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 目錄：：目標 </span> </p> </td> 
   <td> <p>任何目標的 <span class="codeph"> 值。*.label </span> 和目 <span class="codeph"> 標。*.userdata屬 </span> 性。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 目錄：:UserData </span> </p> </td> 
   <td> <p>任何屬性的值。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 字串語法 {#section-d12320edf300409f8e17565b143acafc}

影像目錄 *`string`* 中啟用本地化的元素由一或多個本地化字串組成，每個字串前面都有本地化Token。

<table id="simpletable_CEFDAE8395E6493E902D58A7E5A25BC7"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 字 <span class="varname"> 串元素 </span></span> </p> </td> 
  <td class="stentry"> <p>[ <span class="varname"> defaultString </span>]*{ localizationToken <span class="varname"> localized </span> String <span class="varname"></span>} </p> </td> 
 </tr> 
</table>

<table id="simpletable_0A687FA72C4C4C1AAFFCB43143C1AB3B"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 本 <span class="varname"> 地化Token </span></span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> ^loc= <span class="varname"> locStr </span> ^ </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> locId </span></span> </p> </td> 
  <td class="stentry"> <p>本地化字串的內部地區 <span class="varname"> 設定ID </span> ，在此本 <span class="varname"> 地化Token </span>後。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 本地化 <span class="varname"> 的字串 </span></span> </p> </td> 
  <td class="stentry"> <p>本地化字串。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 預 <span class="varname"> 設字串 </span></span> </p> </td> 
  <td class="stentry"> <p>用於未知地區設定的字串。 </p> </td> 
 </tr> 
</table>

*`locId`* 必須為ASCII，且不得包含&#39;^&#39;。

&#39;^&#39;可能發生在有無HTTP編碼的子字串中的任何位置。 伺服器會比對整個模 *`localizationToken`* 式以區 `^loc=locId^` 隔子字串。

*`stringElements`* 不包含至少一個的ID *`localizationToken`* 則不視為本地化。

## 翻譯地圖 {#section-f7ce3df91b724adf95cee44eac4915d4}

`attribute::LocaleStrMap` 定義伺服器用於確定要返回客戶 *`localizedStrings`* 端的規則。 它包含輸入清單(與 *`locales`* 指定的值相符 `locale=`)，每個值都沒有或更多內部地區ID( *`locId`*)。 例如：

`attribute::LocaleStrMap= en,E|nl,N|de,D|,`

空 *`locId`* 值表示應傳 *`defaultString`* 回（如果可用）。

有關詳細資訊，請參 `attribute::LocaleStrMap` 閱的說明。

## 翻譯流程 {#section-a2a8a3e5850f4f7c9d2318267afe98a2}

鑒於上述範例轉譯地圖和請求 `/is/image/myCat/myItem?req=&locale=nl`，伺服器會先在地區設定地圖 `nl`中尋找&quot;&quot;。 相符的項 `nl,N` 目表示應針對每 *`stringElement`*&#x200B;個項目 *`localizedString`* 傳回標籤 `^loc=N^` 為的項目。 如果 *`localizationToken`* 中不存在此值， *`stringElement`*&#x200B;則會返回空值。

假設包含 `catalog::UserData` 以 `myCat/myItem` 下內容（為清楚起見插入斷行）:

`val1=111?? str1=Default1^loc=N^Dutch1^loc=D^German1?? val2=value2?? str2=^loc=E^English2^loc=N^Dutch2^loc=D^German2?? str3=Default3^loc=N^Dutch3^loc=D^German3`

伺服器會回應我們的範例要求，傳回下列內容：

`val1=111 str1=Dutch1 val2=value2 str2=Dutch2 str3=Dutch3`

## 未知地區 {#section-26dfeefbd60345de94bbfeaaf7741223}

在上述範例中， `attribute::LocaleStrMap` 有一個包含空值的 *`locale`* 條目。 伺服器使用此條目處理未在轉 `locale=` 譯映射中明確指定的所有值。

示例轉換映射指定在這種情況下，應 *`defaultString`* 當返回（如果可用）。 因此，如果此轉譯地圖套用至請求，將會傳回下列內容 `/is/image/myCat/myItem?req=&locale=ja`:

`val1=111 str1=Default1 val2=value2 str2= str3=Default3`

## 範例 {#section-ae6ff7fb90754b839f04ed08aadffa3f}

**語系**

多個 *`locId`* 值可以與翻譯映射中的 *`locale`* 每個值相關聯。 這可支援特定國家或地區的變化（例如，美國英文與英國英文），以供選擇，同時處理大部分具有共同基本地區（例如，國際英文）的內容。 *`stringElements`*

例如，我們想新增對美國特定英文( ` *`locId`* EUS`)和英國特定英文( ` *`locId`* EUK`)的支援，以支援偶爾的替代拼字。 如果EUK或EUS不存在，我們將返回E。同樣，奧地利特定的德文變體( `DAT`)可以在大部分時間返回普通德 *`localizedStrings`* 文(標 `D`有)時根據需要提供。

`attribute::LocaleStrMap` 會像這樣：

`en,E|en_us,EUS,E|en_uk,EUK,E|de,D|de_at,DAT,D|de_de,D`

下表說明了某些代表性和組合 *`stringElement`* 的輸 *`locale`* 出：

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
   <td> <p> <span class="codeph"> ^loc=E^English^loc=D^German </span> </p> </td> 
   <td> <p> en,en_us, en_uk </p> <p> de, de_at, de_de </p> <p>所有其他 </p> </td> 
   <td> <p>英語 </p> <p>德文 </p> <p>- </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> ^loc=E^English^loc=UKE^UK-English^loc=D^German^loc=DAT^Austrian </span> </p> </td> 
   <td> <p> en, en_us </p> <p> en_uk </p> <p> de, de_de </p> <p>de_at </p> <p>所有其他 </p> </td> 
   <td> <p>英語 </p> <p>英文 </p> <p>德文 </p> <p>奧地利文 </p> <p>- </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> ^ loc=en^English^loc=USE^US-English^loc=D^German^loc=DDE^Deutsch </span> </p> <p> 請注意，在此範例中， <span class="varname"> locId </span> DDE不存在於屬 <span class="codeph"> 性：:LocaleStrMap中，因此不會傳回與此locId相關的子 </span>字 <span class="varname"></span> 串。 </p> </td> 
   <td> <p> en, en_uk </p> <p> en_us </p> <p> de, de_at, de_de </p> <p>所有其他 </p> </td> 
   <td> <p>英語 </p> <p>美文——英文 </p> <p>德文 </p> <p>- </p> </td> 
  </tr> 
 </tbody> 
</table>

