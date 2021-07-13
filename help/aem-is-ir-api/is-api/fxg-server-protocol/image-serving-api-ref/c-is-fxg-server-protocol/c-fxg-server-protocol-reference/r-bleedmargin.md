---
description: 設定出血邊界。 設定在PDF檔案中設定的出血邊界。
solution: Experience Manager
title: 下限
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: badb8ca5-52ba-4b44-b53f-fb302626adc4
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '62'
ht-degree: 0%

---

# 下限{#bleedmargin}

設定出血邊界。 設定在PDF檔案中設定的出血邊界。

`bleedMargin=[ *[!DNL top]*[, *[!DNL left]*= *[!DNL top]*[, *[!DNL bottom]*= *[!DNL top]*[, *[!DNL right]*= *[!DNL left]*]]]]` 點

預設情況下，`bleedMargin`設定為`viewWidth`和`viewHeight`所定義的文檔的完整大小。 若未指定，*[!DNL left]*、*[!DNL bottom]*&#x200B;和&#x200B;*[!DNL right]*&#x200B;值會預設為&#x200B;*[!DNL top]*&#x200B;值。
