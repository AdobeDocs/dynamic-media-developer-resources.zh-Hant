---
description: 影像演算支援簡單的要求前置處理機制，此機制以規則運算式比對和替代規則為基礎。
solution: Experience Manager
title: 規則集參考
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 194600d0-72d9-47fb-8525-598beb2ce17d
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '619'
ht-degree: 0%

---

# 規則集參考{#rule-set-reference}

影像演算支援簡單的要求前置處理機制，此機制以規則運算式比對和替代規則為基礎。

<!--<a id="section_F44601A65CE1451EAD0A449C66B773CC"></a>-->

前置處理規則的集合（*規則集*）可以附加到材質目錄或預設目錄。 只有當請求未附加特定材質目錄時，才會套用預設目錄中的規則。

請求前置處理規則可在伺服器的請求剖析器處理請求之前，修改請求的路徑和查詢部分，包括操作路徑、新增命令、變更命令值，以及套用範本或巨集。 規則也可用來設定和覆寫某些目錄屬性，以及限制服務給特定使用者端IP位址。

規則集會儲存為XML檔案檔案。 必須在`attribute::RuleSetFile`中指定規則集檔案的相對或絕對路徑。

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

在有效的規則集XML檔案中，`<?xml>`、`<!DOCTYPE>`和`<ruleset>`專案永遠是必要的，即使未定義實際規則。

允許一個包含任意數目`<ruleset>`個元素的`<rule>`元素。

預先處理規則檔案的內容區分大小寫。

## URL前置處理 {#section-737a38d1b8c746f995e64fa6cfbcec87}

在任何其他處理作業之前，會先對傳入的HTTP要求進行部分解析，以決定應套用哪些材質目錄。 識別目錄後，將套用所選目錄的規則集（或預設目錄，如果未識別特定目錄）。

`<rule>`元素會依照指定的順序搜尋，以符合`<expression>`元素( *`expression`*)的內容。

如果符合`<rule>`，則會套用選用的&#x200B;*`substitution`*，並將修改過的要求字串傳遞給伺服器的要求剖析器，以進行正常處理。

如果到達`<ruleset>`的結尾時未成功比對，則未修改即會將要求傳遞至剖析器。

## OnMatch屬性 {#section-7a8ad3597780486985af5e9a3b1c7b56}

可以使用`OnMatch`專案的`<rule>`屬性修改預設行為。 `OnMatch`可設為`break` （預設）、`continue`或`error.`

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
   <td colname="col2"> <p>在套用此規則的替代之後，規則處理會立即終止。 預設。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> &lt;rule OnMatch="continue"&gt;</span> </p> </td> 
   <td colname="col2"> <p>會套用替代，並會繼續處理下一個規則。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> &lt;rule OnMatch="error"&gt;</span> </p> </td> 
   <td colname="col2"> <p>規則處理會立即終止，且「已拒絕要求」回應狀態會傳回給使用者端。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 覆寫目錄屬性 {#section-1f59ce84234f4576ba8473b0e6ba22ee}

當規則成功比對且已設定`<rule>`時，`OnMatch="break"`元素可選擇定義覆寫對應目錄屬性的屬性。 若已設定`OnMatch="continue"`，則不會套用任何屬性。 如需可透過規則控制的屬性清單，請參閱`<rule>`的說明。

## 規則運算式 {#section-4d326507b52544b0960a9a5f303e3fe6}

簡單字串比對適用於非常基本的應用程式，但在大多數情況下都需要規則運算式。 雖然規則運算式是符合業界標準的，但具體的實施會因例項而異。

[封裝java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)說明「影像伺服」使用的特定規則運算式實作。

## 擷取的子字串 {#section-8057cd65d48949ffb6a50e929bd3688b}

為了便於修改複雜的URL，您可以在運算式中擷取子字串，方法是以括弧(...)括住子字串。 擷取的子字串會根據前括弧的位置，從1開始依序編號。 擷取的子字串可以使用&#x200B;*`$n`*&#x200B;插入替代中，其中&#x200B;*`n`*&#x200B;是擷取的子字串的序號。

## 管理規則集檔案 {#section-e8ce976b56404c009496426fd334d23d}

一個規則集檔案可附加至每個具有目錄屬性`attribute::RuleSetFile`的材料目錄。 雖然您可以隨時編輯規則集檔案，但影像伺服器只有在重新載入關聯的材質目錄時，才會辨識變更。 當[!DNL Platform Server]啟動或重新啟動時，以及當主要目錄檔案（具有[!DNL .ini]檔案字尾）被修改或「接觸」（以變更檔案日期）時，就會發生這種情況。

## 範例 {#section-c4142a41f5cd4ff799a72fbc130c3700}

規則集範例位於影像伺服檔案中影像目錄參考的對應區段中。

## 另請參閱 {#section-cdaacf84f92c4bffbb4b76197b4e531a}

[封裝java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
