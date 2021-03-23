---
description: 影像遮色片。 請求遮色片（alpha色版）資料。
seo-description: 影像遮色片。 請求遮色片（alpha色版）資料。
seo-title: 遮罩
solution: Experience Manager
title: 遮罩
uuid: 9a8dc4bc-0757-45d2-adfe-d4bd69b4efa9
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 0%

---


# 掩碼{#mask}

影像遮色片。 請求遮色片（alpha色版）資料。

`req=mask`

支援與`req=img`相同的命令，並且由伺服器以相同的方式處理，但伺服器不返回RGB或RGBA資料，而是丟棄顏色資訊並僅返回蒙版（alpha通道）資料。 回覆資料格式和回應MIME類型由`fmt=`決定。

HTTP響應基於`catalog::Expiration`可以與TTL進行快取。
