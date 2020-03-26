---
description: 「影像伺服」支援基於規則運算式比對和替代規則的簡單請求預處理機制。
seo-description: 「影像伺服」支援基於規則運算式比對和替代規則的簡單請求預處理機制。
seo-title: 規則集參考
solution: Experience Manager
title: 規則集參考
topic: Scene7 Image Serving - Image Rendering API
uuid: 356e4939-c57d-459a-8e40-9b25e20fc0a3
translation-type: tm+mt
source-git-commit: b27327f940202b1883a654702aa386c7ae83c856

---


# 規則集參考{#rule-set-reference}

「影像伺服」支援基於規則運算式比對和替代規則的簡單請求預處理機制。

可將預處理規則(規&#x200B;*則集*)的集合附加至影像目錄或預設目錄。 預設目錄中的規則僅適用於請求未識別特定主影像目錄時。

請求預處理規則可在請求被平台伺服器解析器處理之前修改路徑和查詢部分，包括操作路徑、添加命令、更改命令值以及應用模板或宏。 規則也可用來設定和覆寫某些通常只受目錄屬性控制的安全功能，例如請求模糊化、水標籤，以及將服務限制在特定用戶端IP位址。

規則集會儲存為XML檔案檔。 必須在中指定規則集檔案的相對或絕對路徑 `attribute::RuleSetFile`。

## 一般結構 {#section-8bcbd91ea8a946f28051bde8ad21827f}

```
 <?xml version="1.0" encoding="UTF-8"?> 
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
      <header> 
<varname>
  headerValue 
</varname></header>  
   </rule> 
</ruleset>
```

有效 `<?xml>` 的規 `<ruleset>` 則集XML檔案中一律需要有和元素，即使未定義實際規則亦然。

允許 `<ruleset>` 一個元素包含任意數量的 `<rule>` 元素。

預處理規則檔案的內容區分大小寫。

## 規則集驗證 {#section-d8d101a0b4d74580835e37d128d05567}

目錄檔案 [!DNL RuleSet.xsd] 夾中提供了一個副本，在將規則集檔案註冊到檔案之前，應該使用該副本驗證該 [!DNL catalog.ini] 檔案。 請注意，「影像伺服」會使用內部副本進 [!DNL RuleSet.xsd] 行驗證。

## URL預處理 {#section-2c09a2d79ada46b994857c6a7fb4c13a}

在進行任何其他處理之前，系統會部分解析傳入的HTTP請求，以決定應套用哪個影像目錄。 在識別目錄後，會套用所選目錄的規則集（若未識別特定目錄，則會套用預設目錄）。

依 `<rule>` 據與元素()的內容相符的指定順序來搜 `<expression>` 尋元素 *`expression`*。

如果匹 `<rule>` 配，則應用可選 *`substitution`* 請求字串，並將修改的請求字串傳遞到伺服器的請求解析器以進行正常處理。

如果到達結束時未成功匹配，則 `<ruleset>` 請求將傳遞給解析器而不進行修改。

## OnMatch屬性 {#section-ed952fa55d99422db0ee68a2b9d395d3}

可以使用元素的屬性來修 `OnMatch` 改預設行 `<rule>` 為。 `OnMatch` 可設為 `break` （預設）、 `continue`或 `error`。

<table id="table_6680A81492B24CE593330DA7B0075E8F"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>元素和屬性</b> </th> 
   <th class="entry"> <b>相符時的行為</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> &lt;規則OnMatch="break"&gt; </span> </p> </td> 
   <td> <p>在套用此規則的替代後，規則處理會立即終止。 預設. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> &lt;規則OnMatch="continue"&gt; </span> </p> </td> 
   <td> <p>系統會套用替代項目，處理作業會繼續下一個規則。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> &lt;規則OnMatch="error"&gt; </span> </p> </td> 
   <td> <p>規則處理會立即終止，而「請求拒絕」回應狀態會傳回給用戶端。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 覆蓋目錄屬性 {#section-3f1e33a65c5346d1b4a69958c61432f3}

`<rule>` 元素可以選擇定義屬性，當規則成功匹配時，這些屬性將覆蓋相應的目錄屬性。 如果多個符合的規則設定了相同的屬性，則最後一個會佔上風。 請參閱元素的說 ` [<rule>](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/r-rule-rule.md#reference-af76c0e2b8be48dabb52b71fe7e51ee9)` 明，以取得可使用規則控制的屬性清單。

## 規則運算式 {#section-3f77bb9a265147b38c645f63ab1bad8b}

簡單的字串比對適用於非常基本的應用程式，但大部分的例項都需要規則運算式。 雖然規則運算式是業界標準，但特定實作會因例項而異。

[ [!DNL軟體包java.util.regex]描 ](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/) 述了映像服務使用的特定規則運算式實現。

## 擷取的子字串 {#section-066e659406d5403599cd26ae35e80d68}

為方便複雜的URL修改，可在運算式中擷取子字串，方法是將子字串加上括弧(...)。 擷取的子字串會根據前括弧的位置，以1開始依序編號。 捕獲的子字串可以使用 ` $ *`n`*`，其 *`n`* 中是捕獲的子字串的序列號。

## 管理規則集檔案 {#section-0598a608e4044bb4805fe93ceebe10a9}

一個規則集檔案可以附加到具有目錄屬性的每個影像目錄 `attribute::RuleSetFile`。 雖然您可以隨時編輯規則集檔案，但影像伺服器只會在重新載入相關影像目錄時識別變更。 當平台伺服器啟動或重新啟動時，以及當主目錄檔案（具有檔案尾碼）被修改或「接觸」以更改檔案日期時，將執行此重裝。 [!DNL .ini]

## 範例 {#section-aa769437d967459299b83a4bf34fe924}

**範例A.** 定義一個規則，如果影像名稱有尾碼&quot; [!DNL _hg]&quot;，則會增加影像品質設定：

```
<rule> 
   <expression>(?i)_hg$</expression> 
   <substitution>\?&amp;qlt=95,1&amp;resmode=bicub</substitution> 
</rule>
```

規則運算式會指定URL字串結尾處 [!DNL _hg]的「」不區分大小寫的比對。 字尾會以指定的查詢字串取代，這會變更影像品質設定。 請注意，替 `?` 代字串中的字元會被逸出，因為這是規則運算式中的特殊字元。

>[!NOTE]
>
>&amp;符號字元的必要編碼。 或者，替換字串可以包含在CDATA塊中：

`<substitution><![CDATA[&qlt=95,1&resmode=bicub]]></substitution>`

**範例B.** 特定Web應用程式不允許查詢字串。 定義將尾隨路徑元素 `small`、 `medium``large` 或轉換為範本的規則，使用路徑的余數作為影像名稱。 例如， `myCat/myImage/small` 將轉換為 `myCat/smallTemplate?src=myCat/myImage`。

我們可以使用子字串來重新架構請求：

```
<rule> 
   <expression>([^/]+)/(small|medium|large)$</expression> 
   <substitution>$2Template?src=sample/$1</substitution> 
</rule>
```

## 另請參閱 {#section-9b748e7c5cff4759a70f96657bd43352}

[軟體包java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
