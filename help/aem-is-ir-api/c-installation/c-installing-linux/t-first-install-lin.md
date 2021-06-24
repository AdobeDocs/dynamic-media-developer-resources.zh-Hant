---
description: 此過程說明如何在Linux上首次安裝映像服務。
solution: Experience Manager
title: 首次安裝
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: f27e6b27-641c-4a88-9ed0-94ada9ba75a9
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '387'
ht-degree: 0%

---

# 首次安裝{#installing-for-the-first-time}

此過程說明如何在Linux上首次安裝映像服務。

1. 以根權限登入您的伺服器主機。
1. 建立資料夾[!DNL /usr/local/scene7/licenses]。

   如果「影像提供」和/或「影像呈現」許可證密鑰檔案（帶有[!DNL .sc8]檔案尾碼）可用，請將其複製到此資料夾。 否則，請繼續安裝，稍後安裝許可證密鑰。
1. 解壓縮Image Serving分發tar檔案。
1. 運行[!DNL Setup]資料夾中的[!DNL ./install-is]以啟動安裝嚮導。

   如果未找到許可證密鑰，則顯示說明如何獲取許可證檔案的說明。 此時請執行此操作，或繼續安裝映像服務，並稍後安裝許可證密鑰。
1. 顯示最終用戶許可協定(EULA)時，請閱讀許可協定，然後輸入`y`以繼續。

   安裝程式顯示下表中列出的提示。

<table id="table_0E7B673CAD8E4C5EB72F8283A0DDEFC8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 主監聽埠[8080]:</span> </p> </td> 
   <td colname="col2"> <p>影像提供和影像轉譯的主要HTTP監聽埠。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 管理員監聽埠[8083]:</span> </p> </td> 
   <td colname="col2"> <p>管理員監聽埠。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 最大HTTP快取大小(MB)[2000]:</span> </p> </td> 
   <td colname="col2"> <p>主響應快取的初始大小。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 快取根資料夾[/usr/local/scene7/ImageServing/cache]:</span> </p> </td> 
   <td colname="col2"> <p>PS快取資料夾。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 映像伺服器所有者ID [root]:</span> </p> </td> 
   <td colname="col2"> <p>安裝映像伺服器的用戶帳戶。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 影像伺服器組ID [root]:</span> </p> </td> 
   <td colname="col2"> <p>安裝映像伺服器的組帳戶。 </p> </td> 
  </tr> 
 </tbody> 
</table>

1. 按&#x200B;**[!UICONTROL Enter]**&#x200B;以接受預設值或指定其他值。

   請確定所有指定的埠號都是唯一的，並且不會在此主機上使用。

   >[!IMPORTANT]
   >
   >如果指定了root以外的帳戶，則必須確保在配置檔案中重新配置這些資料夾時，正確設定映像伺服器需要讀取和/或寫入的所有檔案和資料夾的訪問權限。
   >
   >「影像伺服」現在已安裝至[!DNL /usr/local/Scene7/ImageServing]。 某些影像呈現內容已安裝到[!DNL /usr/local/Scene7/ImageRendering]中。
   >
   >在安裝結束時，安裝嚮導將嘗試啟動映像伺服器。 如果未找到有效的許可證密鑰，則無法啟動映像伺服器。 如果存在有效的許可證且映像伺服器仍未啟動，請查閱日誌檔案。

>[!NOTE]
>
>如果安裝Image Serving後安裝了許可證，則必須在使用前手動啟動Image Server。
