---
description: 命令宏為一組命令提供了命名的快捷方式。 宏在單獨的宏定義檔案中定義，這些檔案可附加到影像目錄或預設目錄。
solution: Experience Manager
title: 命令宏
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 304d93af-3427-4111-882a-35be9ec3aef5
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '317'
ht-degree: 1%

---

# 命令宏{#command-macros}

命令宏為一組命令提供了命名的快捷方式。 宏在單獨的宏定義檔案中定義，這些檔案可附加到影像目錄或預設目錄。

`$ *`名稱`*$`

<table id="simpletable_A03541622C354F60B5F304B999C4EF8E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 名稱</span></span> </p> </td> 
  <td class="stentry"> <p>宏名稱。 </p></td> 
 </tr> 
</table>

`*``*` name不區分大小寫，並且可能包含ASCII字母、數字、「 — 」、「_」和「。」的任何組合。字元.

可以在「？」後的請求中的任意位置以及`catalog::Modifier`或`catalog::PostModifier`欄位內的任意位置調用宏。 宏只能表示一個或多個完整的Image Serving命令，並且必須與具有「&amp;」分隔符的其他命令分開。

在解析期間，宏調用會被其替代字串替換。 如果宏中的命令在請求中的宏調用之前發生，則這些命令將覆蓋請求中的相同命令。 這與`catalog::Modifier`不同，後者要求字串中的命令一律會覆寫`catalog::Modifier`字串中的命令，無論要求中的位置為何。

命令巨集不能有引數值，但可使用自訂變數將值從請求傳遞至巨集。

巨集可以巢狀，但有下列限制：僅當在分析宏定義時已定義宏時，才能調用該宏，方法是先前在同一宏定義檔案中顯示，或將此類嵌入宏的定義放在預設宏定義檔案中。

## 範例 {#section-2f73d36ac8d64254a03bae5afeae2fb9}

如果要將相同屬性套用至不同的影像，巨集將十分實用。

`http://server/cat/1345?wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1 http://server/cat/1435?wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1 http://server/cat/8243?wid=480&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1`

我們可以為公共屬性定義宏：

`view wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1`

宏的使用方式如下：

`http://server/cat/1345?$view$ http://server/cat/1435?$view$ http://server/cat/8243?$view$&wid=480`

由於第三個請求的`wid=`不同，因此我們只是在叫用宏的&#x200B;*之後覆寫值*（在&#x200B;*`$view$`之前指定`wid=`*&#x200B;將不會產生任何效果）。

## 另請參閱 {#section-8cdba0ed2480444ca61e719e54f8871c}

[catalog::MacroFile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-macrofile.md#reference-f91d717b3847458ca0f1fe95387554a2) ,  [catalog::Modifier](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md)，宏定義 [參考](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-macro-definition-reference/c-macro-definition-reference.md#concept-5ec73f7636c1496fba1e94094e694e79)
