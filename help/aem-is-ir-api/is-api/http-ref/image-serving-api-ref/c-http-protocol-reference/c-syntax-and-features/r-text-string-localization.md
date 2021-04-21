---
description: 文字字串本地化可讓影像目錄包含相同字串值的多個地區特定表示法。
solution: Experience Manager
title: 文字字串本地化
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '674'
ht-degree: 3%

---


# 文字字串本地化{#text-string-localization}

文字字串本地化可讓影像目錄包含相同字串值的多個地區特定表示法。

伺服器會將符合使用`locale=`指定之地區設定的表示法傳回用戶端，以避免用戶端本地化，並讓應用程式只需傳送適當的`locale=`值與IS文字要求，即可切換地區設定。

## 範圍 {#section-a03f48e3bc0e4ab281909a2bd441a3c2}

文字字串本地化套用至下列目錄欄位中包含本地化Token ` ^loc= *`locId`*^`的所有字串元素：

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
   <td> <p>任何包含可翻譯字串的子元素（由分隔符',' ';' ':'和／或欄位開始／結束的任意組合所分隔）。 </p> <p> 在可本地化欄位的開頭處的<span class="codeph"> 0xrrgbb </span>顏色值被排除在本地化之外，並且不經修改而通過。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 目錄：:Map  </span> </p> </td> 
   <td> <p>除<span class="codeph"> coords= </span>和<span class="codeph"> shape= </span>屬性的值外，任何單引號或雙引號屬性值。 </p> </td> 
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

## 字串語法{#section-d12320edf300409f8e17565b143acafc}

影像目錄中啟用本地化的&#x200B;*`string`*&#x200B;元素由一或多個本地化字串組成，每個字串前面都有本地化Token。

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
  <td class="stentry"> <p><span class="varname"> localizedString </span>在此<span class="varname"> localizationToken </span>之後的內部地區設定ID。 </p> </td> 
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

*`locId`* 必須為ASCII，且不得包含&#39;^&#39;。

&#39;^&#39;可能發生在有無HTTP編碼的子字串中的任何位置。 伺服器會比對整個&#x200B;*`localizationToken`* `^loc=locId^`模式以區隔子字串。

*`stringElements`* 不包含至少一個內容 *`localizationToken`* 的ID不會視為本地化。

## 翻譯圖{#section-f7ce3df91b724adf95cee44eac4915d4}

`attribute::LocaleStrMap` 定義伺服器用於確定要返回到客 *`localizedStrings`* 戶端的規則。它包含輸入&#x200B;*`locales`*（與使用`locale=`指定的值匹配）的清單，每個值都沒有或更多內部區域設定ID(*`locId`*)。 例如：

`attribute::LocaleStrMap= en,E|nl,N|de,D|,`

空的&#x200B;*`locId`*&#x200B;值表示應返回&#x200B;*`defaultString`*（如果可用）。

有關詳細資訊，請參閱`attribute::LocaleStrMap`的說明。

## 翻譯過程{#section-a2a8a3e5850f4f7c9d2318267afe98a2}

鑒於上述範例轉譯地圖和請求`/is/image/myCat/myItem?req=&locale=nl`，伺服器會先在地區設定圖中尋找&quot; `nl`&quot;。 匹配的條目`nl,N`表示應針對每個&#x200B;*`stringElement`*&#x200B;返回標有`^loc=N^`的&#x200B;*`localizedString`*。 如果此&#x200B;*`localizationToken`*&#x200B;不存在於&#x200B;*`stringElement`*&#x200B;中，則會傳回空值。

假設`myCat/myItem`的`catalog::UserData`包含下列內容（為清楚起見，插入分行符號）:

`val1=111?? str1=Default1^loc=N^Dutch1^loc=D^German1?? val2=value2?? str2=^loc=E^English2^loc=N^Dutch2^loc=D^German2?? str3=Default3^loc=N^Dutch3^loc=D^German3`

伺服器會回應我們的範例要求，傳回下列內容：

`val1=111 str1=Dutch1 val2=value2 str2=Dutch2 str3=Dutch3`

## 未知地區設定{#section-26dfeefbd60345de94bbfeaaf7741223}

在上例中，`attribute::LocaleStrMap`包含一個帶有空&#x200B;*`locale`*&#x200B;值的條目。 伺服器使用此條目來處理所有未在轉換映射中明確指定的`locale=`值。

示例轉換映射指定在這種情況下，應返回&#x200B;*`defaultString`*（如果可用）。 因此，如果此轉換映射應用於請求`/is/image/myCat/myItem?req=&locale=ja`，將返回以下內容：

`val1=111 str1=Default1 val2=value2 str2= str3=Default3`

## 範例 {#section-ae6ff7fb90754b839f04ed08aadffa3f}

**語系**

多個&#x200B;*`locId`*&#x200B;值可以與翻譯映射中的每個&#x200B;*`locale`*&#x200B;相關聯。 這可支援特定國家或地區的變化（例如，美國英文與英國英文），以選擇&#x200B;*`stringElements`*，同時處理大部分具有共同基本地區（例如國際英文）的內容。

對於我們的範例，我們想新增對美國特定英文(`*`locId`* EUS`)和英國特定英文(`*`locId`* EUK`)的支援，以支援偶爾的替代拼字。 如果EUK或EUS不存在，我們將返回E。同樣地，在大部分時間返回通用德文&#x200B;*`localizedStrings`*（標有`D`）時，可視需要提供奧地利專用的德文變體(`DAT`)。

`attribute::LocaleStrMap` 會像這樣：

`en,E|en_us,EUS,E|en_uk,EUK,E|de,D|de_at,DAT,D|de_de,D`

下表說明某些代表性組合&#x200B;*`stringElement`*&#x200B;和&#x200B;*`locale`*&#x200B;的輸出：

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
   <td> <p> <span class="codeph"> ^loc=E^English^loc=D^German  </span> </p> </td> 
   <td> <p> en,en_us, en_uk </p> <p> de, de_at, de_de </p> <p>所有其他 </p> </td> 
   <td> <p>英語 </p> <p>德文 </p> <p>- </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> ^loc=E^English^loc=UKE^UK-English^loc=D^German^loc=DAT^Austrian  </span> </p> </td> 
   <td> <p> en, en_us </p> <p> en_uk </p> <p> de, de_de </p> <p>de_at </p> <p>所有其他 </p> </td> 
   <td> <p>英語 </p> <p>英文 </p> <p>德文 </p> <p>奧地利文 </p> <p>- </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> ^ loc=en^English^loc=USE^US-English^loc=D^German^loc=DDE^Deutsch  </span> </p> <p> 請注意，在本範例中，<span class="varname"> locId </span> DDE不存在於<span class="codeph">屬性：:LocaleStrMap </span>中，因此不會傳回與此<span class="varname"> locId </span>關聯的子字串。 </p> </td> 
   <td> <p> en, en_uk </p> <p> en_us </p> <p> de, de_at, de_de </p> <p>所有其他 </p> </td> 
   <td> <p>英語 </p> <p>美文——英文 </p> <p>德文 </p> <p>- </p> </td> 
  </tr> 
 </tbody> 
</table>

