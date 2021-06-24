---
description: 影像遮色片。 請求遮色片（Alpha通道）資料。
solution: Experience Manager
title: 遮罩
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 0e743fe5-a623-4f5f-bc61-536ed70532bf
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 0%

---

# 遮罩{#mask}

影像遮色片。 請求遮色片（Alpha通道）資料。

`req=mask`

支援與`req=img`相同的命令。 伺服器會以相同方式處理它，但伺服器不會傳回RGB或RGBA資料，而會捨棄顏色資訊，僅傳回遮色片（Alpha色版）資料。 回覆資料格式和回應MIME類型由`fmt=`決定。

HTTP回應可根據`catalog::Expiration`與TTL快取。
