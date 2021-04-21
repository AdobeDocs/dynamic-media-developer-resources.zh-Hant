---
description: 影像遮色片。 請求遮色片（alpha色版）資料。
solution: Experience Manager
title: 遮罩
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: ddfccb4ca157764e39fc719d96b63e6ee95304bf
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 0%

---


# 掩碼{#mask}

影像遮色片。 請求遮色片（alpha色版）資料。

`req=mask`

支援與`req=img`相同的命令。 伺服器會以相同的方式處理它，但伺服器不會傳回RGB或RGBA資料，而會捨棄色彩資訊，只傳回遮色片（alpha色版）資料。 回覆資料格式和回應MIME類型由`fmt=`決定。

HTTP響應基於`catalog::Expiration`可以與TTL進行快取。
