---
description: 影像演算來源資料檔案包括暈映檔案、材質檔案（可重複紋理和貼花的影像，以及封包和視窗覆蓋樣式檔案）和ICC設定檔。
solution: Experience Manager
title: Source資料
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: de2d8fa2-6793-49ba-b873-adf723369cce
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 0%

---

# Source資料{#source-data}

影像演算來源資料檔案包括暈映檔案、材質檔案（可重複紋理和貼花的影像，以及封包和視窗覆蓋樣式檔案）和ICC設定檔。

所有來源資料檔案都必須在影像轉譯的原始程式碼元件可以存取（與影像伺服器共用）。

如果涉及素材目錄，則轉譯伺服器會依下列方式查詢素材目錄（具有`vignette::Path`、`catalog::Path`或`icc::ProfilePath`）中指定的檔案：

* 如果路徑是絕對路徑，則會依原樣使用。
* 如果路徑是相對路徑，則會以`catalog::RootPath` （來自具名材料目錄）為前置詞。
* 如果路徑是絕對路徑，則會使用它；否則，會以`default::RootPath`為前置詞（來自預設目錄）。
* 如果路徑是絕對路徑，則會使用它；否則，伺服器會將其與[ir.resourceRootPaths](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-resource-root-folders.md#concept-39a34d2239934079bb396e1bf568a9c2)中指定的路徑結合。
* 如果路徑現在是絕對路徑，則會使用它；否則，會假設它是相對於[!DNL *[!DNL install_folder]*]。

如果未涉及任何影像目錄，則路徑會與`default::RootPath`結合，然後依照上述方式處理。

來源資料檔案的實體位置通常以[ir.resourceRootPaths](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-resource-root-folders.md#concept-39a34d2239934079bb396e1bf568a9c2)指定。 可以指定多個值，以允許來源資料檔案散佈到多個檔案系統。 轉譯伺服器會依指定的順序嘗試每個路徑，直到找到資料檔案為止。

任何型別的新資料檔案都可以隨時新增，不需要停止伺服器。
