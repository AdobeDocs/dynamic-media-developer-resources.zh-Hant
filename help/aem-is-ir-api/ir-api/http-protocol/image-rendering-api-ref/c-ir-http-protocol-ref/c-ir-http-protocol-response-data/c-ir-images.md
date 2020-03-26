---
description: 如果請求成功完成，且請求中未包含req=命令，或req=包含下列值之一，則會傳回影像資料img, debug
seo-description: 如果請求成功完成，且請求中未包含req=命令，或req=包含下列值之一，則會傳回影像資料img, debug
seo-title: 影像
solution: Experience Manager
title: 影像
topic: Scene7 Image Serving - Image Rendering API
uuid: 8e8c5ec9-dc15-4894-b6a1-8e5241f03977
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 影像{#images}

如果請求成功完成，且請求中未包含req=命令，或req=包含下列值之一，則會傳回影像資料：img, debug

HTTP回應MIME類型由 `fmt=`或，若未 `fmt=` 指定，則取決於的值 `attribute::Format`。

如果request方法為無條件或，則HTTP回應狀態為&#39;200 OK&#39; `GET` 。 `HEAD`

伺服器可以以狀態&#39;304&#39;（未修改）回覆，並且不返回任何影像資料以響應條件 `GET` 性請求(該 [!DNL If-Modified-Since] 欄位在中 `request-header`)。
