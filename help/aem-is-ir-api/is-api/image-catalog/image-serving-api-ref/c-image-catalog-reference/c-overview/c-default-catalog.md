---
description: 預設目錄為所有映像目錄的所有目錄屬性提供預設值。
solution: Experience Manager
title: 預設目錄
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 0%

---


# 預設目錄{#default-catalog}

預設目錄為所有映像目錄的所有目錄屬性提供預設值。

如果在特定影像目錄中找不到特定屬性，伺服器會改用預設目錄的對應值。 同樣地，預設目錄可用來提供特定目錄資料記錄（影像、巨集定義、字型和ICC描述檔）的預設值。 如果在特定的映像目錄中找不到特定的資料記錄，則伺服器會嘗試在預設目錄中查找它。 這可讓影像目錄稀疏填入，並簡化全域屬性和資料的管理，例如共用範本、巨集、字型等。

此外，當操作中未涉及特定影像目錄時，預設目錄會提供所有屬性和資料記錄（宏、字型、ICC配置檔案、請求預處理規則）。

要使平台伺服器正常運行，預設目錄的目錄屬性檔案必須命名為[!DNL default.ini]，必須始終存在於目錄資料夾中，並且必須完全填充所有必需屬性，不包括`attribute::RootId`和對各種目錄資料檔案的引用，這些屬性都是可選的。

>[!NOTE]
>
>除[!DNL default.ini]之外的所有目錄屬性檔案都必須包含唯一的`attribute::RootId`值。 `attribute::RootId` in必 [!DNL default.ini] 須為空。

