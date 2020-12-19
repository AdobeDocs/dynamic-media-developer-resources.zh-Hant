---
description: 'null'
seo-description: 'null'
seo-title: 管理頁面標籤
solution: Experience Manager
title: 管理頁面標籤
topic: Dynamic media
uuid: ab3df37d-113b-4762-ba9c-b92ffc41f1a2
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 0%

---


# 管理頁面標籤{#managing-page-labels}

檢視器使用者介面中有兩個位置會顯示頁面標籤：縮圖模式和目錄下拉式清單。

可以定義三種標籤類型：

* 作者使用SYMBOL定位機制定義的標籤。
* 由作者在後端（位於SPS內）定義的標籤。
* 檢視器自動產生的標籤。

基於符號的標籤使用`MediaSet.LABEL_XX[_YY]`和`MediaSet.LABEL_DELIM` SYMBOL定義，如[用戶介面元素的本地化中所述。 ](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)您可以為整個ecatalog跨頁定義此類標籤，在這種情況下，您應使用簡短的SYMBOL語法(`MediaSet.LABEL_XX`)。 或者，使用完整的SYMBOL語法(`MediaSet.LABEL_XX_YY`)分別為每個頁面指定。

當您在ecatalog跨頁中定義兩個頁面的標籤時，檢視器會使用`MediaSet.LABEL_DELIM` SYMBOL將這些標籤串連成一個字串。 SYMBOL型標籤優先於在後端定義或檢視器自動產生標籤的標籤。

在SPS中定義的標籤會儲存在個別頁面影像的使用者資料記錄中。 與SYMBOL型標籤相同。 也就是說，如果ecatalog跨頁中的兩個頁面都定義了標籤，則它們會在橫向模式下使用`MediaSet.LABEL_DELIM` SYMBOL連接。 SPS標籤優先於自動產生的標籤，但是以SYMBOL為基礎的標籤覆寫。

自動產生的標籤是指派給ecatalog中所有頁面的循序號碼。 如果給定跨頁已定義基於符號的標籤或已定義SPS標籤，則會自動生成的標籤將被忽略。

在目錄中，可使用`showdefault`參數停用自動產生標籤的顯示。
