---
description: 「影像伺服」支援ISO-8859-1和UTF-8編碼的影像目錄。
seo-description: 「影像伺服」支援ISO-8859-1和UTF-8編碼的影像目錄。
seo-title: 字元編碼
solution: Experience Manager
title: 字元編碼
topic: Scene7 Image Serving - Image Rendering API
uuid: dfb56411-40d1-4bac-9213-9104ecba2a02
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 0%

---


# 字元編碼{#character-encoding}

「影像伺服」支援ISO-8859-1和UTF-8編碼的影像目錄。

位元組順序標籤(BOM)用於指定每個檔案的編碼。 對於UTF-8,BOM是位元組序列`EF BB BF`。 在每個影像目錄檔案的開頭處偵測到此字元序列時，會假設使用UTF-8編碼。 任何其他位元組序列都會導致檔案被解譯為已編碼至ISO-8859-1標準。

許多當代應用程式在設定為UTF-8時，會自動插入BOM。
