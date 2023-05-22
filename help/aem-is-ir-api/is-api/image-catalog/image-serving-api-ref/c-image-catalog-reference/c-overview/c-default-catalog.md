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

如果在特定映像目錄中找不到特定屬性，則伺服器將改用預設目錄中的相應值。 同樣，預設目錄可用於為特定目錄資料記錄（影像、宏定義、字型和ICC配置檔案）提供預設值。 如果在特定映像目錄中找不到特定資料記錄，則伺服器會嘗試在預設目錄中找到它。 這允許稀疏填充影像目錄，並簡化全局屬性和資料的管理，如共用模板、宏、字型等。

此外，當操作中未涉及特定影像目錄時，預設目錄將提供所有屬性和資料記錄（宏、字型、ICC配置檔案、請求預處理規則）。

正確運行 [!DNL Platform Server] 必須為預設目錄的目錄屬性檔案命名 [!DNL default.ini]，必須始終存在於目錄資料夾中，並且必須用所有必需屬性(不包括 `attribute::RootId` 以及對各種目錄資料檔案的引用，這些都是可選的。

>[!NOTE]
>
>所有目錄屬性檔案(不包括 [!DNL default.ini] 必須包含唯一 `attribute::RootId` 值。 `attribute::RootId` 在 [!DNL default.ini] 必須為空。
