---
title: 從IS 4.7.4或更高版本更新
description: 在Linux®上升級Dynamic Media映像服務時，請執行此過程。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 54733fcc-c4e3-4501-8a3d-000778678bdb
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 0%

---

# 從IS 4.7.4或更高版本更新{#updating-from-is-or-later}

在Linux®上升級Dynamic Media映像服務時，請執行此過程。

如果從較舊版本的映像服務升級，請聯繫支援人員以獲得正確的流程。

的 [!DNL webapps] 可以在升級時刪除資料夾。 請備份 [!DNL webapps] 資料夾。

1. 以根權限登錄到伺服器主機。
1. 解壓縮並解壓縮Image Serving分發tar檔案。
1. 在 [!DNL setup] 資料夾，運行 [!DNL `./install-is`] 啟動安裝嚮導。

   更新安裝程式會檢查已安裝軟體包的完整性和版本。 如果成功，將顯示最終用戶許可協定(「EULA」)。
1. 閱讀許可協定，然後輸入 **[!UICONTROL y]** 繼續安裝。

   安裝程式將舊伺服器配置檔案備份到 [!DNL BACKUP/] 的子菜單。

   安裝完成後，將顯示以下消息：

   `Image Server was started successfully`

在更新期間， [!DNL ImageServing/conf/server.xml] 檔案更新為最新設定。 如果已更改或添加了任何值，請保存現有值 [!DNL server.xml] 並在升級後重新實施更改。

在安裝更新後，請考慮在使伺服器生存之前預熱HTTP響應快取。 請參閱 [!DNL playlog] 的子菜單。
