---
description: 瀏覽器中點選動作的目標。
solution: Experience Manager
title: 影像地圖
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 123eba56-2a59-44c5-93f0-205c362d071d
TQID: 'https://experienceleague.adobe.com/ikMxCQ23L0HzbfmRlcYGL-fRJFK2uhwbZHNzcy1c25k'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: b658a9f9067d2313c1c838c7e157f4070ebc2b50
workflow-type: tm+mt
source-wordcount: 91
ht-degree: 4%

---

# [!DNL ImageMap]{#imagemap}

瀏覽器中點選動作的目標。

永遠與影像相關聯。 您可以從`ImageInfo`取得`ImageMap`目標。

## 參數 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名稱 | 類型 | 說明 |
|---|---|---|
| imageMapHandle | `xsd:string` | 影像地圖控制代碼。 |
| [!DNL name] | `xsd:string` | 影像地圖名稱。 |
| [!DNL region] | `xsd:string` | 影像地圖座標。 格式是以HTML `<area>`標籤屬性為基礎。 |
| [!DNL action] | `xsd:string` | 要包含在HTML `<area>`標籤中的其他屬性，包括`href` URL。 |
| shapetype | `xsd:boolean` | [!DNL RegionShape]值。 |
| [!DNL position] | `xsd:string` | 以HTML `<area>`專案的[!DNL coords]屬性格式放置位置。 例如： `coords ="0,0,84,128"`。 |
| [!DNL enabled] | `xsd:boolean` | 如果啟用影像地圖，則為True。 |
| lastModified | `xsd:dateTime` | 上次修改影像地圖的日期和時間。 |

