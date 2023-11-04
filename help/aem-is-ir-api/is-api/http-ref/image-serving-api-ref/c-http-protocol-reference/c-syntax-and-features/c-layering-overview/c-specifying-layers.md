---
description: 在URL或catalog Modifier指令序列中，圖層定義序列會以layer=指令開始，並以另一個layer=指令、effect=指令或URL結尾結束。
solution: Experience Manager
title: 指定圖層
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: bedd5dac-7577-4c8a-9dc3-43aa4438e53a
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 0%

---

# 指定圖層{#specifying-layers}

在URL或catalog：：Modifier指令序列中，圖層定義序列會以layer=指令開始，並以另一個layer=指令、effect=指令或URL結尾結束。

圖層定義序列中的所有指令都與圖層相關聯。

此 `layer=` command指定圖層編號，它必須是大於或等於0的整數。 圖層定義序列中具有相同圖層編號的所有指令都會套用至相同圖層。 如果同一個命令發生多次，則最後一個執行個體會佔上風。
