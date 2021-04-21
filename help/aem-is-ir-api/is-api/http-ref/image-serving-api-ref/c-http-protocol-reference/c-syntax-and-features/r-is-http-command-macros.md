---
description: 命令宏為命令集提供命名快捷方式。 宏在單獨的宏定義檔案中定義，這些宏定義檔案可以附加到影像目錄或預設目錄。
solution: Experience Manager
title: 命令宏
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '320'
ht-degree: 1%

---


# 命令宏{#command-macros}

命令宏為命令集提供命名快捷方式。 宏在單獨的宏定義檔案中定義，這些宏定義檔案可以附加到影像目錄或預設目錄。

`$ *`名稱`*$`

<table id="simpletable_A03541622C354F60B5F304B999C4EF8E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 名稱</span></span> </p> </td> 
  <td class="stentry"> <p>宏名稱。 </p></td> 
 </tr> 
</table>

`*`名`*` 稱不區分大小寫，可能由ASCII字母、數字、&#39;-&#39;、&#39;_&#39;和&#39;.&#39;的任意組合組成。字元.

宏可在&#39;?&#39;後的請求中的任意位置以及`catalog::Modifier`或`catalog::PostModifier`欄位內的任意位置被調用。 宏只能表示一個或多個完整的「影像服務」命令，並且必須與具有「&amp;」分隔符的其它命令分開。

宏調用在解析期間早被其替代字串替換。 如果宏中的命令在請求中調用宏之前發生，則它們將覆蓋請求中的相同命令。 這與`catalog::Modifier`不同，在中，無論請求中的位置如何，請求字串中的命令一律會覆寫`catalog::Modifier`字串中的命令。

命令宏不能有參數值，但可使用自定義變數將值從請求傳遞到宏。

宏可以嵌套，但有以下限制：僅當在解析宏定義時已定義宏時，才可調用宏，方法是在同一宏定義檔案中顯示較早，或將此類嵌入宏的定義放置在預設宏定義檔案中。

## 範例 {#section-2f73d36ac8d64254a03bae5afeae2fb9}

如果要將相同的屬性應用到不同的影像，則宏非常有用。

`http://server/cat/1345?wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1 http://server/cat/1435?wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1 http://server/cat/8243?wid=480&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1`

我們可以為公共屬性定義一個宏：

`view wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1`

宏的用法如下：

`http://server/cat/1345?$view$ http://server/cat/1435?$view$ http://server/cat/8243?$view$&wid=480`

由於`wid=`與第三個請求不同，我們只要在呼叫宏&#x200B;*之後覆寫值*（在&#x200B;*`$view$`之前指定`wid=`*&#x200B;將不會有任何作用）。

## 另請參閱 {#section-8cdba0ed2480444ca61e719e54f8871c}

[catalog:::MacroFile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-macrofile.md#reference-f91d717b3847458ca0f1fe95387554a2) , catalog [::Modifier](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md) [, Macro Definition Reference](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-macro-definition-reference/c-macro-definition-reference.md#concept-5ec73f7636c1496fba1e94094e694e79)
