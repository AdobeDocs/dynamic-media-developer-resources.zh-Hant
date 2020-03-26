---
description: 如果請求成功完成，且請求中未包含req=命令，或req=img或req=tmb，則會傳回影像資料。
seo-description: 如果請求成功完成，且請求中未包含req=命令，或req=img或req=tmb，則會傳回影像資料。
seo-title: 影像
solution: Experience Manager
title: 影像
topic: Scene7 Image Serving - Image Rendering API
uuid: 715154b6-f9ac-459e-a566-f78a4ca4580d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 影像{#images}

如果請求成功完成，且請求中未包含req=命令，或req=img或req=tmb，則會傳回影像資料。

HTTP回應MIME類型由 `fmt=`或(如果未指 `fmt=` 定)決定 `<image/jpeg>`。

如果request方法為無條件或，則HTTP回應狀態為&#39;200 OK&#39; `GET` 。 `HEAD`

伺服器可以以狀態&#39;304&#39;（未修改）回覆，並且不響應條件性請求（包括有效或標題） `GET` 返回任何 `If-Modified-Since` 影像 `If-None-Match` 資料。
