---
description: Image Service支援使用ISO-8859-1和UTF-8編碼的映像目錄。
solution: Experience Manager
title: 字元編碼
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e6e50c2a-53d3-4776-a3f6-4a9d3407e562
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 0%

---

# 字元編碼{#character-encoding}

Image Service支援使用ISO-8859-1和UTF-8編碼的映像目錄。

位元組順序標籤(BOM)用於指定每個檔案的編碼。 對於UTF-8,BOM是位元組序列 `EF BB BF`。 當在每個影像目錄檔案的開頭檢測到此字元序列時，假定使用UTF-8編碼。 任何其他位元組序列導致檔案被解釋為已編碼到ISO-8859-1標準。

許多當代應用程式在配置為UTF-8時會自動插入BOM。
