---
description: 影像演算來源資料檔案包括暈映檔案、材質檔案（可重複紋理和貼文的影像，以及涵蓋樣式檔案的檔案櫃和視窗）和ICC描述檔。
solution: Experience Manager
title: 來源資料
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '267'
ht-degree: 0%

---


# 源資料{#source-data}

影像演算來源資料檔案包括暈映檔案、材質檔案（可重複紋理和貼文的影像，以及涵蓋樣式檔案的檔案櫃和視窗）和ICC描述檔。

所有原始資料檔案都必須可供影像轉換的原生程式碼元件存取（與影像伺服器同位）。

如果涉及材料目錄，則Render Server會按如下方式查找在材料目錄（具有`vignette::Path`、`catalog::Path`或`icc::ProfilePath`）中指定的檔案：

* 如果路徑是絕對的，則按原樣使用。
* 如果路徑是相對的，則其前置詞為`catalog::RootPath`（來自命名的材料目錄）。
* 如果路徑是絕對的，則使用路徑；否則，它會加上前置詞`default::RootPath`（從預設目錄）。
* 如果路徑是絕對的，則使用路徑；否則，伺服器會將其與[ir.resourceRootPaths](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-resource-root-folders.md#concept-39a34d2239934079bb396e1bf568a9c2)中指定的路徑合併。
* 如果路徑現在是絕對的，則使用它；否則，假設它是相對於[!DNL *[!DNL install_folder]*]。

如果未涉及影像目錄，則路徑與`default::RootPath`組合，然後按上述方式處理。

源資料檔案的物理位置通常使用[ir.resourceRootPaths](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-resource-root-folders.md#concept-39a34d2239934079bb396e1bf568a9c2)指定。 可以指定多個值，以允許源資料檔案跨多個檔案系統分發。 Render Server將按照指定的順序嘗試每個路徑，直到找到資料檔案。

不需停止伺服器，就可隨時新增任何類型的資料檔案。
