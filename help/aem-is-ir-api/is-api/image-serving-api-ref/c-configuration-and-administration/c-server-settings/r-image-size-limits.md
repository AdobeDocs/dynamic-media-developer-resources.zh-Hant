---
description: 使用這些伺服器設定來設定影像大小限制。
solution: Experience Manager
title: 影像大小限制
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 75ec58ee-8c98-46cb-96b2-79d1c32e576f
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 0%

---

# 影像大小限制{#image-size-limits}

使用這些伺服器設定來設定影像大小限制。

## IS::MaxMessageSize — 回應大小限制 {#section-bd942385d4d144cd904003695d72c85e}

限制允許影像伺服器發送到的資料大小 [!DNL Platform Server]. 這有效地限制了編碼/壓縮響應映像的大小，Image Serving可以通過HTTP(MB)返回到客戶端。

## IS::MaxRenderRgnPixels — 輸出影像大小限制 {#section-868ceb9764dd42dfb133ffeb72f9d3fb}

限制影像伺服器可生成的影像的大小（排除保存到檔案的影像）。 大於0的整數值（以百萬像素為單位）。 如果呈現操作超過大小限制，則返回錯誤。 預設為 16。

## IS::MaxSavePixels — 儲存至檔案的大小限制 {#section-d1547c4afa88467080ab08356f775e06}

限制Image Server將寫入檔案的影像大小 `req=saveToFile` 命令。 大於0的整數值（以百萬像素為單位）。 如果檔案儲存操作超過該限制，則會傳回錯誤。 預設為1億像素。

## IS::MaxNonDsfSize — 非PTIFF輸入影像的大小限制 {#section-50de28a7158a436393cce5da0d1e4d46}

允許影像伺服器開啟的非PTIFF影像的最大大小（以M像素為單位）。 嘗試存取大於此限制的非PTIFF影像時，「影像伺服」會傳回錯誤。

>[!NOTE]
>
>將此值設定得太高可能會導致映像伺服器記憶體不足，並導致故障（包括崩潰）。
