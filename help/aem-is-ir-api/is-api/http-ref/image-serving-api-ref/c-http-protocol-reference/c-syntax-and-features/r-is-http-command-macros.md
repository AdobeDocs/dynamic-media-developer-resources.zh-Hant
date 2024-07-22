---
title: 指令巨集
description: 指令巨集為指令集提供已命名的捷徑。 巨集是在個別的巨集定義檔案中定義，這些檔案可附加到影像目錄或預設目錄。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 304d93af-3427-4111-882a-35be9ec3aef5
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '311'
ht-degree: 0%

---

# 指令巨集{#command-macros}

指令巨集為指令集提供已命名的捷徑。 巨集是在個別的巨集定義檔案中定義，這些檔案可附加到影像目錄或預設目錄。

`$ *`名稱`*$`

<table id="simpletable_A03541622C354F60B5F304B999C4EF8E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname">名稱</span></span> </p> </td> 
  <td class="stentry"> <p>巨集名稱。 </p></td> 
 </tr> 
</table>

`*`name`*`不區分大小寫，而且可能包含ASCII字母、數字、&#39;-&#39;、&#39;_&#39;和&#39;.&#39;的任何組合 個字元。

巨集可在&#39;？&#39;之後的任何要求中叫用，也可在`catalog::Modifier`或`catalog::PostModifier`欄位中的任何地方叫用。 巨集只能代表一或多個、完整的「影像伺服」命令，而且必須以`&`分隔符號與其他命令分開。

在剖析期間，巨集引動詞在早期會被替代字串取代。 巨集內的命令會覆寫請求中的相同命令（如果這些命令發生在請求中的巨集呼叫之前）。 此處理流程不同於`catalog::Modifier`，其中要求字串中的命令一律會覆寫`catalog::Modifier`字串中的命令，無論要求中的位置為何。

命令巨集不能有引數值，但自訂變數可用來將要求中的值傳遞至巨集。

巨集可能是巢狀的。 不過，只有在巨集定義剖析時已定義巨集時，才能叫用巨集。 此工作流程是透過先出現在相同巨集定義檔案中，或將此類內嵌巨集的定義置於預設巨集定義檔案中來完成。

## 範例 {#section-2f73d36ac8d64254a03bae5afeae2fb9}

如果要將相同的屬性套用至不同的影像，巨集就相當有用。

`http://server/cat/1345?wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1 http://server/cat/1435?wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1 http://server/cat/8243?wid=480&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1`

您可以定義通用屬性的巨集：

`view wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1`

巨集的使用方式如下：

`http://server/cat/1345?$view$ http://server/cat/1435?$view$ http://server/cat/8243?$view$&wid=480`

因為`wid=`與第三個要求不同，您只需覆寫&#x200B;*after*&#x200B;值，即可叫用巨集（指定&#x200B;`wid=`*before* `$view$`無效）。

## 另請參閱 {#section-8cdba0ed2480444ca61e719e54f8871c}

[目錄：：MacroFile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-macrofile.md#reference-f91d717b3847458ca0f1fe95387554a2) ， [目錄：：Modifier](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md)， [巨集定義參考](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-macro-definition-reference/c-macro-definition-reference.md#concept-5ec73f7636c1496fba1e94094e694e79)
