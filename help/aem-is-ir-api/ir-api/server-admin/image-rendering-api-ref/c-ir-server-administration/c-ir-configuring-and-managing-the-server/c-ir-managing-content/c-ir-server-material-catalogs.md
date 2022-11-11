---
description: 材料目錄提供許多「影像呈現」配置設定。
solution: Experience Manager
title: 材料目錄
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: c0b030b7-bcfb-4e6d-b74a-4533bdb801bf
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 0%

---

# 材料目錄{#material-catalogs}

材料目錄提供許多「影像呈現」配置設定。

物料目錄可將請求中使用的暈映和物料ID映射到實際的檔案路徑，可以儲存與物料相關的所有元資料，並為模板提供容器。 它們跟蹤ICC配置檔案和命令宏。

材料目錄僅由影像呈現的Java元件訪問(與 [!DNL Platform Server])。 目錄屬性檔案必須具有 [!DNL .ini] 尾碼，並放置在註冊的目錄資料夾([ir.catalogRootPath](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-catalog-folder.md#concept-1c1d308112054bb99e3895c3fb8ca5f7))。 預設材料目錄( [!DNL default.ini])必須始終存在，且必須填入所有屬性，才能正確運作影像伺服。
