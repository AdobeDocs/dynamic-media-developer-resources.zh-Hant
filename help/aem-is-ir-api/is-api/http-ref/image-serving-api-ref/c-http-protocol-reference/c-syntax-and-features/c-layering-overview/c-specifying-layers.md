---
description: 在URL或catalog Modifier指令序列中，圖層定義序列會以layer=指令開始，並以另一個layer=指令、effect=指令或URL結尾結束。
solution: Experience Manager
title: 指定圖層
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: bedd5dac-7577-4c8a-9dc3-43aa4438e53a
TQID: 'https://experienceleague.adobe.com/jNFpOYrBFWWc53JvzwENSjpM-SkIpenxxWPUgGX-p0Q'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 123
ht-degree: 0%

---

# 指定圖層{#specifying-layers}

在URL或catalog：：Modifier指令序列中，圖層定義序列會以layer=指令開始，並以另一個layer=指令、effect=指令或URL結尾結束。

圖層定義序列中的所有指令都與圖層相關聯。

`layer=`命令指定圖層編號，它必須是大於或等於0的整數。 圖層定義序列中具有相同圖層編號的所有指令都會套用至相同圖層。 如果同一個命令發生多次，則最後一個執行個體會佔上風。
