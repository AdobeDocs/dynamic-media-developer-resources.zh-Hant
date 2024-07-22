---
description: 材質目錄提供許多「影像演算」組態設定。
solution: Experience Manager
title: 材質目錄
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: c0b030b7-bcfb-4e6d-b74a-4533bdb801bf
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 0%

---

# 材質目錄{#material-catalogs}

材質目錄提供許多「影像演算」組態設定。

材質目錄會將請求中使用的暈映和材質ID對應到實際檔案路徑，可以儲存與材質相關的所有中繼資料，並為範本提供容器。 它們會追蹤ICC設定檔和指令巨集。

材質目錄只能由影像演算的Java元件存取（與[!DNL Platform Server]共用）。 目錄屬性檔案必須有[!DNL .ini]個字尾，並放置在已登入的目錄資料夾([ir.catalogRootPath](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-catalog-folder.md#concept-1c1d308112054bb99e3895c3fb8ca5f7))中。 預設素材目錄([!DNL default.ini])必須永遠存在，且必須填入所有屬性，才能讓「影像伺服」正確運作。
