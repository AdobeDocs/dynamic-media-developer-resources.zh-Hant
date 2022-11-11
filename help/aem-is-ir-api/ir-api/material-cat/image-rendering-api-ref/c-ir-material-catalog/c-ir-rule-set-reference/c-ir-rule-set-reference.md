---
description: 「影像轉譯」支援以規則運算式比對和替代規則為基礎的簡單要求預處理機制。
solution: Experience Manager
title: 規則集參考
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 194600d0-72d9-47fb-8525-598beb2ce17d
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '632'
ht-degree: 0%

---

# 規則集參考{#rule-set-reference}

「影像轉譯」支援以規則運算式比對和替代規則為基礎的簡單要求預處理機制。

<!--<a id="section_F44601A65CE1451EAD0A449C66B773CC"></a>-->

預先處理規則的集合(*規則集*)可附加至材料目錄或預設目錄。 僅當請求未附加特定物料目錄時，預設目錄中的規則才適用。

請求預處理規則可以在請求被伺服器的請求解析器處理之前修改請求的路徑和查詢部分，包括操作路徑、添加命令、更改命令值以及應用模板或宏。 規則也可用來設定和覆寫某些目錄屬性，以及將服務限制在特定用戶端IP位址。

規則集儲存為XML文檔檔案。 規則集檔案的相對或絕對路徑必須在 `attribute::RuleSetFile`.

## 一般結構 {#section-74faaee27fc543a2ab4a306f3a03674e}

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

此 `<?xml>`, `<!DOCTYPE>` 和 `<ruleset>` 即使未定義實際規則，有效規則集XML檔案中也始終需要元素。

一 `<ruleset>` 包含任何數量的元素 `<rule>` 允許使用元素。

預處理規則檔案的內容區分大小寫。

## URL預先處理 {#section-737a38d1b8c746f995e64fa6cfbcec87}

在進行任何其他處理之前，傳入的HTTP要求會部分剖析，以決定應套用哪些材料目錄。 識別目錄後，會套用所選目錄（或預設目錄，若未識別特定目錄）的規則集。

此 `<rule>` 會依為符合內容而指定的順序來搜尋元素 `<expression>` 元素( *`expression`*)。

若 `<rule>` 符合，則為選填 *`substitution`* 會套用，且已修改的要求字串會傳遞至伺服器的要求剖析器，以正常處理。

若結尾為 `<ruleset>` 到達時，會將請求傳遞至解析器，無需修改。

## OnMatch屬性 {#section-7a8ad3597780486985af5e9a3b1c7b56}

預設行為可使用 `OnMatch` 屬性 `<rule>` 元素。 `OnMatch` 可設為 `break` （預設）, `continue`，或 `error.`

<table id="table_4CABF55B33854A128D5F326B31C6C397"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>元素和屬性 </p> </th> 
   <th colname="col2" class="entry"> <p>發生符合時的行為 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> &lt;rule OnMatch="break"&gt;</span> </p> </td> 
   <td colname="col2"> <p>套用此規則的替代後，規則處理會立即終止。 預設. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> &lt;rule OnMatch="continue"&gt;</span> </p> </td> 
   <td colname="col2"> <p>替代會套用，處理會繼續處理下一個規則。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> &lt;rule OnMatch="error"&gt;</span> </p> </td> 
   <td colname="col2"> <p>規則處理會立即終止，並傳回「請求拒絕」回應狀態給用戶端。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 覆寫目錄屬性 {#section-1f59ce84234f4576ba8473b0e6ba22ee}

`<rule>` 元素可以選擇性地定義在規則成功匹配時覆蓋相應目錄屬性的屬性，並 `OnMatch="break"` 已設定。 若 `OnMatch="continue"` 已設定。 請參閱 `<rule>` ，以取得可使用規則控制的屬性清單。

## 規則運算式 {#section-4d326507b52544b0960a9a5f303e3fe6}

簡單字串比對非常基本的應用程式有用，但大多數情況下都需要規則運算式。 雖然規則運算式為業界標準，但特定實作會因例項而異。

[套件java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/) 說明影像伺服器使用的特定規則運算式實施。

## 擷取的子字串 {#section-8057cd65d48949ffb6a50e929bd3688b}

為方便複雜的URL修改，可在運算式中擷取子字串，方法是以括弧(...)包住子字串。 擷取的子字串會根據前括弧的位置，從1開始依序編號。 捕獲的子字串可以使用 *`$n`*，其中 *`n`* 是所擷取子字串的序號。

## 管理規則集檔案 {#section-e8ce976b56404c009496426fd334d23d}

一個規則集檔案可以附加到具有目錄屬性的每個物料目錄 `attribute::RuleSetFile`. 雖然您可以隨時編輯規則集檔案，但映像伺服器僅在重新載入關聯的材料目錄時才能識別更改。 當 [!DNL Platform Server] 會啟動或重新啟動，且每次主目錄檔案(具有 [!DNL .ini] 檔案尾碼)修改或「接觸」（以變更檔案日期）。

## 範例 {#section-c4142a41f5cd4ff799a72fbc130c3700}

在影像伺服檔案的影像目錄參考的對應區段中提供規則集範例。

## 另請參閱 {#section-cdaacf84f92c4bffbb4b76197b4e531a}

[套件java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
