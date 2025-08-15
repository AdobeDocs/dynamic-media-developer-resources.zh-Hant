---
title: 從IS 4.7.4或更新版本更新
description: 在Linux®上升級Dynamic Media影像伺服時，請使用此程式。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 54733fcc-c4e3-4501-8a3d-000778678bdb
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '206'
ht-degree: 0%

---

# 從IS 4.7.4或更新版本更新{#updating-from-is-or-later}

在Linux®上升級Dynamic Media影像伺服時，請使用此程式。

如果您要從舊版「影像伺服」升級，請聯絡支援以取得正確的程式。

升級時可以刪除[!DNL webapps]資料夾。 請先備份[!DNL webapps]資料夾，然後再進行升級。

1. 以超級使用者許可權登入您的伺服器主機。
1. 解壓縮並解壓縮「影像伺服」發佈tar檔案。
1. 在[!DNL setup]資料夾中，執行[!DNL `./install-is`]以啟動安裝精靈。

   更新安裝程式會檢查已安裝封裝的完整性和版本。 如果成功，便會顯示「使用者授權合約」(「EULA」)。
1. 閱讀授權合約，然後輸入&#x200B;**[!UICONTROL y]**&#x200B;以繼續安裝。

   安裝程式會將舊的伺服器組態檔備份至[!DNL BACKUP/]資料夾。

   安裝完成後，會顯示下列訊息：

   `Image Server was started successfully`

在更新期間，[!DNL ImageServing/conf/server.xml]檔案會更新為最新設定。 如果您已變更或新增任何值，請儲存現有的[!DNL server.xml]，並在升級後重新實作變更。

更新安裝後，請考慮先預熱HTTP回應快取，再讓伺服器上線。 如需詳細資訊，請參閱[!DNL playlog]公用程式的說明。
