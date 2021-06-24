---
description: 升級Dynamic Media Image Serving時，請使用此程式。
solution: Experience Manager
title: 從IS 4.7.4或更新版本更新
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: e0781f19-4aa8-46f7-a586-4724ff8a2e68
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '216'
ht-degree: 0%

---

# 從IS 4.7.4或更新版本更新{#updating-from-is-or-later}

升級Dynamic Media Image Serving時，請使用此程式。

如果您從舊版影像伺服升級，請聯絡支援人員以了解正確的流程。

>[!NOTE]
>
>升級時可刪除[!DNL webapps]資料夾。 升級前備份[!DNL webapps]資料夾。

1. 以管理權限登入您的伺服器主機。
1. 解壓縮Image Serving分送Zip檔案的內容。
1. 運行setup/setup.exe以啟動安裝嚮導。
1. 按一下&#x200B;**[!UICONTROL Next]**&#x200B;前進至最終用戶許可協定(EULA)，閱讀許可協定，然後按一下&#x200B;**[!UICONTROL Yes]**。

   下一頁顯示先前的配置設定。
1. 按一下&#x200B;**[!UICONTROL Next]**&#x200B;以開始安裝更新。

   >[!NOTE]
   >
   >安裝程式將舊伺服器配置檔案備份到[!DNL BACKUP/]資料夾。

1. 安裝完成後，按一下「完成」退出安裝嚮導。

   在某些情況下，安裝嚮導可能會要求重新啟動系統。

更新期間， [!DNL ImageServing/conf/server.xml]檔案會更新為最新設定。 如果您已變更或新增任何值，則應儲存現有的[!DNL server.xml]，並在升級後重新實作變更。

安裝更新後，請考慮在伺服器上線前先預熱HTTP回應快取。 有關詳細資訊，請參閱`playlog`實用程式的說明。
