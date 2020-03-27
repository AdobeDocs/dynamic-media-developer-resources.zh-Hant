---
description: 影像演算來源資料檔案包括暈映檔案、材質檔案（可重複紋理和貼文的影像，以及涵蓋樣式檔案的檔案櫃和視窗）和ICC描述檔。
seo-description: 影像演算來源資料檔案包括暈映檔案、材質檔案（可重複紋理和貼文的影像，以及涵蓋樣式檔案的檔案櫃和視窗）和ICC描述檔。
seo-title: 來源資料
solution: Experience Manager
title: 來源資料
topic: Scene7 Image Serving - Image Rendering API
uuid: 76c6419c-613e-4eff-b30f-9fea2a7daf5b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 來源資料{#source-data}

影像演算來源資料檔案包括暈映檔案、材質檔案（可重複紋理和貼文的影像，以及涵蓋樣式檔案的檔案櫃和視窗）和ICC描述檔。

所有原始資料檔案都必須可供影像轉換的原生程式碼元件存取（與影像伺服器同位）。

如果涉及材料目錄，則Render Server會按如下方式查找在材料目錄( `vignette::Path`具有 `catalog::Path`、 `icc::ProfilePath`或)中指定的檔案：

* 如果路徑是絕對的，則按原樣使用。
* 如果路徑是相對的，則會加上前置詞 `catalog::RootPath` （來自命名的材料目錄）。
* 如果路徑是絕對的，則使用路徑；否則，它會加上前置詞 `default::RootPath` （從預設目錄）。
* 如果路徑是絕對的，則使用路徑；否則，伺服器會將其與 [ir.resourceRootPaths中指定的路徑組合](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-resource-root-folders.md#concept-39a34d2239934079bb396e1bf568a9c2)。
* 如果路徑現在是絕對的，則使用它；否則，假設它是[!DNL *[!DNL install_folder]*]。

如果未涉及影像目錄，則會結合路徑， `default::RootPath` 然後依上述方式處理。

源資料檔案的物理位置通常使用 [ir.resourceRootPaths指定](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-resource-root-folders.md#concept-39a34d2239934079bb396e1bf568a9c2)。 可以指定多個值，以允許源資料檔案跨多個檔案系統分發。 Render Server將按照指定的順序嘗試每個路徑，直到找到資料檔案。

不需停止伺服器，就可隨時新增任何類型的資料檔案。
