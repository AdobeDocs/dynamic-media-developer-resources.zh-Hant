---
description: 文本字串本地化允許影像目錄包含同一字串值的多個特定於區域設定的表示法。
solution: Experience Manager
title: 文字字串本地化
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: f105c7f2-b544-4c08-bb91-4916e485572d
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '671'
ht-degree: 3%

---

# 文字字串本地化{#text-string-localization}

文本字串本地化允許影像目錄包含同一字串值的多個特定於區域設定的表示法。

伺服器將與指定的`locale=`語言環境匹配的表示返回給客戶端，從而避免客戶端本地化，並允許應用程式通過發送具有IS文本請求的適當`locale=`值來切換語言環境。

## 範圍 {#section-a03f48e3bc0e4ab281909a2bd441a3c2}

文字字串本地化會套用至所有字串元素，這些元素包含下列目錄欄位中的本地化Token ` ^loc= *`locId`*^`:

<table id="table_83344EFCB5B5418184E0A0B43D0B23F7"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>目錄欄位</b> </th> 
   <th class="entry"> <b>欄位中的字串元素</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> 目錄：:ImageSet  </span> </p> </td> 
   <td> <p>任何包含可翻譯字串的子元素（由分隔符號「，」「；」「：」和/或欄位的開始/結束的任何組合所分隔）。 </p> <p> 本地化欄位開頭的<span class="codeph"> 0xrrggbb </span>顏色值被排除在本地化之外，並且不經修改而傳遞。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 目錄：:Map  </span> </p> </td> 
   <td> <p>任何單引號或雙引號屬性值，但<span class="codeph"> coords= </span>和<span class="codeph"> shape= </span>屬性的值除外。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 目錄：：目標  </span> </p> </td> 
   <td> <p>任何<span class="codeph">目標的值。*.label </span>和<span class="codeph">目標。*.userdata </span>屬性。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 目錄：:UserData  </span> </p> </td> 
   <td> <p>任何屬性的值。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 字串語法 {#section-d12320edf300409f8e17565b143acafc}

影像目錄中已啟用本地化的&#x200B;*`string`*&#x200B;元素包含一或多個本地化字串，每個字串前面都有本地化代號。

<table id="simpletable_CEFDAE8395E6493E902D58A7E5A25BC7"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> stringElement  </span> </span> </p> </td> 
  <td class="stentry"> <p>[ <span class="varname"> defaultString </span>]*{ <span class="varname"> localizationToken </span> <span class="varname"> localizedString </span>} </p> </td> 
 </tr> 
</table>

<table id="simpletable_0A687FA72C4C4C1AAFFCB43143C1AB3B"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> localizationToken  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> ^loc=  <span class="varname"> locStr  </span> ^  </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> locId  </span> </span> </p> </td> 
  <td class="stentry"> <p><span class="varname"> localizedString </span>在此<span class="varname"> localizationToken </span>之後的內部區域設定ID。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> localizedString  </span> </span> </p> </td> 
  <td class="stentry"> <p>本地化字串。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> defaultString  </span> </span> </p> </td> 
  <td class="stentry"> <p>用於未知地區設定的字串。 </p> </td> 
 </tr> 
</table>

*`locId`* 必須為ASCII，且不得包含「^」。

「^」可能出現在含有或不含HTTP-encoding的子字串中的任何位置。 伺服器會比對整個&#x200B;*`localizationToken`* `^loc=locId^`模式，以分隔子字串。

*`stringElements`* 不會將其中至少包含一 *`localizationToken`* 個內容視為本地化。

## 翻譯地圖 {#section-f7ce3df91b724adf95cee44eac4915d4}

`attribute::LocaleStrMap` 定義伺服器用於確定要返回 *`localizedStrings`* 到客戶端的規則。它由輸入&#x200B;*`locales`*（與`locale=`指定的值匹配）的清單組成，每個輸入的內部區域設定ID(*`locId`*)均為無。 例如：

`attribute::LocaleStrMap= en,E|nl,N|de,D|,`

空&#x200B;*`locId`*&#x200B;值表示應傳回&#x200B;*`defaultString`*（如果可用）。

有關詳細資訊，請參閱`attribute::LocaleStrMap`的說明。

## 翻譯程式 {#section-a2a8a3e5850f4f7c9d2318267afe98a2}

在上面的示例翻譯映射和請求`/is/image/myCat/myItem?req=&locale=nl`中，伺服器首先在區域設定映射中查找「 `nl`」。 匹配的條目`nl,N`指示對於每個&#x200B;*`stringElement`*，應返回標籤為`^loc=N^`的&#x200B;*`localizedString`*。 如果&#x200B;*`stringElement`*&#x200B;中未出現此&#x200B;*`localizationToken`*，則返回空值。

假設`myCat/myItem`的`catalog::UserData`包含下列內容（插入分行以求清晰）:

`val1=111?? str1=Default1^loc=N^Dutch1^loc=D^German1?? val2=value2?? str2=^loc=E^English2^loc=N^Dutch2^loc=D^German2?? str3=Default3^loc=N^Dutch3^loc=D^German3`

伺服器會回應我們的範例要求，傳回下列內容：

`val1=111 str1=Dutch1 val2=value2 str2=Dutch2 str3=Dutch3`

## 未知地區 {#section-26dfeefbd60345de94bbfeaaf7741223}

在上例中，`attribute::LocaleStrMap`有一個條目，其中包含空&#x200B;*`locale`*&#x200B;值。 伺服器使用此條目來處理所有未在轉換映射中顯式指定的`locale=`值。

示例轉換映射指定在這種情況下，應返回&#x200B;*`defaultString`*（如果可用）。 因此，如果將此翻譯對應套用至請求`/is/image/myCat/myItem?req=&locale=ja`，將會傳回下列內容：

`val1=111 str1=Default1 val2=value2 str2= str3=Default3`

## 範例 {#section-ae6ff7fb90754b839f04ed08aadffa3f}

**語系**

多個&#x200B;*`locId`*&#x200B;值可以與翻譯映射中的每個&#x200B;*`locale`*&#x200B;相關聯。 這可支援選取&#x200B;*`stringElements`*&#x200B;的特定國家/地區或地區變數（例如美國英語與英國英語），同時以共同的基本地區設定（例如國際英語）處理大部分內容。

例如，我們想要新增對美國特定英文(`*`locId`* EUS`)和英國特定英文(`*`locId`* EUK`)的支援，以支援偶爾的替代拼字。 如果EUK或EUS不存在，我們會回復為E。同樣，在大部分時間返回普通德文&#x200B;*`localizedStrings`*（標籤為`D`）時，可以根據需要提供奧地利特定的德文變體(`DAT`)。

`attribute::LocaleStrMap` 會如下所示：

`en,E|en_us,EUS,E|en_uk,EUK,E|de,D|de_at,DAT,D|de_de,D`

下表說明了某些代表性組合&#x200B;*`stringElement`*&#x200B;和&#x200B;*`locale`*&#x200B;的輸出：

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
   <td> <p> <span class="codeph"> ^loc=E^English^loc=D^德文  </span> </p> </td> 
   <td> <p> en,en_us, en_uk </p> <p> de, de_at, de_de </p> <p>所有其他 </p> </td> 
   <td> <p>英語 </p> <p>德文 </p> <p>- </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> ^loc=E^English^loc=UK^UK-English^loc=D^German^loc=DAT^Austrian  </span> </p> </td> 
   <td> <p> en_us </p> <p> en_uk </p> <p> de, de_de </p> <p>de_at </p> <p>所有其他 </p> </td> 
   <td> <p>英語 </p> <p>英文 </p> <p>德文 </p> <p>奧地利 </p> <p>- </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> ^ loc=en^english^loc=USE^US-English^loc=D^German^loc=DDE^Deutsch  </span> </p> <p> 請注意，在此示例中，<span class="varname"> locId </span> DDE在<span class="codeph">屬性中不存在：:LocaleStrMap </span>，因此不會返回與此<span class="varname"> locId </span>關聯的子字串。 </p> </td> 
   <td> <p> en, en_uk </p> <p> en_us </p> <p> de, de_at, de_de </p> <p>所有其他 </p> </td> 
   <td> <p>英語 </p> <p>美國 — 英語 </p> <p>德文 </p> <p>- </p> </td> 
  </tr> 
 </tbody> 
</table>
