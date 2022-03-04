---
title: 物料目錄
description: 材料目錄提供多種功能。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 502f80f5-fdd1-468b-89a9-64cc9128d655
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 0%

---

# 物料目錄 {#material-catalogs}

材料目錄提供多種功能。

* 允許對材料進行持久定義，包括所有材料屬性。

   在材料目錄中定義的材料可以使用簡單ID來參照，而不是使用一組材料屬性。
* 為某些請求屬性(如JPEG質量或預設回復影像大小)提供預設值。
* 管理小節、ICC配置檔案和請求模板。

即使未定義特定的材料目錄，材料目錄的所有特徵也可通過預設目錄( [!DNL default.ini])。

雖然可以使用材料屬性在請求中顯式指定渲染材料，但通常更希望使用材料目錄從網站中隱藏材料的詳細資訊。 src=命令接受目錄引用，而不是顯式檔案路徑。 目錄條目由 ` [ *[!DNL catId]*/] *[!DNL itemId]*`，也請參見Wiki頁。 ` *[!DNL catId]*` 標識物料目錄 ` *[!DNL itemId]*` 標識目錄中的記錄。 如果 ` *[!DNL catId]*` 未指定，將使用會話目錄（請參閱下面）。

如果(a)，則目錄記錄匹配成功 ` *[!DNL catId]*` 與 `attribute::RootId` (b)物料目錄及(b) ` *[!DNL recId]*` 與同一目錄中的目錄：:Id值匹配。 如果匹配成功，則物料的屬性(包括 `src=`)。 如果MSS除了src=之外還包括此材料的其他屬性，則它們會覆蓋目錄記錄中的值。

如果 ` *[!DNL recId]*` 無法與目錄條目匹配， ` *[!DNL catId]*` 替換為 `attribute::RootPath` 然後，將生成的路徑假定為簡單的檔案路徑。 其他預設屬性(例如， `attribute::Resolution`)也可從材料目錄中繼承。

可以在材料目錄中逐項列出與材料本身相似的材料和給定屬性。 此外，vignette映射還為模板提供了容器。

**另請參閱**

物料目錄參考， [ `src=`](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272)。 `attribute::RootId`。 `attribute::RootPath`。 `attribute::VignettePath`
