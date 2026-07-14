---
description: 管理頁面標籤
solution: Experience Manager
title: 管理頁面標籤
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 73c3904f-678f-47c4-b895-86671402df79
TQID: 'https://experienceleague.adobe.com/EprHC1GFDB5Lkytg4NZf8Am0myr-jXC2wxxcefelvc8'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: f6432244ef9faba7a81488e9de8e438154ae6123
workflow-type: tm+mt
source-wordcount: 269
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

