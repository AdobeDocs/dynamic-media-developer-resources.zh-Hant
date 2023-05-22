---
description: 命令宏提供一組命令的命名快捷方式。 宏在單獨的宏定義檔案中定義，這些檔案可以附加到影像目錄或預設目錄。
solution: Experience Manager
title: 命令宏
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 304d93af-3427-4111-882a-35be9ec3aef5
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '312'
ht-degree: 1%

---

# 命令宏{#command-macros}

命令宏提供一組命令的命名快捷方式。 宏在單獨的宏定義檔案中定義，這些檔案可以附加到影像目錄或預設目錄。

`$ *`名稱`*$`

<table id="simpletable_A03541622C354F60B5F304B999C4EF8E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 名稱</span></span> </p> </td> 
  <td class="stentry"> <p>宏名稱。 </p></td> 
 </tr> 
</table>

`*`名稱`*` 不區分大小寫，並且可能包含ASCII字母、數字、「 — 」、「_」和「。」的任意組合 字元.

宏可以在「？」之後的請求中的任意位置以及 `catalog::Modifier` 或 `catalog::PostModifier` 的子菜單。 宏只能表示一個或多個完整的「影像服務」命令，並且必須與具有「&amp;」分隔符的其他命令分開。

宏調用在分析時被其替換字串提前替換。 如果宏中的命令在請求中調用宏之前發生，則宏中的命令將覆蓋請求中的相同命令。 這與 `catalog::Modifier`，其中，請求字串中的命令將始終覆蓋 `catalog::Modifier` 字串，而不管請求中的位置。

命令宏不能具有參數值，但可以使用自定義變數將值從請求傳遞到宏。

宏可以嵌套，但有以下限制：只有在分析宏定義時已定義宏時才可調用該宏，方法是在同一宏定義檔案中顯示得較早，或者將此類嵌入宏的定義放在預設宏定義檔案中。

## 範例 {#section-2f73d36ac8d64254a03bae5afeae2fb9}

如果將相同的屬性應用於不同的影像，則宏將非常有用。

`http://server/cat/1345?wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1 http://server/cat/1435?wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1 http://server/cat/8243?wid=480&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1`

我們可以為公共屬性定義一個宏：

`view wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1`

宏的使用方式如下：

`http://server/cat/1345?$view$ http://server/cat/1435?$view$ http://server/cat/8243?$view$&wid=480`

自 `wid=` 不同於第三個請求，我們只是覆蓋 *後* 調用宏(指定 `wid=`*先* `$view$` 不會有任何效果)。

## 另請參閱 {#section-8cdba0ed2480444ca61e719e54f8871c}

[目錄：：宏檔案](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-macrofile.md#reference-f91d717b3847458ca0f1fe95387554a2) 。 [目錄：：修改量](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md)。 [宏定義引用](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-macro-definition-reference/c-macro-definition-reference.md#concept-5ec73f7636c1496fba1e94094e694e79)
