---
title: 規則
description: 請求規則元素。 一個或多個規則在 <ruleset> 的子菜單。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4fabd469-c80c-422a-80b0-3d31ce191d58
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 6%

---

# 規則{#rule}

請求規則元素。 一個或多個規則在 `<ruleset>` 的子菜單。

## 屬性 {#section-d4a3b0496c0c4aa5bd7da87203b9379b}

`OnMatch = "break" | "continue" | "error"`: 選擇性. 預設值為&quot;break&quot;。

`Replace = "first" | "all"`: 選擇性. 預設值為「first」。

`RequestType` = *&quot;`types`&quot;*:可選。 指定規則應用於的輸入上下文。 *`types`* 是逗號分隔的清單，其中可能包含下表中列出的一個或多個令牌。 如果 `RequestType` 未指定，該規則適用於所有受支援上下文上接收的請求。

<table id="table_4935E1ED03624DA6AF3F8DC9AAA10237"> 
 <thead> 
  <tr> 
   <th class="entry"> <p><b>代號</b> </p> </th> 
   <th class="entry"> <p><b>上下文</b> </p> </th> 
   <th class="entry"> <p><b>說明</b> </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> 是</span> </p> </td> 
   <td> <p> <span class="filepath"> /is/image//</span> </p> </td> 
   <td> <p>應用於映像服務請求 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 紅</span> </p> </td> 
   <td> <p> <span class="filepath"> /ir/render/</span> </p> </td> 
   <td> <p>應用於影像呈現請求 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 靜態</span> </p> </td> 
   <td> <p> <span class="filepath"> /is/content//</span> </p> </td> 
   <td> <p>應用於靜態內容請求 </p> </td> 
  </tr> 
 </tbody> 
</table>

**`Name = "text"`**: 選擇性. 用於標識 `<rule>` 調試日誌和錯誤消息中的元素。

`  *`屬性`* ="value"`:可選。 `<rule>` 元素可以在任何組合中定義以下任何屬性。 如果指定，並且規則成功匹配，則它們將覆蓋此請求的相應目錄屬性。 預設為 `RequestType="is"`.

<table id="table_67AED5BEADDF4DAC99B5EF46438C1ABC"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <span class="varname"> 屬性 </span> </b> </th> 
   <th class="entry"> <p>相應的影像目錄屬性 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> 預設影像模式</span> </p> </td> 
   <td> <p><a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultimagemode.md#reference-8a996af162f84e46bbe9e6e0d4e26782" type="reference" format="dita" scope="local"> 屬性：:DefaultImageMode</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 錯誤影像</span> </p> </td> 
   <td> <p><a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c" type="reference" format="dita" scope="local"> 屬性：:ErrorImage</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 過期</span> </p> </td> 
   <td> <p> <a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-expiration.md#reference-a0bf4686425d4e00b8014c4950fb62b7" type="reference" format="dita" scope="local"> 屬性：：到期</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 最大圖</span> </p> </td> 
   <td> <p><a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5" type="reference" format="dita" scope="local"> 屬性：:MaxPix </a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 請求鎖</span> </p> </td> 
   <td> <p> <a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestlock.md#reference-8bbe2f581be847d3b9fa123e8e5e94b0" type="reference" format="dita" scope="local"> 屬性：:RequestLock</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 請求模糊處理</span> </p> </td> 
   <td> <p> <a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestobfuscation.md#reference-730a3330253343f893419ebd52baf0bd" type="reference" format="dita" scope="local"> 屬性：:RequestObfuscation</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 根URL</span> </p> </td> 
   <td> <p> <a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rooturl.md#reference-3b0e43881020409cbe642366913cf137" type="reference" format="dita" scope="local"> 屬性：:RootUrl</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 保存路徑</span> </p> </td> 
   <td> <p> <a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-savepath.md#reference-9c4686dc153b41d8a0751cde83615432" type="reference" format="dita" scope="local"> 屬性：:SavePath</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 水印</span> </p> </td> 
   <td> <p><a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-watermark.md#reference-942b50acb2dd43a5ae498dc41ea9ac9b" type="reference" format="dita" scope="local"> 屬性：：水印</a> </p> </td> 
  </tr> 
 </tbody> 
</table>

有關詳細資訊，請參閱相應影像目錄屬性的說明。

到期屬性只覆蓋預設屬性值。 如果特定 `catalog::Expiration` 值適用於請求。

## 資料 {#section-8fce013a4c724da58af3fee4e7a90e72}

<table id="simpletable_4F1C03671DA942A3A332B2C686A63C52"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> &lt;expression&gt;</span> </p></td> 
  <td class="stentry"> <p>選擇性 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> &lt;substitution&gt;</span> </p></td> 
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

如果兩者都 `<expression>` 和 `<substitution>` 指定，且未使用捕獲的子字串，則第一個匹配的子字串將替換為 `<substitution>`。

如果 `<expression>` 未指定，任何路徑匹配和 `<substitution>` 添加到路徑的末尾。

如果 `<substitution>` 未指定，未發生路徑或查詢轉換，但所有指定的目錄屬性都被覆蓋。 如果 `<substitution>` 為空，將刪除匹配的子字串。

的 `<addressfilter>` 僅在出現匹配時和應用查詢規則之前應用。
