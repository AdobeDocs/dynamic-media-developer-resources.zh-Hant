---
description: 預設目錄為所有映像目錄的所有目錄屬性提供預設值。
seo-description: 預設目錄為所有映像目錄的所有目錄屬性提供預設值。
seo-title: 預設目錄
solution: Experience Manager
title: 預設目錄
topic: Scene7 Image Serving - Image Rendering API
uuid: 9f0c967e-a2fa-4ef0-bacb-3dcfb06a8027
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 預設目錄{#default-catalog}

預設目錄為所有映像目錄的所有目錄屬性提供預設值。

如果在特定影像目錄中找不到特定屬性，伺服器會改用預設目錄的對應值。 同樣地，預設目錄可用來提供特定目錄資料記錄（影像、巨集定義、字型和ICC描述檔）的預設值。 如果在特定的映像目錄中找不到特定的資料記錄，則伺服器會嘗試在預設目錄中查找它。 這可讓影像目錄稀疏填入，並簡化全域屬性和資料的管理，例如共用範本、巨集、字型等。

此外，當操作中未涉及特定影像目錄時，預設目錄會提供所有屬性和資料記錄（宏、字型、ICC配置檔案、請求預處理規則）。

為了使平台伺服器正常運行，預設目錄的目錄屬性檔案必須命名 [!DNL default.ini]`attribute::RootId` ，必須始終存在於目錄資料夾中，並且必須完全填充所有必需屬性（排除和對各種目錄資料檔案的引用），這些屬性都是可選的。

>[!NOTE]
>
>除外的所有目錄屬性 [!DNL default.ini] 檔案都必須包含唯一 `attribute::RootId` 值。 `attribute::RootId` 中 [!DNL default.ini] 必須為空。

