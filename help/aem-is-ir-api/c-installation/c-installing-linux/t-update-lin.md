---
description: 在Linux上升級Dynamic Media映像服務時，請使用此過程。
solution: Experience Manager
title: 從IS 4.7.4或更新版本更新
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 0%

---


# 從IS 4.7.4或更新版本{#updating-from-is-or-later}更新

在Linux上升級Dynamic Media映像服務時，請使用此過程。

如果您是從舊版影像伺服升級，請聯絡支援以取得正確的程式。

升級時，[!DNL webapps]資料夾可能會被刪除。 升級前，請備份[!DNL webapps]資料夾。

1. 以根權限登錄到伺服器主機。
1. 解壓縮並解壓縮Image Serving散發tar檔案。
1. 運行[!DNL ./install-is]以啟動位於[!DNL setup]資料夾中的安裝嚮導。

   更新安裝程式會檢查已安裝套件的完整性和版本。 如果成功，則會顯示使用者授權合約(「EULA」)。
1. 閱讀授權合約，然後輸入&quot;**[!UICONTROL y]**&quot;以繼續安裝。

   安裝程式將舊伺服器配置檔案備份到[!DNL BACKUP/]資料夾。

   安裝完成後，將顯示以下消息：

   `Image Server was started successfully`

在更新期間，[!DNL ImageServing/conf/server.xml]檔案會更新為最新的設定。 如果您已變更或新增任何值，則應儲存現有的[!DNL server.xml]，並在升級後重新實作變更。

在安裝更新後，請考慮在將伺服器上線之前先預熱HTTP回應快取。 有關詳細資訊，請參閱[!DNL playlog]實用程式的說明。
