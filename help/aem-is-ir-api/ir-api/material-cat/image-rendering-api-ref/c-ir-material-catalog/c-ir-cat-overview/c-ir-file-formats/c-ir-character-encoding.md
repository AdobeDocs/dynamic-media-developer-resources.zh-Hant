---
description: 影像演算支援ISO-8859-1和UTF-8編碼的材質型錄。
solution: Experience Manager
title: 字元編碼
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 0%

---


# 字元編碼{#character-encoding}

影像演算支援ISO-8859-1和UTF-8編碼的材質型錄。

位元組順序標籤(BOM)用於指定每個檔案的編碼。 對於UTF-8,BOM是位元組序列`EF BB BF`。 在每個材料目錄檔案的開頭處檢測到此字元序列時，假定使用UTF-8編碼。 任何其他位元組序列都會導致檔案被解譯為已編碼至ISO-8859-1標準。

許多當代應用程式在設定為UTF-8時，會自動插入BOM。
