---
description: 影像蒙版。 請求掩碼（Alpha通道）資料。
solution: Experience Manager
title: 掩模
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0e743fe5-a623-4f5f-bc61-536ed70532bf
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 0%

---

# 掩模{#mask}

影像蒙版。 請求掩碼（Alpha通道）資料。

`req=mask`

支援與 `req=img`。 伺服器以相同方式處理它，但伺服器不返回RGB或RGBA資料，而是丟棄顏色資訊並僅返回掩碼（Alpha通道）資料。 答復資料格式和響應MIME類型由 `fmt=`。

HTTP響應可以與基於的TTL進行快取 `catalog::Expiration`。
