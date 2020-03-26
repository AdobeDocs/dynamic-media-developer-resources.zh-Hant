---
description: 影像（預設）。 要求標準影像資料。
seo-description: 影像（預設）。 要求標準影像資料。
seo-title: img
solution: Experience Manager
title: img
topic: Scene7 Image Serving - Image Rendering API
uuid: 4809f916-0ccf-4a24-a93b-c51ed6203061
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# img{#img}

影像（預設）。 要求標準影像資料。

`req=img`

回覆資料格式和回應MIME類型由決定 `fmt=`。 `req=img` 是預設請求類型，不需要明確指定。 The HTTP response is cacheable with the TTL based on `catalog::Expiration`.

其他請求命令會如檔案所述應用。
