---
description: 材料目錄提供了許多「影像渲染」配置設定。
solution: Experience Manager
title: 物料目錄
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: c0b030b7-bcfb-4e6d-b74a-4533bdb801bf
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 0%

---

# 物料目錄{#material-catalogs}

材料目錄提供了許多「影像渲染」配置設定。

物料目錄將請求中使用的視圖和物料ID映射到實際的檔案路徑，可以儲存與物料相關的所有元資料，並為模板提供容器。 它們跟蹤ICC配置檔案和命令宏。

材料目錄僅由「影像渲染」的Java元件訪問(與 [!DNL Platform Server])。 目錄屬性檔案必須具有 [!DNL .ini] 尾碼並放入註冊的目錄資料夾([ir.catalogRootPath](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-catalog-folder.md#concept-1c1d308112054bb99e3895c3fb8ca5f7))。 預設物料目錄( [!DNL default.ini])必須始終存在，並且必須填充所有屬性才能正確運行映像服務。
