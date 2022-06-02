---
description: 影像服務支援基於規則運算式匹配和替換規則的簡單請求預處理機制。
solution: Experience Manager
title: 規則集引用
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: dfbb5f5e-d75a-496a-8b97-f102ad1a34d5
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '799'
ht-degree: 0%

---

# 規則集引用{#rule-set-reference}

影像服務支援基於規則運算式匹配和替換規則的簡單請求預處理機制。

預處理規則的集合(*規則集*)可以附加到映像目錄或預設目錄。 僅當請求未標識特定主映像目錄時，預設目錄中的規則才適用。

請求預處理規則可以在請求由平台伺服器的分析器處理之前修改其路徑和查詢部分，包括操作路徑、添加命令、更改命令值以及應用模板或宏。 規則還可用於配置和覆蓋某些通常僅通過目錄屬性控制的安全功能，如請求混淆、水標籤以及將服務限制到特定客戶端IP地址。

規則集以XML文檔檔案形式儲存。 必須在中指定規則集檔案的相對路徑或絕對路徑 `attribute::RuleSetFile`。

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

的 `<?xml>` 和 `<ruleset>` 有效規則集XML檔案中始終需要元素，即使未定義任何實際規則。

一 `<ruleset>` 包含任意數量的元素 `<rule>` 元素。

預處理規則檔案的內容區分大小寫。

## 規則集驗證 {#section-d8d101a0b4d74580835e37d128d05567}

副本 [!DNL RuleSet.xsd] 在目錄資料夾中提供，應用於驗證規則集檔案，然後才將其註冊到 [!DNL catalog.ini] 的子菜單。 請注意，Image Serving使用 [!DNL RuleSet.xsd] 。

## URL預處理 {#section-2c09a2d79ada46b994857c6a7fb4c13a}

在進行任何其他處理之前，將部分分析傳入的HTTP請求，以確定應應用哪個影像目錄。 一旦標識了目錄，則應用所選目錄（或預設目錄，如果未標識特定目錄）的規則集。

的 `<rule>` 按為與元素的內容匹配而指定的順序搜索元素 `<expression>` 元素(E) *`expression`*)。

如果 `<rule>` 匹配，可選 *`substitution`* 應用並將修改的請求字串傳遞給伺服器的請求解析器以進行正常處理。

如果在 `<ruleset>` 訪問時，請求將傳遞給解析器，而不進行修改。

## OnMatch屬性 {#section-ed952fa55d99422db0ee68a2b9d395d3}

可以使用 `OnMatch` 屬性 `<rule>` 的子菜單。 `OnMatch` 可能設定為 `break` （預設）, `continue`或 `error`。

<table id="table_6680A81492B24CE593330DA7B0075E8F"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>元素和屬性</b> </th> 
   <th class="entry"> <b>匹配時的行為</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> &lt;rule OnMatch="break"&gt; </span> </p> </td> 
   <td> <p>應用此規則的替代後，規則處理即終止。 預設. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> &lt;rule OnMatch="continue"&gt; </span> </p> </td> 
   <td> <p>應用替代，並繼續處理下一個規則。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> &lt;rule OnMatch="error"&gt; </span> </p> </td> 
   <td> <p>規則處理立即終止，並且「請求拒絕」響應狀態返回給客戶端。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 覆蓋目錄屬性 {#section-3f1e33a65c5346d1b4a69958c61432f3}

的 `rule` 元素可以根據需要定義在規則成功匹配時覆蓋相應目錄屬性的屬性。 如果多個匹配的規則設定了同一屬性，則最後一個將佔上風。 請參閱 [規則](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/r-rule-rule.md) 元素，用於可用規則控制的屬性清單。

## 規則運算式 {#section-3f77bb9a265147b38c645f63ab1bad8b}

簡單字串匹配適用於非常基本的應用程式，但大多數實例都需要規則運算式。 雖然規則運算式是行業標準，但具體實現因實例而異。

[ [!DNL package java.util.regex] ](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/) 描述Image Service使用的特定規則運算式實現。

## 捕獲的子字串 {#section-066e659406d5403599cd26ae35e80d68}

為便於對複雜URL進行修改，可以通過用括弧(...)將子字串括起來，在表達式中捕獲子字串。 捕獲的子字串根據前括弧的位置以1開始按順序編號。 捕獲的子字串可以使用 ` $ *`n`*`，也請參見Wiki頁。 *`n`* 是捕獲的子字串的序列號。

## 管理規則集檔案 {#section-0598a608e4044bb4805fe93ceebe10a9}

可以使用目錄屬性將一個規則集檔案附加到每個影像目錄 `attribute::RuleSetFile`。 雖然您可以隨時編輯規則集檔案，但僅當重新載入關聯的映像目錄時，映像伺服器才能識別更改。 當平台伺服器啟動或重新啟動時以及主目錄檔案(其具有 [!DNL .ini] 修改或「接觸」以更改檔案日期。

## 範例 {#section-aa769437d967459299b83a4bf34fe924}

**示例A。** 定義一個規則，如果影像名稱具有尾碼&quot; [!DNL _hg]「：

```
<rule> 
   <expression>(?i)_hg$</expression> 
   <substitution>\?&amp;qlt=95,1&amp;resmode=bicub</substitution> 
</rule>
```

規則表達式指定「」的不區分大小寫的匹配項 [!DNL _hg]&quot;。 尾碼將替換為更改影像質量設定的指定查詢字串。 請注意 `?` 替代字串中的字元將轉義，因為這是規則運算式中的一個特殊字元。

>[!NOTE]
>
>與符字元所需的編碼。 或者，替換字串可以包含在CDATA塊中：

`<substitution><![CDATA[&qlt=95,1&resmode=bicub]]></substitution>`

**示例B。** 特定Web應用程式不允許查詢字串。 定義轉換尾隨路徑元素的規則 `small`。 `medium`或 `large` 到模板，使用路徑的其餘部分作為影像名稱。 比如說， `myCat/myImage/small` 會轉換成 `myCat/smallTemplate?src=myCat/myImage`。

我們可以使用子字串來重構請求：

```
<rule> 
   <expression>([^/]+)/(small|medium|large)$</expression> 
   <substitution>$2Template?src=sample/$1</substitution> 
</rule>
```

## 另請參閱 {#section-9b748e7c5cff4759a70f96657bd43352}

[軟體包java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
