---
description: 影像渲染支援基於規則運算式匹配和替換規則的簡單請求預處理機制。
solution: Experience Manager
title: 規則集引用
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 194600d0-72d9-47fb-8525-598beb2ce17d
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '632'
ht-degree: 0%

---

# 規則集引用{#rule-set-reference}

影像渲染支援基於規則運算式匹配和替換規則的簡單請求預處理機制。

<!--<a id="section_F44601A65CE1451EAD0A449C66B773CC"></a>-->

預處理規則的集合(*規則集*)可附加到材料目錄或預設目錄。 僅當請求未附加特定物料目錄時，預設目錄中的規則才適用。

請求預處理規則可以在請求由伺服器的請求分析器處理之前修改請求的路徑和查詢部分，包括操作路徑、添加命令、更改命令值以及應用模板或宏。 規則還可用於配置和覆蓋某些目錄屬性，以及將服務限制到特定客戶端IP地址。

規則集以XML文檔檔案形式儲存。 必須在中指定規則集檔案的相對路徑或絕對路徑 `attribute::RuleSetFile`。

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

的 `<?xml>`。 `<!DOCTYPE>` 和 `<ruleset>` 有效規則集XML檔案中始終需要元素，即使未定義任何實際規則。

一 `<ruleset>` 包含任意數量的元素 `<rule>` 元素。

預處理規則檔案的內容區分大小寫。

## URL預處理 {#section-737a38d1b8c746f995e64fa6cfbcec87}

在進行任何其他處理之前，將部分分析傳入的HTTP請求以確定應應用哪些材料目錄。 一旦標識了目錄，則應用所選目錄（或預設目錄，如果未標識特定目錄）的規則集。

的 `<rule>` 按為與元素的內容匹配而指定的順序搜索元素 `<expression>` 元素(E) *`expression`*)。

如果 `<rule>` 匹配，可選 *`substitution`* 應用並將修改的請求字串傳遞給伺服器的請求解析器以進行正常處理。

如果在 `<ruleset>` 訪問時，請求將傳遞給解析器，而不進行修改。

## OnMatch屬性 {#section-7a8ad3597780486985af5e9a3b1c7b56}

可以使用 `OnMatch` 屬性 `<rule>` 元素。 `OnMatch` 可能設定為 `break` （預設）, `continue`或 `error.`

<table id="table_4CABF55B33854A128D5F326B31C6C397"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>元素和屬性 </p> </th> 
   <th colname="col2" class="entry"> <p>匹配時的行為 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> &lt;rule OnMatch="break"&gt;</span> </p> </td> 
   <td colname="col2"> <p>應用此規則的替代後，規則處理即終止。 預設. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> &lt;rule OnMatch="continue"&gt;</span> </p> </td> 
   <td colname="col2"> <p>應用替代，並繼續處理下一個規則。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> &lt;rule OnMatch="error"&gt;</span> </p> </td> 
   <td colname="col2"> <p>規則處理立即終止，並且「請求拒絕」響應狀態返回給客戶端。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 覆蓋目錄屬性 {#section-1f59ce84234f4576ba8473b0e6ba22ee}

`<rule>` 元素可以根據需要定義在規則成功匹配時覆蓋相應目錄屬性的屬性， `OnMatch="break"` 的子菜單。 如果 `OnMatch="continue"` 的子菜單。 請參閱 `<rule>` 的子菜單。

## 規則運算式 {#section-4d326507b52544b0960a9a5f303e3fe6}

簡單字串匹配適用於非常基本的應用程式，但大多數實例都需要規則運算式。 雖然規則運算式是行業標準，但具體實現因實例而異。

[軟體包java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/) 描述Image Service使用的特定規則運算式實現。

## 捕獲的子字串 {#section-8057cd65d48949ffb6a50e929bd3688b}

為便於對複雜URL進行修改，可以通過用括弧(...)將子字串括起來，在表達式中捕獲子字串。 捕獲的子字串根據前括弧的位置以1開始按順序編號。 捕獲的子字串可以使用 *`$n`*，也請參見Wiki頁。 *`n`* 是捕獲的子字串的序列號。

## 管理規則集檔案 {#section-e8ce976b56404c009496426fd334d23d}

一個規則集檔案可以附加到具有目錄屬性的每個材料目錄 `attribute::RuleSetFile`。 雖然您可以隨時編輯規則集檔案，但影像伺服器僅在重新載入關聯的材料目錄時才識別更改。 當 [!DNL Platform Server] 啟動或重新啟動主目錄檔案(其 [!DNL .ini] 檔案尾碼)被修改或「接觸」（以更改檔案日期）。

## 範例 {#section-c4142a41f5cd4ff799a72fbc130c3700}

規則集示例在映像服務文檔的映像目錄參考的相應部分中提供。

## 另請參閱 {#section-cdaacf84f92c4bffbb4b76197b4e531a}

[軟體包java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
