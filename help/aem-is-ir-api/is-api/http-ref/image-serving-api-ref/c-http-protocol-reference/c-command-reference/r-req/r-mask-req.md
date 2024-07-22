---
description: 影像遮色片。 要求遮罩（Alpha色版）資料。
solution: Experience Manager
title: 遮色片
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0e743fe5-a623-4f5f-bc61-536ed70532bf
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 0%

---

# 遮色片{#mask}

影像遮色片。 要求遮罩（Alpha色版）資料。

`req=mask`

支援與`req=img`相同的命令。 伺服器會以相同的方式處理它，但不會傳回RGB或RGBA資料，而是捨棄顏色資訊，只傳回遮色片(alpha channel)資料。 回覆資料格式和回應MIME型別由`fmt=`決定。

HTTP回應可使用以`catalog::Expiration`為基礎的TTL進行快取。
