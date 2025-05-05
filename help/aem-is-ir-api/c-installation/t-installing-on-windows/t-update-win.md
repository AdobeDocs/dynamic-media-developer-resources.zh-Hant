---
title: 從IS 4.7.4或更新版本更新
description: 升級Dynamic Media影像伺服時請使用此程式。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e0781f19-4aa8-46f7-a586-4724ff8a2e68
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 0%

---

# 從IS 4.7.4或更新版本更新{#updating-from-is-or-later}

升級Dynamic Media影像伺服時請使用此程式。

如果您要從舊版「影像伺服」升級，請聯絡支援以取得正確的程式。

>[!NOTE]
>
>升級時可能會刪除[!DNL webapps]資料夾。 請先備份[!DNL webapps]資料夾，然後再進行升級。

1. 以管理許可權登入您的伺服器主機。
1. 擷取「影像伺服」發佈Zip檔案的內容。
1. 執行`setup/setup.exe`以啟動安裝精靈。
1. 選取&#x200B;**[!UICONTROL 下一步]**&#x200B;以進入使用者授權合約(EULA)，閱讀授權合約，然後選取&#x200B;**[!UICONTROL 是]**。

   下一頁顯示先前的組態設定。
1. 按一下[下一步]&#x200B;**&#x200B;**&#x200B;開始更新安裝。

   >[!NOTE]
   >
   >安裝程式會將舊的伺服器組態檔備份至[!DNL BACKUP/]資料夾。

1. 安裝完成之後，請選取&#x200B;**[!UICONTROL 完成]**&#x200B;以結束安裝精靈。

   有時安裝精靈可能會要求您重新啟動系統。

在更新期間，[!DNL ImageServing/conf/server.xml]檔案會更新為最新設定。 如果您已變更或新增任何值，您應儲存現有的[!DNL server.xml]，並在升級後重新實作變更。

更新安裝後，請考慮先預熱HTTP回應快取，再讓伺服器上線。 如需詳細資訊，請參閱`playlog`公用程式的說明。
