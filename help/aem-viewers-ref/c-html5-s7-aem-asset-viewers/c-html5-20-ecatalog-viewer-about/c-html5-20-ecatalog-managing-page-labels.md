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

檢視器使用者介面中顯示頁面標籤的位置有兩處：縮圖模式和目錄下拉式清單。

可以定義三種型別的標籤：

* 作者使用SYMBOL本地化機制所定義的標籤。
* 作者在Dynamic Media Classic的後端上定義的標籤。
* 檢視器自動產生的標籤。

符號型標籤是使用`MediaSet.LABEL_XX[_YY]`和`MediaSet.LABEL_DELIM` SYMBOL來定義，如[使用者介面元素的本地化](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)中所述。 您可以為整個ecatalog跨頁定義這類標籤，在這種情況下，您應該使用簡短的SYMBOL語法( `MediaSet.LABEL_XX`)。 或者，使用完整SYMBOL語法( `MediaSet.LABEL_XX_YY`)個別指定每個頁面。

當您為ecatalog跨頁中的兩個頁面定義標籤時，檢視器會使用`MediaSet.LABEL_DELIM` SYMBOL將這些標籤串連為一個字串。 以符號為基礎的標籤優先於在後端定義的標籤或由檢視器自動產生的標籤。

Dynamic Media Classic中定義的標籤會儲存在個別頁面影像的UserData記錄中。 與SYMBOL標籤相同。 也就是說，如果ecatalog跨頁中的兩個頁面都定義了標籤，則這些頁面會以橫向模式使用`MediaSet.LABEL_DELIM` SYMBOL串連。 Dynamic Media Classic標籤優先於自動產生的標籤，但會被SYMBOL型標籤覆寫。

自動產生的標籤是指派給eCatalog中所有頁面的連續編號。 如果自動產生的標籤已定義SYMBOL型標籤或定義Dynamic Media Classic標籤，則會忽略指定的跨頁。

在目錄中，可以使用`showdefault`引數停用自動產生標籤的顯示。
