---
title: 材質目錄
description: 材料目錄提供幾個功能。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 502f80f5-fdd1-468b-89a9-64cc9128d655
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '298'
ht-degree: 0%

---

# 材質目錄 {#material-catalogs}

材料目錄提供幾個功能。

* 允許持續定義材料，包括所有材料屬性。

  在材料目錄中定義的材料可以使用簡單ID來參照，而不是使用一組材料屬性。
* 為特定請求屬性提供預設值，例如JPEG品質或預設回覆影像大小。
* 管理暈映、ICC設定檔和請求範本。

即使未定義特定的材料目錄，材料目錄的所有特徵仍可透過預設目錄( [!DNL default.ini])。

雖然轉譯資料可以使用資料屬性在請求中明確指定，但通常更希望使用資料目錄來隱藏網站的資料細節。 src=命令接受目錄參照，而非明確的檔案路徑。 目錄專案包含 ` [ *[!DNL catId]*/] *[!DNL itemId]*`，其中 ` *[!DNL catId]*` 會識別材質目錄和 ` *[!DNL itemId]*` 會識別目錄中的記錄。 如果 ` *[!DNL catId]*` 未指定，則會使用工作階段目錄（請參閱下文）。

目錄記錄符合成功，如果(a) ` *[!DNL catId]*` 符合 `attribute::RootId` 材質目錄和(b)的值 ` *[!DNL recId]*` 和相同目錄中的catalog：：Id值相符。 如果有成功的相符專案，則材料的屬性(包括 `src=`)設定為目錄記錄中的資料。 如果MSS包含src=以外的其他材質屬性，則會覆寫目錄記錄中的值。

如果 ` *[!DNL recId]*` 無法比對至目錄專案，則 ` *[!DNL catId]*` 已取代為 `attribute::RootPath` 之後，會將目錄和產生的路徑假設為簡單的檔案路徑。 其他預設屬性(例如， `attribute::Resolution`)也可以繼承自材質目錄。

暈映和ICC輪廓可在與材料本身類似的材料目錄中逐項列出，以及指定的屬性。 此外，暈映對應也提供範本的容器。

**另請參閱**

材質目錄參考， [`src=`](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272)， `attribute::RootId`， `attribute::RootPath`， `attribute::VignettePath`
