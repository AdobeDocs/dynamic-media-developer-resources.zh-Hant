---
description: 使用這些伺服器設定來設定影像大小限制。
solution: Experience Manager
title: 影像大小限制
feature: Dynamic Media經典，SDK/API
role: 開發人員、管理員、商業從業人員
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 0%

---


# 影像大小限制{#image-size-limits}

使用這些伺服器設定來設定影像大小限制。

## IS::MaxMessageSize —— 響應大小限制{#section-bd942385d4d144cd904003695d72c85e}

限制允許將映像伺服器發送到平台伺服器的資料大小。 這有效地限制了「影像伺服」可透過HTTP(MB)傳回給用戶端的編碼／壓縮回應影像大小。

## IS::MaxRenderRgnPixels —— 輸出影像大小限制{#section-868ceb9764dd42dfb133ffeb72f9d3fb}

限制影像伺服器可產生的影像大小（排除儲存至檔案的影像）。 大於0的整數值（以百萬像素為單位）。 如果演算作業超過大小限制，則會傳回錯誤。 預設為 16。

## IS::MaxSavePixels —— 保存到檔案的大小限制{#section-d1547c4afa88467080ab08356f775e06}

使用`req=saveToFile`命令限制影像伺服器將寫入檔案的影像大小。 大於0的整數值（以百萬像素為單位）。 如果檔案保存操作超過該限制，則返回錯誤。 預設為1億像素。

## IS::MaxNonDsfSize —— 非PTIFF輸入影像的大小限制{#section-50de28a7158a436393cce5da0d1e4d46}

允許影像伺服器開啟的非PTIFF影像的最大大小（以Mpixels為單位）。 當嘗試存取大於此限制的非PTIFF影像時，「影像伺服」會傳回錯誤。

>[!NOTE]
>
>將此值設定得太高可能導致映像伺服器缺少記憶體，並導致故障（包括崩潰）。

