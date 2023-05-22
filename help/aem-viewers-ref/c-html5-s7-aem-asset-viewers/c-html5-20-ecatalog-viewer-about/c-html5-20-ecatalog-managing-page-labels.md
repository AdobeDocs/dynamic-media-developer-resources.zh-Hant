---
title: 管理頁面標籤
description: 管理頁面標籤
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: b62b5cb8-6100-4d0f-afd8-e6daa6ce6539
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 0%

---

# 管理頁面標籤{#managing-page-labels}

查看器用戶介面中有兩個位置顯示頁面標籤：縮略圖模式和目錄下拉框。

可以定義三種類型的標籤：

* 作者使用SYMBOL定位機制定義的標籤。
* 作者在後端定義的標籤，位於Dynamic Media Classic。
* 由查看器自動生成的標籤。

基於符號的標籤使用 `MediaSet.LABEL_XX[_YY]` 和 `MediaSet.LABEL_DELIM` SYMBOL（如所述） [用戶介面元素的本地化](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)。 您可以為整個對錄跨頁定義此類標籤，在這種情況下，應使用短SYMBOL語法( `MediaSet.LABEL_XX`)。 或者，使用完整SYMBOL語法為每個頁分別指定( `MediaSet.LABEL_XX_YY`)。

在對子目錄跨頁中的兩個頁面定義標籤時，查看器將使用 `MediaSet.LABEL_DELIM` 。 基於符號的標籤優先於在後端定義或由查看器自動生成的標籤。

在Dynamic Media Classic中定義的標籤儲存在單個頁面影像的UserData記錄中。 與基於SYMBOL的標籤相同。 即，如果對目錄跨頁中的兩個頁面都定義了標籤，則會使用 `MediaSet.LABEL_DELIM` 橫向模式下的SYMBOL。 Dynamic Media Classic標籤優先於自動生成的標籤，但由基於SYMBOL的標籤覆蓋。

自動生成的標籤是分配給目錄中所有頁面的順序編號。 如果給定跨頁定義了基於SYMBOL的標籤或定義了Dynamic Media Classic標籤，則會忽略該跨頁的自動生成的標籤。

在目錄中，可以使用 `showdefault` 的下界。
