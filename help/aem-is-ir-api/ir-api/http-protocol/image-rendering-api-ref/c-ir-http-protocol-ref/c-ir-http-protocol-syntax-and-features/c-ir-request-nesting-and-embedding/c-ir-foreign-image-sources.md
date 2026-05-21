---
title: 外部影像來源
description: 「影像伺服」支援對外國HTTP和FTP伺服器上的來源影像的存取。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 90f96a76-e9f3-4ad0-84af-bc0d093acf19
TQID: 'https://experienceleague.adobe.com/doS6fbVfaXGtLVNBAmOkB-TquNmOc5B2B--IewouFDY'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 103
ht-degree: 0%

---

# 外部影像來源{#foreign-image-sources}

「影像伺服」支援對外國HTTP和FTP伺服器上的來源影像的存取。

若要為`src=`或`mask=`命令指定外部URL，只要使用大括弧分隔整個內嵌URL即可：

` …&src={ *[!DNL foreignUrl]*}&…`

允許完整的絕對URL （如果已設定`attribute::AllowDirectUrls`）和相對`attribute::RootUrl`的URL。 如果內嵌絕對URL且屬性： `AllowDirectUrls`為0，或如果指定了相對URL且`attribute::RootUrl`為空白，則會發生錯誤。

伺服器會根據HTTP回應隨附的快取標頭來快取外部影像。
