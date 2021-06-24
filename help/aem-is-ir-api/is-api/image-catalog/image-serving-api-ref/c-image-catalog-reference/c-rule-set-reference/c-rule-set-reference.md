---
description: 「影像伺服」支援以規則運算式比對和替代規則為基礎的簡單請求預處理機制。
solution: Experience Manager
title: 規則集參考
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: dfbb5f5e-d75a-496a-8b97-f102ad1a34d5
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '807'
ht-degree: 0%

---

# 規則集參考{#rule-set-reference}

「影像伺服」支援以規則運算式比對和替代規則為基礎的簡單請求預處理機制。

預先處理規則的集合（*規則集*）可附加至影像目錄或預設目錄。 預設目錄中的規則僅在請求未識別特定主影像目錄時才適用。

請求預處理規則可以在請求由平台伺服器解析器處理之前修改其路徑和查詢部分，包括操作路徑、添加命令、更改命令值以及應用模板或宏。 規則也可用來設定和覆寫某些安全功能，這些功能通常只能由目錄屬性控制，例如請求模糊化、加水標籤，以及將服務限制在特定用戶端IP位址。

規則集儲存為XML文檔檔案。 必須在`attribute::RuleSetFile`中指定規則集檔案的相對路徑或絕對路徑。

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

在有效的規則集XML檔案中，即使未定義實際規則，也始終需要`<?xml>`和`<ruleset>`元素。

允許一個`<ruleset>`元素包含任意數量的`<rule>`元素。

預處理規則檔案的內容區分大小寫。

## 規則集驗證 {#section-d8d101a0b4d74580835e37d128d05567}

目錄資料夾中提供了[!DNL RuleSet.xsd]的副本，在[!DNL catalog.ini]檔案中註冊規則集檔案之前，應該用於驗證規則集檔案。 請注意，影像伺服使用[!DNL RuleSet.xsd]的內部副本進行驗證。

## URL預先處理 {#section-2c09a2d79ada46b994857c6a7fb4c13a}

在進行任何其他處理之前，傳入的HTTP要求會經過部分剖析，以決定應套用哪個影像目錄。 識別目錄後，會套用所選目錄（或預設目錄，若未識別特定目錄）的規則集。

按照為與`<expression>`元素(*`expression`*)的內容匹配而指定的順序搜索`<rule>`元素。

如果`<rule>`匹配，則應用可選&#x200B;*`substitution`*，並將修改的請求字串傳遞到伺服器的請求解析器，以進行正常處理。

如果達到`<ruleset>`結尾時未進行成功匹配，則該請求將傳遞給解析器，無需修改。

## OnMatch屬性 {#section-ed952fa55d99422db0ee68a2b9d395d3}

預設行為可使用`<rule>`元素的`OnMatch`屬性進行修改。 `OnMatch` 可設為( `break` 預設)、 `continue`或 `error`。

<table id="table_6680A81492B24CE593330DA7B0075E8F"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>元素和屬性</b> </th> 
   <th class="entry"> <b>發生符合時的行為</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> &lt;rule OnMatch="break"&gt; </span> </p> </td> 
   <td> <p>套用此規則的替代後，規則處理會立即終止。 預設. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> &lt;rule OnMatch="continue"&gt; </span> </p> </td> 
   <td> <p>替代會套用，處理會繼續處理下一個規則。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> &lt;rule OnMatch="error"&gt; </span> </p> </td> 
   <td> <p>規則處理會立即終止，並傳回「請求拒絕」回應狀態給用戶端。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 覆寫目錄屬性 {#section-3f1e33a65c5346d1b4a69958c61432f3}

`<rule>` 元素可以選擇定義在規則成功匹配時覆蓋相應目錄屬性的屬性。如果多個相符的規則設定了相同的屬性，則最後一個會優先。 如需可使用規則控制的屬性清單，請參閱` [<rule>](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/r-rule-rule.md#reference-af76c0e2b8be48dabb52b71fe7e51ee9)`元素的說明。

## 規則運算式 {#section-3f77bb9a265147b38c645f63ab1bad8b}

簡單字串比對非常基本的應用程式有用，但大多數情況下都需要規則運算式。 雖然規則運算式為業界標準，但特定實作會因例項而異。

[ [!DNL package java.util.regex] ](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/) 說明影像伺服器使用的特定規則運算式實施。

## 擷取的子字串 {#section-066e659406d5403599cd26ae35e80d68}

為方便複雜的URL修改，可在運算式中擷取子字串，方法是以括弧(...)包住子字串。 擷取的子字串會根據前括弧的位置，從1開始依序編號。 捕獲的子字串可以使用` $ *`n`*`插入替代中，其中&#x200B;*`n`*&#x200B;是捕獲的子字串的序列號。

## 管理規則集檔案 {#section-0598a608e4044bb4805fe93ceebe10a9}

一個規則集檔案可以附加到每個具有目錄屬性`attribute::RuleSetFile`的影像目錄。 雖然您隨時都可以編輯規則集檔案，但映像伺服器僅在重新載入相關映像目錄時才能識別更改。 當平台伺服器啟動或重新啟動時，以及當主目錄檔案（其檔案尾碼為[!DNL .ini]）被修改或「接觸」以更改檔案日期時，就會發生此重新載入。

## 範例 {#section-aa769437d967459299b83a4bf34fe924}

**範例A.** 如果影像名稱尾碼為「 [!DNL _hg]」，定義會增加影像品質設定的規則：

```
<rule> 
   <expression>(?i)_hg$</expression> 
   <substitution>\?&amp;qlt=95,1&amp;resmode=bicub</substitution> 
</rule>
```

規則運算式會指定URL字串結尾處不區分大小寫的「 [!DNL _hg]」比對。 尾碼會取代為指定的查詢字串，這會變更影像品質設定。 請注意，替代字串中的`?`字元會逸出，因為這是規則運算式中的特殊字元。

>[!NOTE]
>
>&amp;符號字元的必要編碼。 或者，替代字串可以括在CDATA塊中：

`<substitution><![CDATA[&qlt=95,1&resmode=bicub]]></substitution>`

**範例B.** 特定Web應用程式不允許查詢字串。定義一個規則，該規則將尾隨路徑元素`small`、`medium`或`large`轉換為模板，使用路徑的其餘部分作為影像名稱。 例如， `myCat/myImage/small`將轉譯為`myCat/smallTemplate?src=myCat/myImage`。

我們可以使用子字串來重新建構請求：

```
<rule> 
   <expression>([^/]+)/(small|medium|large)$</expression> 
   <substitution>$2Template?src=sample/$1</substitution> 
</rule>
```

## 另請參閱 {#section-9b748e7c5cff4759a70f96657bd43352}

[套件java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
