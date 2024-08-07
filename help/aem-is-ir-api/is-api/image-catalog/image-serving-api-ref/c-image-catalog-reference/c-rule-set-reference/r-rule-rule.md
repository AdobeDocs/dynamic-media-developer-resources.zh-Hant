---
title: 規則
description: 要求規則元素。 <ruleset>元素中的一個或多個規則是選用的。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4fabd469-c80c-422a-80b0-3d31ce191d58
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 3%

---

# 規則{#rule}

要求規則元素。 `<ruleset>`專案中的一或多個規則是選用的。

## 屬性 {#section-d4a3b0496c0c4aa5bd7da87203b9379b}

`OnMatch = "break" | "continue" | "error"`：選擇性。 預設值為「break」。

`Replace = "first" | "all"`：選擇性。 預設值為「first」。

`RequestType` = *&quot;`types`&quot;*：選擇性。 指定規則套用的輸入內容。 *`types`*&#x200B;是以逗號分隔的清單，可能包含下表所列的一或多個權杖。 如果未指定`RequestType`，則規則會套用至在所有支援的內容上收到的要求。

<table id="table_4935E1ED03624DA6AF3F8DC9AAA10237"> 
 <thead> 
  <tr> 
   <th class="entry"> <p><b>權杖</b> </p> </th> 
   <th class="entry"> <p><b>內容</b> </p> </th> 
   <th class="entry"> <p><b>描述</b> </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph">是</span> </p> </td> 
   <td> <p> <span class="filepath"> /is/image/</span> </p> </td> 
   <td> <p>套用至影像伺服請求 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> ir</span> </p> </td> 
   <td> <p> <span class="filepath"> /ir/render/</span> </p> </td> 
   <td> <p>套用至影像演算要求 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">靜態</span> </p> </td> 
   <td> <p> <span class="filepath"> /is/content/</span> </p> </td> 
   <td> <p>套用至靜態內容要求 </p> </td> 
  </tr> 
 </tbody> 
</table>

**`Name = "text"`**：選擇性。 用於識別偵錯記錄檔和錯誤訊息中的`<rule>`專案。

`  *`屬性`* ="value"`：選擇性。 `<rule>`元素可以任意組合方式定義下列任何屬性。 如果已指定，且規則已成功比對，則會覆寫此請求對應的目錄屬性。 預設值為`RequestType="is"`。

<table id="table_67AED5BEADDF4DAC99B5EF46438C1ABC"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <span class="varname">屬性</span> </b> </th> 
   <th class="entry"> <p>對應的影像目錄屬性 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> DefaultImageMode</span> </p> </td> 
   <td> <p><a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultimagemode.md#reference-8a996af162f84e46bbe9e6e0d4e26782" type="reference" format="dita" scope="local">屬性：：DefaultImageMode</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> ErrorImage</span> </p> </td> 
   <td> <p><a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c" type="reference" format="dita" scope="local">屬性：：ErrorImage</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">到期</span> </p> </td> 
   <td> <p> <a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-expiration.md#reference-a0bf4686425d4e00b8014c4950fb62b7" type="reference" format="dita" scope="local">屬性：：Expiration</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> MaxPix</span> </p> </td> 
   <td> <p><a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5" type="reference" format="dita" scope="local">屬性：：MaxPix </a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> RequestLock</span> </p> </td> 
   <td> <p> <a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestlock.md#reference-8bbe2f581be847d3b9fa123e8e5e94b0" type="reference" format="dita" scope="local">屬性：：RequestLock</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> RequestObfuscation</span> </p> </td> 
   <td> <p> <a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestobfuscation.md#reference-730a3330253343f893419ebd52baf0bd" type="reference" format="dita" scope="local">屬性：：RequestObfuscation</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> RootUrl</span> </p> </td> 
   <td> <p> <a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rooturl.md#reference-3b0e43881020409cbe642366913cf137" type="reference" format="dita" scope="local">屬性：：RootUrl</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> SavePath</span> </p> </td> 
   <td> <p> <a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-savepath.md#reference-9c4686dc153b41d8a0751cde83615432" type="reference" format="dita" scope="local">屬性：：SavePath</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">水印</span> </p> </td> 
   <td> <p><a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-watermark.md#reference-942b50acb2dd43a5ae498dc41ea9ac9b" type="reference" format="dita" scope="local">屬性：：WaterMark</a> </p> </td> 
  </tr> 
 </tbody> 
</table>

如需詳細資訊，請參閱對應影像目錄屬性的說明。

Expiration屬性只會覆寫預設屬性值。 如果特定的`catalog::Expiration`值套用至要求，則忽略覆寫。

## 資料 {#section-8fce013a4c724da58af3fee4e7a90e72}

<table id="simpletable_4F1C03671DA942A3A332B2C686A63C52"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> &lt;運算式&gt;</span> </p></td> 
  <td class="stentry"> <p>選擇性 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> &lt;替代&gt;</span> </p></td> 
  <td class="stentry"> <p>選擇性 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> &lt;addressfilter&gt;</span> </p></td> 
  <td class="stentry"> <p>選擇性 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> &lt;header&gt;</span> </p></td> 
  <td class="stentry"> <p>選擇性 </p></td> 
 </tr> 
</table>

## 附註 {#section-0c5fbc363070419d8c9800b0c02dc9f9}

如果同時指定`<expression>`和`<substitution>`，但未使用擷取的子字串，則第一個相符的子字串會取代為`<substitution>`。

如果未指定`<expression>`，則所有路徑皆相符，且`<substitution>`會附加至路徑的結尾。

如果未指定`<substitution>`，則不會發生路徑或查詢轉換，但會覆寫任何指定的目錄屬性。 如果`<substitution>`為空白，則會移除相符的子字串。

`<addressfilter>`只會在符合發生時套用，並在套用查詢規則之前套用。
