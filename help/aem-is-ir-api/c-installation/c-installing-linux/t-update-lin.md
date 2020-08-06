---
description: 在Linux上升級Scene7 Image Serving時，請使用此程式。
seo-description: 在Linux上升級Scene7 Image Serving時，請使用此程式。
seo-title: 從IS 4.7.4或更新版本更新
solution: Experience Manager
title: 從IS 4.7.4或更新版本更新
topic: Scene7 Image Serving - Image Rendering API
uuid: 70beb1a3-71b9-4bd0-b048-13d88446a9d3
translation-type: tm+mt
source-git-commit: 038f0f8f2c4f815e47749e0bab153c63e5396c91
workflow-type: tm+mt
source-wordcount: '220'
ht-degree: 0%

---


# 從IS 4.7.4或更新版本更新{#updating-from-is-or-later}

在Linux上升級Scene7 Image Serving時，請使用此程式。

如果您是從舊版影像伺服升級，請聯絡支援以取得正確的程式。

升級 [!DNL webapps] 時可以刪除該資料夾。 升級前請備份 [!DNL webapps] 該資料夾。

1. 以根權限登錄到伺服器主機。
1. 解壓縮並解壓縮Image Serving散發tar檔案。
1. 運 [!DNL ./install-is] 行以啟動位於資料夾中的安裝向 [!DNL setup] 導。

   更新安裝程式會檢查已安裝套件的完整性和版本。 如果成功，則會顯示使用者授權合約(「EULA」)。
1. 閱讀授權合約，然後輸 **[!UICONTROL 入]**&quot;y&quot;繼續安裝。

   安裝程式會將舊伺服器組態檔備份至資料 [!DNL BACKUP/] 夾。

   安裝完成後，將顯示以下消息：

   `Image Server was started successfully`

在更新期間，檔 [!DNL ImageServing/conf/server.xml] 案會更新為最新的設定。 如果您已變更或新增任何值，則應儲存現有值，並在 [!DNL server.xml] 升級後重新實作變更。

在安裝更新後，請考慮在將伺服器上線之前先預熱HTTP回應快取。 有關詳細資訊，請參 [!DNL playlog] 閱實用程式說明。
