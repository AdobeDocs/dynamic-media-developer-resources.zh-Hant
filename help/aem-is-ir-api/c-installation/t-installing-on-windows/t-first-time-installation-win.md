---
description: 使用這些步驟，在Windows上首次安裝Image Serving。
solution: Experience Manager
title: 首次安裝
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '383'
ht-degree: 0%

---


# 首次安裝{#installing-for-the-first-time}

使用這些步驟，在Windows上首次安裝Image Serving。

1. 使用管理權限登錄到伺服器主機。
1. 如果您已收到授權，請將它複製至您的伺服器，然後連按兩下檔案以執行授權安裝。

   如果您尚未取得授權，則可繼續安裝，稍後再安裝授權。
1. 解壓縮「影像伺服」散發zip檔案的內容。
1. 運行[!DNL setup]/ [!DNL setup.exe]以啟動安裝嚮導。
1. 按一下「下一步」進入最終用戶許可協定(EULA)，閱讀許可協定，然後按一下&#x200B;**[!UICONTROL 是]**。

   下面將顯示[!DNL Authentication]對話框。
1. 如果已安裝許可證，且許可證資訊顯示在[!DNL Authentication]對話框中，請按一下&#x200B;**[!UICONTROL Next]**&#x200B;繼續。

   如果您沒有授權，請按一下「請求授權」**[!UICONTROL 。]**&#x200B;下一個對話框顯示您電腦的一個網路介面卡MAC地址。 以電子郵件寄送此MAC位址、您的公司名稱，以及您要安裝的產品，並依照提示進行指示。

   **重要：** 此許可證基於安裝在此主機上的其中一個網路介面卡的MAC地址。如果您停用、移除或更換此卡片，將不會再將授權辨識為有效。 請務必為要用於IS的硬體配置獲取許可證。

   您可以繼續安裝IS（沒有有效的授權），稍後再安裝該授權。 要繼續，按一下&#x200B;**[!UICONTROL Back]**&#x200B;返回[!DNL Authentication]對話框，然後按一下&#x200B;**[!UICONTROL Next]**。
1. 繼續至「平台伺服器管理設定」頁面。 根據需要輸入新值或接受預設值。

   您可以設定下列項目：

<table id="table_AA5D7674BBBE4AD4B373066AEF413FFD"> 
 <tbody> 
  <tr> 
   <td> <p> 平台伺服器HTTP連接埠 </p> </td> 
   <td> <p>影像服務與影像轉換的主HTTP監聽埠 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> 管理員監聽埠 </p> </td> 
   <td> <p>管理員監聽埠 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> 平台伺服器快取大小(MB) </p> </td> 
   <td> <p>主響應快取的初始大小 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> 平台伺服器快取位置 </p> </td> 
   <td> <p>PS快取資料夾 </p> </td> 
  </tr> 
 </tbody> 
</table>

指定的埠號必須是唯一的，不能用於其他應用程式或服務。

下一個畫面提供檢閱所選設定的機會。
1. 按一下&#x200B;**[!UICONTROL Back]**&#x200B;進行更改，或按一下&#x200B;**[!UICONTROL Next]**&#x200B;開始安裝。
1. 按一下&#x200B;**[!UICONTROL 完成]**&#x200B;退出安裝嚮導。
