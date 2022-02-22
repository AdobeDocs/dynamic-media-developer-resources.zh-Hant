---
title: 首次安裝
description: 此過程說明如何在Linux®上首次安裝Image Serving。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f27e6b27-641c-4a88-9ed0-94ada9ba75a9
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '380'
ht-degree: 0%

---

# 首次安裝{#installing-for-the-first-time}

此過程說明如何在Linux®上首次安裝Image Serving。

1. 使用根權限登錄到伺服器主機。
1. 建立資料夾 [!DNL /usr/local/scene7/licenses]。

   如果影像服務和/或影像呈現許可證密鑰檔案(使用 [!DNL .sc8] 檔案尾碼)可用，將其複製到此資料夾。 否則，請繼續安裝，稍後安裝許可證密鑰。
1. 解壓縮並解壓縮Image Serving分發tar檔案。
1. 在 [!DNL Setup] 資料夾，通過運行啟動安裝嚮導 [!DNL ./install-is]。

   如果找不到許可證密鑰，則顯示說明如何獲取許可證檔案。 此時執行此操作，或繼續安裝映像服務，稍後安裝許可證密鑰。
1. 顯示最終用戶許可協定(EULA)時，請閱讀許可協定，然後輸入 `y` 繼續。

   安裝程式將顯示下表中列出的提示。

<table id="table_0E7B673CAD8E4C5EB72F8283A0DDEFC8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 主偵聽埠[8080]:</span> </p> </td>
   <td colname="col2"> <p>用於影像服務和影像呈現的主HTTP偵聽埠。 </p> </td>
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 管理員偵聽埠[8083]:</span> </p> </td> 
   <td colname="col2"> <p>管理員偵聽埠。 </p> </td>
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
   <td colname="col2"> <p>要安裝映像伺服器的用戶帳戶。 </p> </td>
  </tr>
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 映像伺服器組ID [root]:</span> </p> </td>
   <td colname="col2"> <p>要安裝映像伺服器的組帳戶。 </p> </td>
  </tr>
 </tbody>
</table>

1. 按 **[!UICONTROL 輸入]** 接受預設值或指定其他值。

   確保指定的所有埠號都是唯一的，並且不在此主機上使用。

   >[!IMPORTANT]
   >
   >如果指定了除根帳戶之外的帳戶，則必須確保在配置檔案中重新配置這些資料夾時正確設定了映像伺服器需要讀取和寫入的所有檔案和資料夾的訪問權限。
   >
   >映像服務現在已安裝到 [!DNL /usr/local/Scene7/ImageServing]。 某些影像呈現內容安裝到 [!DNL /usr/local/Scene7/ImageRendering]。
   >
   >在安裝接近尾聲時，安裝嚮導會嘗試啟動映像伺服器。 如果找不到有效的許可證密鑰，則無法啟動映像伺服器。 如果存在有效的許可證且映像伺服器仍未啟動，請查閱日誌檔案。

>[!NOTE]
>
>如果在安裝Image Serving後安裝了許可證，則必須在使用前手動啟動Image Server。
