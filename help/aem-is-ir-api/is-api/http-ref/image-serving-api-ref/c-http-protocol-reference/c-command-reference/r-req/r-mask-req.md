---
description: 影像遮色片。 請求遮色片（alpha色版）資料。
seo-description: 影像遮色片。 請求遮色片（alpha色版）資料。
seo-title: 遮罩
solution: Experience Manager
title: 遮罩
topic: Scene7 Image Serving - Image Rendering API
uuid: 9a8dc4bc-0757-45d2-adfe-d4bd69b4efa9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# mask{#mask}

影像遮色片。 請求遮色片（alpha色版）資料。

`req=mask`

伺服器支援與 `req=img`相同的命令，並由伺服器以相同的方式處理，但伺服器不返回RGB或RGBA資料，而是丟棄顏色資訊並僅返回蒙版（alpha通道）資料。 回覆資料格式和回應MIME類型由決定 `fmt=`。

The HTTP response is cacheable with the TTL based on `catalog::Expiration`.
