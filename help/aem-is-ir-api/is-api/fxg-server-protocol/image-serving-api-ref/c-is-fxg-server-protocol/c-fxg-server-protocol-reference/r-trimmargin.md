---
description: 設定修剪邊距。 設定在PDF檔案中設定的修剪邊距。
solution: Experience Manager
title: 裁切邊距
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: dc6e31f8-d3be-44d3-8342-a4ef4b3fd61b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 0%

---

# 裁切邊距{#trimmargin}

設定修剪邊距。 設定在PDF檔案中設定的修剪邊距。

` trimMargin=[ *[!DNL top]*[, *[!DNL left]*= *[!DNL top]*[, *[!DNL bottom]*= *[!DNL top]*[, *[!DNL right]*= *[!DNL left]*]]]]` 點

預設情況下， `trimMargin` 設定為由定義的文檔的全部大小 `viewWidth` 和 `viewHeight`。 的 *[!DNL left]*。 *[!DNL bottom]*, *[!DNL right]* 值預設為 *[!DNL top]* 值。
