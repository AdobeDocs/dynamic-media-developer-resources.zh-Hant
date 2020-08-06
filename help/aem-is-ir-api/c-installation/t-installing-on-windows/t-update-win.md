---
description: 升級Scene7 Image Serving時，請使用此程式。
seo-description: 升級Scene7 Image Serving時，請使用此程式。
seo-title: 從IS 4.7.4或更新版本更新
solution: Experience Manager
title: 從IS 4.7.4或更新版本更新
topic: Scene7 Image Serving - Image Rendering API
uuid: 3d23f13a-a9be-45ff-9765-c71bdeb77c5f
translation-type: tm+mt
source-git-commit: edb21832b3e36a6498c6aad27813cd4b3032b48f
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 0%

---


# 從IS 4.7.4或更新版本更新{#updating-from-is-or-later}

升級Scene7 Image Serving時，請使用此程式。

如果您是從舊版影像伺服升級，請聯絡支援以取得正確的程式。

>[!NOTE]
>
>升級 [!DNL webapps] 時可以刪除該資料夾。 在升級前 [!DNL webapps] 備份資料夾。

1. 使用管理權限登錄到伺服器主機。
1. 解壓縮「影像伺服」散發zip檔案的內容。
1. 運行setup/setup.exe以啟動安裝嚮導。
1. 按一 **[!UICONTROL 下]** 「下一步」以進入「使用者授權合約(EULA)」，閱讀授權合約，然後按一下「 **[!UICONTROL 是」]**。

   下一頁顯示先前的配置設定。
1. 按一下 **[!UICONTROL 下一步]** ，開始安裝更新。

   >[!NOTE]
   >
   >安裝程式會將舊伺服器組態檔備份至資料 [!DNL BACKUP/] 夾。

1. 安裝完成後，按一下「完成」退出安裝嚮導。

   在某些情況下，安裝嚮導可能會要求重新啟動系統。

在更新期間，檔 [!DNL ImageServing/conf/server.xml] 案會更新為最新的設定。 如果您已變更或新增任何值，則應儲存現有值，並在 [!DNL server.xml] 升級後重新實作變更。

在安裝更新後，請考慮在將伺服器上線之前先預熱HTTP回應快取。 有關詳細資訊，請參 `playlog` 閱實用程式說明。
