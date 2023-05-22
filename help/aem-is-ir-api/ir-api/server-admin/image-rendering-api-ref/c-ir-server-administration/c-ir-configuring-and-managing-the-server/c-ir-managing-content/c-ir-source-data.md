---
description: 「影像渲染」源資料檔案包括視頻檔案、材料檔案（可重複紋理和圖案的影像，以及覆蓋樣式檔案的檔案櫃和窗口）和ICC配置檔案。
solution: Experience Manager
title: 源資料
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: de2d8fa2-6793-49ba-b873-adf723369cce
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 0%

---

# 源資料{#source-data}

「影像渲染」源資料檔案包括視頻檔案、材料檔案（可重複紋理和圖案的影像，以及覆蓋樣式檔案的檔案櫃和窗口）和ICC配置檔案。

所有源資料檔案必須可以訪問「影像呈現」的本機代碼元件（與「影像伺服器」同位）。

如果涉及材料目錄，則在材料目錄中指定的檔案(使用 `vignette::Path`。 `catalog::Path`或 `icc::ProfilePath`)由Render Server查找，如下所示：

* 如果路徑是絕對路徑，則按原樣使用。
* 如果路徑是相對的，則其前置詞為 `catalog::RootPath` （來自命名的材料目錄）。
* 如果路徑為絕對路徑，則使用；否則，它預先 `default::RootPath` （從預設目錄）。
* 如果路徑為絕對路徑，則使用；否則，伺服器將其與中指定的路徑組合 [ir.resourceRootPaths](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-resource-root-folders.md#concept-39a34d2239934079bb396e1bf568a9c2)。
* 如果路徑現在是絕對路徑，則使用它；否則，假定它是相對於[!DNL]  *[!DNL install_folder]*]。

如果不涉及映像目錄，則路徑與 `default::RootPath` 然後按上述方式處理。

源資料檔案的物理位置通常指定為 [ir.resourceRootPaths](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-resource-root-folders.md#concept-39a34d2239934079bb396e1bf568a9c2)。 可以指定多個值以允許源資料檔案跨多個檔案系統分佈。 呈現伺服器將按指定的順序嘗試每個路徑，直到找到資料檔案。

可以隨時添加任何類型的新資料檔案，而不停止伺服器。
