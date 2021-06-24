---
description: 影像轉譯支援ISO-8859-1和UTF-8編碼的材料目錄。
solution: Experience Manager
title: 字元編碼
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: ee7b33fd-7607-4bff-867b-6e7a837a9ed4
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 0%

---

# 字元編碼{#character-encoding}

影像轉譯支援ISO-8859-1和UTF-8編碼的材料目錄。

位元組順序標籤(BOM)用於指定每個檔案的編碼。 對於UTF-8,BOM是位元組序列`EF BB BF`。 在每個材料目錄檔案的開頭檢測到此字元序列時，會假設使用UTF-8編碼。 任何其他位元組序列都會導致檔案被解釋為已編碼至ISO-8859-1標準。

許多當代應用程式在配置為UTF-8時，會自動插入BOM。
