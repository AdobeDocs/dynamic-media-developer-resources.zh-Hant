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


# 從IS 4.7.4或更新版本{#updating-from-is-or-later}更新

升級Scene7 Image Serving時，請使用此程式。

如果您是從舊版影像伺服升級，請聯絡支援以取得正確的程式。

>[!NOTE]
>
>升級時，[!DNL webapps]資料夾可能會被刪除。 升級前備份[!DNL webapps]資料夾。

1. 使用管理權限登錄到伺服器主機。
1. 解壓縮「影像伺服」散發zip檔案的內容。
1. 運行setup/setup.exe以啟動安裝嚮導。
1. 按一下&#x200B;**[!UICONTROL Next]**&#x200B;進入最終用戶許可協定(EULA)，閱讀許可協定，然後按一下&#x200B;**[!UICONTROL 是]**。

   下一頁顯示先前的配置設定。
1. 按一下&#x200B;**[!UICONTROL Next]**&#x200B;啟動更新安裝。

   >[!NOTE]
   >
   >安裝程式將舊伺服器配置檔案備份到[!DNL BACKUP/]資料夾。

1. 安裝完成後，按一下「完成」退出安裝嚮導。

   在某些情況下，安裝嚮導可能會要求重新啟動系統。

在更新期間，[!DNL ImageServing/conf/server.xml]檔案會更新為最新的設定。 如果您已變更或新增任何值，則應儲存現有的[!DNL server.xml]，並在升級後重新實作變更。

在安裝更新後，請考慮在將伺服器上線之前先預熱HTTP回應快取。 有關詳細資訊，請參閱`playlog`實用程式的說明。
