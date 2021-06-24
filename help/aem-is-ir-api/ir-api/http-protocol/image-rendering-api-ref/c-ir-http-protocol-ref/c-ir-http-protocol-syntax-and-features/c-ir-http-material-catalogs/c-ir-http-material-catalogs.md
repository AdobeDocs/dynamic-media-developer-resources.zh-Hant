---
description: 材料目錄提供多種功能。
solution: Experience Manager
title: 材料目錄*
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 502f80f5-fdd1-468b-89a9-64cc9128d655
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 0%

---

# 材料目錄*{#material-catalogs}

材料目錄提供多種功能。

* 允許對材料進行持久定義，包括所有材料屬性。

   材料目錄中定義的材料可以使用簡單ID來引用，而不是使用一組材料屬性。
* 提供特定請求屬性的預設值，例如JPEG品質或預設回覆影像大小。
* 管理暈映、ICC設定檔和請求範本。

即使未定義特定材料目錄，材料目錄的所有功能也可通過預設目錄([!DNL default.ini])獲得。

雖然可以在使用材料屬性的請求中明確指定呈現材料，但在許多情況下，最好使用材料目錄從網站隱藏材料的詳細資訊。 src=命令接受目錄引用，而不是顯式檔案路徑。 目錄條目由` [ *[!DNL catId]*/] *[!DNL itemId]*`組成，其中` *[!DNL catId]*`標識物料目錄，` *[!DNL itemId]*`標識目錄中的記錄。 如果未指定` *[!DNL catId]*`，則使用會話目錄（請參見下面）。

如果(a)` *[!DNL catId]*`符合物料目錄的`attribute::RootId`值，且(b)` *[!DNL recId]*`符合相同目錄中的目錄：:Id值，則目錄記錄會成功匹配。 如果匹配成功，則將材料的屬性（包括`src=`）設定為來自目錄記錄的資料。 如果MSS除了src=之外還包含此材料的其他屬性，則它們將覆蓋目錄記錄中的值。

如果` *[!DNL recId]*`不能與目錄項匹配，則` *[!DNL catId]*`將從目錄中替換為`attribute::RootPath`，然後將生成的路徑假定為簡單檔案路徑。 其他預設屬性(例如`attribute::Resolution`)也可以從材料目錄中繼承。

可以在材料目錄中逐項列出與材料本身相似的暈映和ICC配置檔案，並且可以指定屬性。 此外，暈映圖也提供範本的容器。

**另請參閱**

材料目錄參考， [ `src=`](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272), `attribute::RootId`, `attribute::RootPath`, `attribute::VignettePath`
