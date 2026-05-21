---
description: 影像遮色片。 要求遮罩（Alpha色版）資料。
solution: Experience Manager
title: 遮色片
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0e743fe5-a623-4f5f-bc61-536ed70532bf
TQID: 'https://experienceleague.adobe.com/FMsQMZsc3N1ToEzXBE0vOzkezfemSzT6NaGJQ1gQqd8'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 76
ht-degree: 0%

---

# 遮色片{#mask}

影像遮色片。 要求遮罩（Alpha色版）資料。

`req=mask`

支援與`req=img`相同的命令。 伺服器會以相同的方式處理它，但不會傳回RGB或RGBA資料，而是捨棄顏色資訊並只傳回遮色片(alpha channel)資料。 回覆資料格式和回應MIME型別由`fmt=`決定。

HTTP回應可使用以`catalog::Expiration`為基礎的TTL進行快取。
