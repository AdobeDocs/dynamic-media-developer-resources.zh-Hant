---
title: 字元編碼
description: 影像呈現支援使用ISO-8859-1和UTF-8編碼的材料目錄。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ee7b33fd-7607-4bff-867b-6e7a837a9ed4
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 0%

---

# 字元編碼{#character-encoding}

影像呈現支援使用ISO-8859-1和UTF-8編碼的材料目錄。

位元組順序標籤(BOM)用於指定每個檔案的編碼。 對於UTF-8,BOM是位元組序列 `EF BB BF`。 當在每個材料目錄檔案的開頭檢測到此字元序列時，假定使用UTF-8編碼。 任何其他位元組序列導致檔案被解釋為已編碼到ISO-8859-1標準。

許多當代應用程式在配置為UTF-8時，會自動插入BOM。
