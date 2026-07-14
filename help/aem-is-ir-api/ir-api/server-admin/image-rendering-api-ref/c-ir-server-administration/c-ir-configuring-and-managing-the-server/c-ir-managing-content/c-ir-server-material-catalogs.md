---
description: 材質目錄提供許多「影像演算」組態設定。
solution: Experience Manager
title: 材質目錄
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: c0b030b7-bcfb-4e6d-b74a-4533bdb801bf
TQID: 'https://experienceleague.adobe.com/FOwuQrKYaRJ78mdRbPeoy71crT9GHj4R5MXFbMGnrZE'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 49c3ac586f6fb17608838f8dcf2c637822314fc7
workflow-type: tm+mt
source-wordcount: 108
ht-degree: 0%

---

# 材質目錄{#material-catalogs}

材質目錄提供許多「影像演算」組態設定。

材質目錄會將請求中使用的暈映和材質ID對應到實際檔案路徑，可以儲存與材質相關的所有中繼資料，並為範本提供容器。 它們會追蹤ICC設定檔和指令巨集。

材質目錄只能由影像演算的Java元件存取（與[!DNL Platform Server]共用）。 目錄屬性檔案必須有[!DNL .ini]個字尾，並放置在已登入的目錄資料夾([ir.catalogRootPath](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-catalog-folder.md#concept-1c1d308112054bb99e3895c3fb8ca5f7))中。 預設素材目錄([!DNL default.ini])必須永遠存在，且必須填入所有屬性，才能讓「影像伺服」正確運作。

