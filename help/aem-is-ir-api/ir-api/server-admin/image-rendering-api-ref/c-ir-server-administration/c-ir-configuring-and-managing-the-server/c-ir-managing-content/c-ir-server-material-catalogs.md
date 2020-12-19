---
description: 材質型錄提供許多「影像演算」組態設定。
seo-description: 材質型錄提供許多「影像演算」組態設定。
seo-title: 材料型錄
solution: Experience Manager
title: 材料型錄
topic: Scene7 Image Serving - Image Rendering API
uuid: 6d209019-f9ca-43e4-900b-3597c7044a79
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 0%

---


# 材料目錄{#material-catalogs}

材質型錄提供許多「影像演算」組態設定。

材料目錄可將請求中使用的暈映和材料ID映射至實際的檔案路徑，可儲存與材料相關的所有中繼資料，並提供範本容器。 他們會追蹤ICC描述檔和指令巨集。

材質型錄僅能由影像演算的Java元件存取（與平台伺服器同位）。 目錄屬性檔案必須有[!DNL .ini]尾碼，並放置在已註冊的目錄資料夾([ir.catalogRootPath](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-catalog-folder.md#concept-1c1d308112054bb99e3895c3fb8ca5f7))中。 預設材料目錄([!DNL default.ini])必須始終存在，並且必須填入所有屬性，才能正確運行影像服務。
