---
description: 預設目錄為所有影像目錄的所有目錄屬性提供預設值。
solution: Experience Manager
title: 預設目錄
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: db42fb67-aa6f-4217-bc69-45b01bbd0b10
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 0%

---

# 預設目錄{#default-catalog}

預設目錄為所有影像目錄的所有目錄屬性提供預設值。

如果在特定影像目錄中找不到特定屬性，則伺服器會改用預設目錄中的對應值。 同樣，預設目錄可用於提供特定目錄資料記錄（影像、宏定義、字型和ICC配置檔案）的預設值。 如果在特定映像目錄中找不到特定資料記錄，則伺服器會嘗試在預設目錄中找到它。 這可讓影像目錄稀疏填入，並簡化全域屬性和資料（如共用範本、巨集、字型等）的管理。

此外，當操作中不涉及特定影像目錄時，預設目錄提供所有屬性和資料記錄（宏、字型、ICC配置檔案、請求預處理規則）。

為了正確運行Platform Server，預設目錄的目錄屬性檔案必須命名為[!DNL default.ini]，必須始終存在於目錄資料夾中，並且必須完全填充所有必需屬性，不包括`attribute::RootId`和對各種目錄資料檔案的引用，這些都是可選的。

>[!NOTE]
>
>除[!DNL default.ini]之外的所有目錄屬性檔案都必須包含唯一的`attribute::RootId`值。 `attribute::RootId` 中的 [!DNL default.ini] 必須為空。
