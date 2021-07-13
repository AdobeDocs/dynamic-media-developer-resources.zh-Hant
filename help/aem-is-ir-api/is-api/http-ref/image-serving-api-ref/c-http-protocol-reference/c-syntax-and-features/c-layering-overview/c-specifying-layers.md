---
description: 在URL或目錄修飾符命令序列中，層定義序列以layer=命令開頭，以另一個layer=命令、effect=命令或URL的結尾終止。
solution: Experience Manager
title: 指定圖層
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: bedd5dac-7577-4c8a-9dc3-43aa4438e53a
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 0%

---

# 指定圖層{#specifying-layers}

在URL或目錄：:Modifier命令序列中，層定義序列以layer=命令開頭，以另一個layer=命令、effect=命令或URL的結尾終止。

層定義序列中的所有命令都與層相關聯。

`layer=`命令指定層號，該層號必須是整數0或更大。 具有相同層編號的層定義序列中的所有命令都應用到同一層。 如果同一命令多次發生，則最後一個實例將佔優。
