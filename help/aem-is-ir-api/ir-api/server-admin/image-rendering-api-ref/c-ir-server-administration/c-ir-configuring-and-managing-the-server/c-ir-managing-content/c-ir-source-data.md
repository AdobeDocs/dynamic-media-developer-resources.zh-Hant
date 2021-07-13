---
description: 影像呈現源資料檔案包括暈映檔案、材料檔案（用於可重複紋理和標籤的影像，以及覆蓋樣式檔案的檔案櫃和窗口）和ICC配置檔案。
solution: Experience Manager
title: 源資料
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,User
exl-id: de2d8fa2-6793-49ba-b873-adf723369cce
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 0%

---

# 源資料{#source-data}

影像呈現源資料檔案包括暈映檔案、材料檔案（用於可重複紋理和標籤的影像，以及覆蓋樣式檔案的檔案櫃和窗口）和ICC配置檔案。

所有原始資料檔案必須可供影像呈現的本機代碼元件存取（與影像伺服器共同位置）。

如果涉及物料目錄，則渲染伺服器將查找物料目錄（具有`vignette::Path`、`catalog::Path`或`icc::ProfilePath`）中指定的檔案，如下所示：

* 如果路徑為絕對路徑，則會依原樣使用。
* 如果路徑為相對路徑，則其前置詞為`catalog::RootPath`（來自命名的材料目錄）。
* 如果路徑為絕對路徑，則使用；否則，會加上前置詞`default::RootPath`（來自預設目錄）。
* 如果路徑為絕對路徑，則使用；否則，伺服器會將其與[ir.resourceRootPaths](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-resource-root-folders.md#concept-39a34d2239934079bb396e1bf568a9c2)中指定的路徑組合。
* 如果路徑現在是絕對路徑，則會使用；否則，此變數會假設為相對於[!DNL *[!DNL install_folder]*]。

如果未涉及映像目錄，則路徑將與`default::RootPath`組合，然後按上述方式處理。

源資料檔案的物理位置通常以[ir.resourceRootPaths](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-resource-root-folders.md#concept-39a34d2239934079bb396e1bf568a9c2)指定。 可以指定多個值，以允許源資料檔案在多個檔案系統之間分佈。 呈現伺服器將按指定的順序嘗試每個路徑，直到找到資料檔案。

可以隨時添加任何類型的新資料檔案，而無需停止伺服器。
