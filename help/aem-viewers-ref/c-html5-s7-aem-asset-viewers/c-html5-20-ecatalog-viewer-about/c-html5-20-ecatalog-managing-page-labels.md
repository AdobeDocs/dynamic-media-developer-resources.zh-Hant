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

檢視器使用者介面中有兩個位置會顯示頁面標籤：縮圖模式和目錄下拉式清單。

可定義的標籤類型有三種：

* 由作者使用SYMBOL定位機制定義的標籤。
* 由作者在後端、Dynamic Media Classic內定義的標籤。
* 檢視器自動產生的標籤。

SYMBOL型標籤的定義使用 `MediaSet.LABEL_XX[_YY]` 和 `MediaSet.LABEL_DELIM` 符號，如 [用戶介面元素本地化](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74). 您可以為整個ecatalog跨頁定義此類標籤，在這種情況下，您應使用簡短的SYMBOL語法( `MediaSet.LABEL_XX`)。 或者，使用完整的SYMBOL語法( `MediaSet.LABEL_XX_YY`)。

當您為ecatalog跨頁中的兩個頁面定義標籤時，檢視器會使用 `MediaSet.LABEL_DELIM` 符號。 以SYMBOL為基礎的標籤優先於在後端定義或由檢視器自動產生標籤的標籤。

在Dynamic Media Classic中定義的標籤會儲存在個別頁面影像的UserData記錄中。 與基於SYMBOL的標籤相同。 也就是說，如果ecatalog跨頁中的兩個頁面皆已定義標籤，則會使用 `MediaSet.LABEL_DELIM` 橫向模式中的符號。 Dynamic Media Classic標籤優先於自動產生的標籤，但是以SYMBOL為基礎的標籤所覆寫。

自動產生的標籤是指派給ecatalog中所有頁面的循序編號。 如果給定的跨頁已定義基於符號的標籤或已定義Dynamic Media Classic標籤，則會忽略自動生成的標籤。

在目錄中，可以使用 `showdefault` 參數。
