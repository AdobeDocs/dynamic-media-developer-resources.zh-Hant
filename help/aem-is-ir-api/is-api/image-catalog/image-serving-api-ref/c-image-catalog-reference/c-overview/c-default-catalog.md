---
description: 預設目錄為所有影像目錄的所有目錄屬性提供預設值。
solution: Experience Manager
title: 預設目錄
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: db42fb67-aa6f-4217-bc69-45b01bbd0b10
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 0%

---

# 預設目錄{#default-catalog}

預設目錄為所有影像目錄的所有目錄屬性提供預設值。

如果在特定影像目錄中找不到特定屬性，則伺服器會改用預設目錄中的對應值。 同樣，預設目錄可用於提供特定目錄資料記錄（影像、宏定義、字型和ICC配置檔案）的預設值。 如果在特定映像目錄中找不到特定資料記錄，則伺服器會嘗試在預設目錄中找到它。 這可讓影像目錄稀疏填入，並簡化全域屬性和資料（如共用範本、巨集、字型等）的管理。

此外，當操作中不涉及特定影像目錄時，預設目錄提供所有屬性和資料記錄（宏、字型、ICC配置檔案、請求預處理規則）。

為正確運作 [!DNL Platform Server] 預設目錄的目錄屬性檔案必須命名為 [!DNL default.ini]，必須始終存在於目錄資料夾中，且必須以所有必要屬性完全填入，但不包括 `attribute::RootId` 和各種目錄資料檔案的參考，這些都是選用的。

>[!NOTE]
>
>除外的所有目錄屬性檔案 [!DNL default.ini] 必須包含唯一 `attribute::RootId` 值。 `attribute::RootId` in [!DNL default.ini] 必須為空。
