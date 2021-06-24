---
description: 管理頁面標籤
solution: Experience Manager
title: 管理頁面標籤
feature: Dynamic Media Classic，檢視器，SDK/API,eCatalog搜尋
role: Developer,Business Practitioner
exl-id: 73c3904f-678f-47c4-b895-86671402df79
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 0%

---

# 管理頁面標籤{#managing-page-labels}

檢視器使用者介面中有兩個位置會顯示頁面標籤：縮圖模式和目錄下拉式清單。

可定義的標籤類型有三種：

* 由作者使用SYMBOL定位機制定義的標籤。
* 由作者在後端、Dynamic Media Classic內定義的標籤。
* 檢視器自動產生的標籤。

基於符號的標籤使用`MediaSet.LABEL_XX[_YY]`和`MediaSet.LABEL_DELIM` SYMBOL定義，如[用戶介面元素的本地化](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)中所述。 您可以為整個ecatalog跨頁定義此類標籤，在這種情況下，您應使用短的SYMBOL語法(`MediaSet.LABEL_XX`)。 或者，使用完整的SYMBOL語法(`MediaSet.LABEL_XX_YY`)為每個頁面分別指定它。

當您為ecatalog跨頁中的兩個頁面定義標籤時，檢視器會使用`MediaSet.LABEL_DELIM` SYMBOL將這些標籤串連成一個字串。 以SYMBOL為基礎的標籤優先於在後端定義或由檢視器自動產生標籤的標籤。

在Dynamic Media Classic中定義的標籤會儲存在個別頁面影像的UserData記錄中。 與基於SYMBOL的標籤相同。 也就是說，如果ecatalog跨頁中的兩個頁面都已定義標籤，則會在橫向模式中使用`MediaSet.LABEL_DELIM` SYMBOL來串連這些頁面。 Dynamic Media Classic標籤優先於自動產生的標籤，但是以SYMBOL為基礎的標籤所覆寫。

自動產生的標籤是指派給ecatalog中所有頁面的循序編號。 如果指定的跨頁已定義SYMBOL型標籤或已定義Dynamic Media Classic標籤，則會忽略自動產生的標籤。

在目錄中，可使用`showdefault`參數停用自動產生標籤的顯示。
