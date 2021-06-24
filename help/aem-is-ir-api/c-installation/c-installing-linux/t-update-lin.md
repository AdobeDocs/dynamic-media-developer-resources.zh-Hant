---
description: 在Linux上升級Dynamic Media Image Serving時，請使用此程式。
solution: Experience Manager
title: 從IS 4.7.4或更新版本更新
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 54733fcc-c4e3-4501-8a3d-000778678bdb
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 0%

---

# 從IS 4.7.4或更新版本更新{#updating-from-is-or-later}

在Linux上升級Dynamic Media Image Serving時，請使用此程式。

如果您從舊版影像伺服升級，請聯絡支援人員以了解正確的流程。

升級時可刪除[!DNL webapps]資料夾。 升級前，請備份[!DNL webapps]資料夾。

1. 以根權限登入您的伺服器主機。
1. 解壓縮Image Serving分發tar檔案。
1. 運行[!DNL ./install-is]以啟動位於[!DNL setup]資料夾中的安裝嚮導。

   更新安裝程式會檢查已安裝套件的完整性和版本。 如果成功，則會顯示使用者授權合約(「EULA」)。
1. 閱讀許可協定，然後輸入&quot; **[!UICONTROL y]**&quot;以繼續安裝。

   安裝程式將舊伺服器配置檔案備份到[!DNL BACKUP/]資料夾。

   當安裝完成時，會顯示下列訊息：

   `Image Server was started successfully`

更新期間， [!DNL ImageServing/conf/server.xml]檔案會更新為最新設定。 如果您已變更或新增任何值，則應儲存現有的[!DNL server.xml]，並在升級後重新實作變更。

安裝更新後，請考慮在伺服器上線前先預熱HTTP回應快取。 有關詳細資訊，請參閱[!DNL playlog]實用程式的說明。
