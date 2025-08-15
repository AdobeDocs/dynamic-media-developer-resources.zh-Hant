---
title: Debug_trace記錄
description: 使用這些伺服器設定來偵錯追蹤記錄。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: fe1fc984-3c6b-4bd1-b5ba-630860ac7319
source-git-commit: 163ac6a6f44193f1b66ae24059630521d7247eae
workflow-type: tm+mt
source-wordcount: '404'
ht-degree: 0%

---

# Debug_trace記錄{#debug-trace-logging}

使用這些伺服器設定來偵錯追蹤記錄。

>[!NOTE]
>
>Adobe建議您將所有記錄檔設定為寫入與`TC::directory`相同的資料夾。 這麼做可確保所有「影像伺服」記錄檔都參與以`TC::maxDays`設定的自動記錄檔旋轉，避免因磁碟空間不足而造成伺服器不穩定。

## SV：：log — 伺服器監督員追蹤記錄檔路徑 {#section-3697bc480ff646e79cacc2812c55ef26}

伺服器管理員記錄檔的資料夾和基本檔案名稱。 路徑可以是絕對或相對於&#x200B;*[!DNL install_folder]*。 伺服器監督員會將連字型大小和目前日期( *[!DNL -yyyy-mm-dd]*)附加至檔案名稱（在檔案字尾之前，如果有的話）。 Adobe建議您將所有記錄檔傳送至與[!DNL Platform Server]記錄檔( `PS::LogFolder`)相同的資料夾，以使用[!DNL Platform Server] (`PS::LogDays`)實作的記錄檔管理。 預設值為[!DNL logs/Supervisor.log]。

>[!NOTE]
>
>必須先建立新資料夾，才能變更此設定。 請確定已設定存取許可權，讓伺服器管理員擁有必要的建立、讀取和寫入許可權。

## SV：：tracelevel — 伺服器監督員追蹤記錄層級 {#section-36f8634741da4c618d67aa628b5fe474}

記錄層級可以是1、2、3或4。 預設值為 2。

## IS：：Log — 影像伺服器偵錯記錄檔路徑 {#section-73a3f09b77f2446c9f82207b7d8aec39}

影像伺服器追蹤記錄檔的資料夾和基本檔案名稱。 路徑可以是絕對或相對於&#x200B;*[!DNL install_folder]*。 ImageServer會將連字型大小與目前日期( *[!DNL -yyyy-mm-dd]*)附加至檔案名稱（在檔案字尾之前，如果有的話）。 Adobe建議您將影像伺服器記錄檔傳送至與[!DNL Platform Server]記錄檔( `PS::LogFolder`)相同的資料夾，以使用由[!DNL Platform Server]實作的記錄檔管理（請參閱`PS::LogDays`）。

>[!NOTE]
>
>必須先建立新資料夾，才能變更此設定。 請確定已設定存取許可權，讓「影像伺服」具備必要的建立、讀取和寫入許可權。

## IS:TraceClient — 影像伺服器偵錯記錄層級 {#section-3851f1f68e404430985c629ac80534db}

記錄層級可以是1、2、3或4 （預設為2）

層級1會記錄與啟動、關閉及[!DNL Platform Server]連線相關的事件。

層級2也會記錄來源影像的連線與中斷連線。

層級3新增畫素資料的請求記錄以及畫素資料的傳遞到[!DNL Platform Server]。

層級4會記錄從[!DNL Platform Server]接收的所有郵件。

層級3和4應僅用於偵錯，因為記錄檔可能會變得很大。

## IS：：TraceStatsInterval — 影像伺服器統計記錄間隔 {#section-1d8df96d61044e33a5b2b2b0309c2d59}

影像伺服器會以此設定指定的間隔將記憶體統計資料寫入其追蹤記錄檔。 有效範圍為5至86,400秒。
