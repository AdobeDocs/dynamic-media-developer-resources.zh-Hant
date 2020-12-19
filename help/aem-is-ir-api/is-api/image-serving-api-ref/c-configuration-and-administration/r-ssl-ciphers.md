---
description: server.xml中的Connector標籤支援密碼屬性，以限制可針對SSL連線選擇的密碼。
seo-description: server.xml中的Connector標籤支援密碼屬性，以限制可針對SSL連線選擇的密碼。
seo-title: 定義SSL密碼
solution: Experience Manager
title: 定義SSL密碼
topic: Scene7 Image Serving - Image Rendering API
uuid: 9490fb9a-5abb-4f5e-b660-b7af0a5e4b4d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 0%

---


# 定義SSL密碼{#defining-ssl-ciphers}

server.xml中的Connector標籤支援密碼屬性，以限制可針對SSL連線選擇的密碼。

依預設，所有密碼皆可使用。 清單以逗號分隔，可包含下列任一值：

`SSL_DHE_DSS_EXPORT_WITH_DES40_CBC_SHA`

`SSL_DHE_DSS_WITH_3DES_EDE_CBC_SHA`

`SSL_DHE_DSS_WITH_DES_CBC_SHA`

`SSL_DHE_RSA_EXPORT_WITH_DES40_CBC_SHA`

`SSL_DHE_RSA_WITH_3DES_EDE_CBC_SHA`

`SSL_DHE_RSA_WITH_DES_CBC_SHA`

`SSL_RSA_EXPORT_WITH_DES40_CBC_SHA`

`SSL_RSA_EXPORT_WITH_RC4_40_MD5`

`SSL_RSA_WITH_3DES_EDE_CBC_SHA`

`SSL_RSA_WITH_DES_CBC_SHA`

`SSL_RSA_WITH_RC4_128_MD5`

`SSL_RSA_WITH_RC4_128_SHA`

`TLS_DHE_DSS_WITH_AES_128_CBC_SHA`

`TLS_DHE_RSA_WITH_AES_128_CBC_SHA`

`TLS_RSA_WITH_AES_128_CBC_SHA`

如果值中有任何值錯誤，Tomcat將啟用每個密碼。 因此，在設定後使用外部工具檢查哪些密碼已實際啟用是十分必要的。

例如，下列組態將僅啟用「128位元」密碼套裝及以上版本：

`ciphers="SSL_DHE_DSS_WITH_3DES_EDE_CBC_SHA,SSL_DHE_DSS_WITH_DES_CBC_SHA,SSL_DHE_RSA_WITH_3DES_EDE_CBC_SHA,SSL_RSA_WITH_3DES_EDE_CBC_SHA,TLS_DHE_DSS_WITH_AES_128_CBC_SHA,TLS_DHE_RSA_WITH_AES_128_CBC_SHA,TLS_RSA_WITH_AES_128_CBC_SHA"`
