---
description: 材質型錄提供多種功能。
solution: Experience Manager
title: 材料型錄*
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '305'
ht-degree: 0%

---


# 材料目錄*{#material-catalogs}

材質型錄提供多種功能。

* 允許對材料進行持久定義，包括所有材料屬性。

   在材料目錄中定義的材料可以使用簡單ID來參考，而不是使用一組材料屬性。
* 提供特定請求屬性的預設值，例如JPEG品質或預設回覆影像大小。
* 管理暈映、ICC設定檔和要求範本。

即使未定義特定的材料目錄，材料目錄的所有功能也可通過預設目錄([!DNL default.ini])使用。

雖然可使用材質屬性在要求中明確指定演算材質，但在許多情況下，最好使用材質目錄來隱藏網站上的材質詳細資訊。 src=命令接受目錄引用，而不是顯式檔案路徑。 目錄條目由` [ *[!DNL catId]*/] *[!DNL itemId]*`組成，其中` *[!DNL catId]*`標識物料目錄，` *[!DNL itemId]*`標識目錄中的記錄。 如果未指定` *[!DNL catId]*`，則會使用作業目錄（請參閱下面）。

如果(a)` *[!DNL catId]*`與材料目錄的`attribute::RootId`值匹配，並且(b)` *[!DNL recId]*`與同一目錄中的目錄：:Id值匹配，則目錄記錄將成功匹配。 如果匹配成功，則材料的屬性（包括`src=`）被設定為來自目錄記錄的資料。 如果MSS除了src=之外還包含此材料的其他屬性，則它們會覆蓋目錄記錄中的值。

如果` *[!DNL recId]*`無法與目錄條目匹配，則` *[!DNL catId]*`將從目錄中替換為`attribute::RootPath` ，然後將生成的路徑假定為簡單檔案路徑。 其他預設屬性(例如`attribute::Resolution`)也可從材料目錄繼承。

在類似材質本身及特定屬性的材質目錄中，可逐項列出暈映和ICC描述檔。 此外，暈映地圖也提供範本的容器。

**另請參閱**

物料目錄參考、[ `src=`](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272)、`attribute::RootId`、`attribute::RootPath`、`attribute::VignettePath`
