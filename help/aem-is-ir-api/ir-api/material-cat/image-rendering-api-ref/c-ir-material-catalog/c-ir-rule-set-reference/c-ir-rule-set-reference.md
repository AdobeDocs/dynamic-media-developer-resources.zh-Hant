---
description: 「影像演算」支援簡單的請求預處理機制，此機制以規則運算式比對和替代規則為基礎。
solution: Experience Manager
title: 規則集參考
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '642'
ht-degree: 0%

---


# 規則集引用{#rule-set-reference}

「影像演算」支援簡單的請求預處理機制，此機制以規則運算式比對和替代規則為基礎。

<!--<a id="section_F44601A65CE1451EAD0A449C66B773CC"></a>-->

預先處理規則（*規則集*）的集合可附加至材質目錄或預設目錄。 僅當請求未附加特定物料目錄時，預設目錄中的規則才適用。

請求預處理規則可在請求由伺服器的請求解析器處理之前修改路徑和查詢部分請求，包括操作路徑、添加命令、更改命令值以及應用模板或宏。 規則也可用來設定和覆寫某些目錄屬性，以及用來限制特定用戶端IP位址的服務。

規則集會儲存為XML檔案檔。 必須在`attribute::RuleSetFile`中指定規則集檔案的相對或絕對路徑。

## 一般結構{#section-74faaee27fc543a2ab4a306f3a03674e}

```
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE ruleset SYSTEM" RuleSet.dtd">
<ruleset>
   <rule>
      <expression>
<varname>
  expression
</varname></expression>
      <substitution>
<varname>
  substitution
</varname></substitution>
      <addressfilter>
<varname>
  addressFilter
</varname></addressfilter>
   </rule>
</ruleset>
```

在有效的規則集XML檔案中，即使未定義實際規則，`<?xml>`、`<!DOCTYPE>`和`<ruleset>`元素也始終是必需的。

允許一個包含任意數目的`<rule>`元素的`<ruleset>`元素。

預處理規則檔案的內容會區分大小寫。

## URL預處理{#section-737a38d1b8c746f995e64fa6cfbcec87}

在進行任何其他處理之前，會部分解析傳入的HTTP請求，以決定應套用哪些材料目錄。 在識別目錄後，會套用所選目錄的規則集（若未識別特定目錄，則會套用預設目錄）。

搜索`<rule>`元素時，按與`<expression>`元素(*`expression`*)的內容匹配的指定順序。

如果`<rule>`符合，則會套用選用的&#x200B;*`substitution`*，並將修改的請求字串傳遞至伺服器的請求剖析器，以進行正常處理。

如果到達`<ruleset>`結尾時未成功匹配，則請求將傳遞給解析器，而不進行修改。

## OnMatch屬性{#section-7a8ad3597780486985af5e9a3b1c7b56}

可以使用`<rule>`元素的`OnMatch`屬性來修改預設行為。 `OnMatch` 可設為 `break` （預設值）、 `continue`或  `error.`

<table id="table_4CABF55B33854A128D5F326B31C6C397"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>元素和屬性 </p> </th> 
   <th colname="col2" class="entry"> <p>相符時的行為 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> &lt;rule OnMatch="break"&gt;</span> </p> </td> 
   <td colname="col2"> <p>在套用此規則的替代後，規則處理會立即終止。 預設. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> &lt;rule OnMatch="continue"&gt;</span> </p> </td> 
   <td colname="col2"> <p>系統會套用替代項目，處理作業會繼續下一個規則。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> &lt;rule OnMatch="error"&gt;</span> </p> </td> 
   <td colname="col2"> <p>規則處理會立即終止，而「請求拒絕」回應狀態會傳回給用戶端。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 覆蓋目錄屬性{#section-1f59ce84234f4576ba8473b0e6ba22ee}

`<rule>` 元素可以選擇定義在規則成功匹配並被設定時覆蓋相應目錄屬性 `OnMatch="break"` 的屬性。如果設定`OnMatch="continue"`，則不應用任何屬性。 請參閱`<rule>`的說明，以取得可使用規則控制的屬性清單。

## 規則運算式{#section-4d326507b52544b0960a9a5f303e3fe6}

簡單的字串比對適用於非常基本的應用程式，但大部分的例項都需要規則運算式。 雖然規則運算式是業界標準，但特定實作會因例項而異。

[軟體包java.util.](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/) regex描述映像服務使用的特定規則運算式實現。

## 擷取的子字串{#section-8057cd65d48949ffb6a50e929bd3688b}

為方便複雜的URL修改，可在運算式中擷取子字串，方法是將子字串加上括弧(...)。 擷取的子字串會根據前括弧的位置，以1開始依序編號。 捕獲的子字串可以使用&#x200B;*`$n`*&#x200B;插入替代中，其中&#x200B;*`n`*&#x200B;是捕獲的子字串的序列號。

## 管理規則集檔案{#section-e8ce976b56404c009496426fd334d23d}

一個規則集檔案可以附加到每個具有目錄屬性`attribute::RuleSetFile`的物料目錄。 雖然您可以隨時編輯規則集檔案，但影像伺服器僅在重新載入相關材料目錄時識別更改。 當平台伺服器啟動或重新啟動時，以及當主目錄檔案（具有[!DNL .ini]檔案尾碼）被修改或「觸摸」（更改檔案日期）時，就會發生這種情況。

## 範例 {#section-c4142a41f5cd4ff799a72fbc130c3700}

規則集示例在映像服務文檔的映像目錄參考的相應部分中提供。

## 另請參閱 {#section-cdaacf84f92c4bffbb4b76197b4e531a}

[軟體包java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
