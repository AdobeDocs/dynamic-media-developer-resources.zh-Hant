---
description: 使用這些伺服器設定設定映像大小限制。
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

使用這些伺服器設定設定映像大小限制。

## IS::MaxMessageSize — 響應大小限制 {#section-bd942385d4d144cd904003695d72c85e}

限制允許映像伺服器發送到的資料的大小 [!DNL Platform Server]。 這有效地限制了Image Serving可通過HTTP(MB)返回到客戶端的編碼/壓縮響應映像的大小。

## IS::MaxRenderRgnPixels — 輸出影像大小限制 {#section-868ceb9764dd42dfb133ffeb72f9d3fb}

限制影像伺服器可以生成的影像的大小（不包括保存到檔案中的影像）。 大於0的整數值（以百萬像素為單位）。 如果渲染操作將超過大小限制，則返回錯誤。 預設為 16。

## IS::MaxSavePixels — 保存到檔案的大小限制 {#section-d1547c4afa88467080ab08356f775e06}

限制Image Server將寫入檔案的映像大小 `req=saveToFile` 的子菜單。 大於0的整數值（以百萬像素為單位）。 如果檔案保存操作將超過該限制，則返回錯誤。 預設值為1億像素。

## IS::MaxNonDsfSize — 非PTIFF輸入影像的大小限制 {#section-50de28a7158a436393cce5da0d1e4d46}

允許影像伺服器開啟的非PTIFF影像的最大大小（以M像素為單位）。 當嘗試訪問大於此限制的非PTIFF影像時，影像服務將返回錯誤。

>[!NOTE]
>
>將此值設定得太高可能會導致映像伺服器記憶體不足，並導致故障，包括崩潰。
