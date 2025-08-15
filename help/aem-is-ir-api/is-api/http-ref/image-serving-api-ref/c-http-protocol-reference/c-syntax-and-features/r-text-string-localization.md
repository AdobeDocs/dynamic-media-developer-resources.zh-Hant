---
title: 文字字串本地化
description: 文字字串本地化可讓影像目錄針對相同的字串值，包含多個地區設定的特定表示法。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f105c7f2-b544-4c08-bb91-4916e485572d
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '644'
ht-degree: 1%

---

# 文字字串本地化{#text-string-localization}

文字字串本地化可讓影像目錄針對相同的字串值，包含多個地區設定的特定表示法。

伺服器會將符合以`locale=`指定的地區設定的表示傳回給使用者端，避免使用者端本地化，並允許應用程式只要傳送適當的`locale=`值搭配IS文字要求來切換地區設定。

## 範圍 {#section-a03f48e3bc0e4ab281909a2bd441a3c2}

文字字串本地化已套用至下列目錄欄位中包含本地化語彙基元` ^loc= *`locId`*^`的所有字串元素：

<table id="table_83344EFCB5B5418184E0A0B43D0B23F7"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>目錄欄位</b> </th> 
   <th class="entry"> 欄位<b>中的</b>字串專案 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph">目錄：：影像集</span> </p> </td> 
   <td> <p>包含可翻譯字串的任何子元素（以分隔符號「，」「；」「：」和/或欄位開頭/結尾的任何組合分隔）。 </p> <p> 可當地語系化欄位開頭的<span class="codeph"> 0xrrggbb </span>色彩值會從本地化中排除，且不會經過修改而通過。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">目錄：：對應</span> </p> </td> 
   <td> <p>任何單引號或雙引號屬性值，除了<span class="codeph">字串= </span>和<span class="codeph">形狀= </span>屬性的值。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">目錄：：目標</span> </p> </td> 
   <td> <p>任何<span class="codeph">目標的值。*.label </span>和<span class="codeph">目標。*.userdata </span>屬性。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">目錄：：UserData </span> </p> </td> 
   <td> <p>任何屬性的值。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 字串語法 {#section-d12320edf300409f8e17565b143acafc}

影像目錄中啟用本地化的&#x200B;*`string`*&#x200B;元素包含一或多個本地化字串，每個字串前面都有一個本地化權杖。

<table id="simpletable_CEFDAE8395E6493E902D58A7E5A25BC7"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> stringElement </span> </span> </p> </td> 
  <td class="stentry"> <p>[ <span class="varname"> defaultString </span>]*{ <span class="varname"> localizationToken </span> <span class="varname"> localizedString </span>} </p> </td> 
 </tr> 
</table>

<table id="simpletable_0A687FA72C4C4C1AAFFCB43143C1AB3B"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> localizationToken </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> ^loc= <span class="varname"> locStr </span> ^ </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> locId </span> </span> </p> </td> 
  <td class="stentry"> <p><span class="varname"> localizedString </span>的內部地區設定識別碼會跟隨此<span class="varname"> localizationToken </span>。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> localizedString </span> </span> </p> </td> 
  <td class="stentry"> <p>當地語系化字串。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname">預設字串</span> </span> </p> </td> 
  <td class="stentry"> <p>用於未知地區設定的字串。 </p> </td> 
 </tr> 
</table>

*`locId`*&#x200B;必須是ASCII且不可包含&#39;^&#39;。

&#39;^&#39;可能會出現在具有或不具有HTTP編碼的子字串中的任何位置。 伺服器符合整個&#x200B;*`localizationToken`* `^loc=locId^`模式，以分隔子字串。

*`stringElements`* （不包含至少一個&#x200B;*`localizationToken`*）不視為本地化。

## 翻譯地圖 {#section-f7ce3df91b724adf95cee44eac4915d4}

`attribute::LocaleStrMap`定義伺服器用來決定哪個&#x200B;*`localizedStrings`*&#x200B;要傳回使用者端的規則。 它包含輸入&#x200B;*`locales`*&#x200B;的清單（符合以`locale=`指定的值），每個都沒有任何或多個內部地區設定識別碼( *`locId`*)。 例如: 

`attribute::LocaleStrMap= en,E|nl,N|de,D|,`

空的&#x200B;*`locId`*&#x200B;值表示應傳回&#x200B;*`defaultString`* （如果有的話）。

如需詳細資訊，請參閱`attribute::LocaleStrMap`的說明。

## 翻譯程式 {#section-a2a8a3e5850f4f7c9d2318267afe98a2}

根據以上範例翻譯對應和請求`/is/image/myCat/myItem?req=&locale=nl`，伺服器會先在地區設定對應中尋找「`nl`」。 相符的專案`nl,N`表示應傳回每個&#x200B;*`stringElement`*&#x200B;標示為&#x200B;*`localizedString`*&#x200B;的`^loc=N^`。 如果此&#x200B;*`localizationToken`*&#x200B;不存在於&#x200B;*`stringElement`*&#x200B;中，則會傳回空值。

假設`catalog::UserData`的`myCat/myItem`包含下列內容（為了清楚起見，插入了分行符號）：

`val1=111?? str1=Default1^loc=N^Dutch1^loc=D^German1?? val2=value2?? str2=^loc=E^English2^loc=N^Dutch2^loc=D^German2?? str3=Default3^loc=N^Dutch3^loc=D^German3`

伺服器會傳回下列內容以回應範例要求：

`val1=111 str1=Dutch1 val2=value2 str2=Dutch2 str3=Dutch3`

## 未知的語言環境 {#section-26dfeefbd60345de94bbfeaaf7741223}

在上述範例中，`attribute::LocaleStrMap`的專案具有空的&#x200B;*`locale`*&#x200B;值。 伺服器使用此專案來處理翻譯對應中未明確指定的所有`locale=`值。

範例翻譯對應會指定在這種情況下應傳回&#x200B;*`defaultString`* （如果有的話）。 因此，若將此翻譯對應套用至要求`/is/image/myCat/myItem?req=&locale=ja`，將會傳回下列專案：

`val1=111 str1=Default1 val2=value2 str2= str3=Default3`

## 範例 {#section-ae6ff7fb90754b839f04ed08aadffa3f}

**語言系列**

多個&#x200B;*`locId`*&#x200B;值可能與翻譯對應中的每個&#x200B;*`locale`*&#x200B;相關聯。 原因是它允許為選取的&#x200B;*`stringElements`*&#x200B;支援特定國家或地區的變體（例如美式英文與英式英文），同時處理大多數具有通用基本語言環境的內容（例如國際英文）。

例如，新增美國專屬英文(`*`locId`* EUS`)和英國專屬英文(`*`locId`* EUK`)的支援，以支援偶爾使用的替代拼字。 如果EUK或EUS不存在，則會退回E。同樣地，在大部分時間傳回通用德文`DAT` （以&#x200B;*`localizedStrings`*&#x200B;標籤）時，奧地利特定德文變體(`D`)可以在需要時使用。

`attribute::LocaleStrMap`看起來像這樣：

`en,E|en_us,EUS,E|en_uk,EUK,E|de,D|de_at,DAT,D|de_de,D`

下表說明部分代表&#x200B;*`stringElement`*&#x200B;與&#x200B;*`locale`*&#x200B;組合的輸出：

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
   <td> <p> en， en_us， en_uk </p> <p> de， de_at， de_de </p> <p>所有其他 </p> </td> 
   <td> <p>英語 </p> <p>德文 </p> <p>- </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> ^loc=E^English^loc=UKE^UK-English^loc=D^German^loc=DAT^Audiential </span> </p> </td> 
   <td> <p> en， en_us </p> <p> en_uk </p> <p> de， de_de </p> <p>de_at </p> <p>所有其他 </p> </td> 
   <td> <p>英語 </p> <p>UK — 英文 </p> <p>德文 </p> <p>奧地利文 </p> <p>- </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> ^ loc=en^English^loc=USE^US-English^loc=D^German^loc=DDE^Deutsch </span> </p> <p> 在此範例中，<span class="varname"> locId </span> DDE不存在於<span class="codeph">屬性：：LocaleStrMap </span>中，因此永遠不會傳回與此<span class="varname"> locId </span>關聯的子字串。 </p> </td> 
   <td> <p> en， en_uk </p> <p> en_us </p> <p> de， de_at， de_de </p> <p>所有其他 </p> </td> 
   <td> <p>英語 </p> <p>美式英文 </p> <p>德文 </p> <p>- </p> </td> 
  </tr> 
 </tbody> 
</table>
