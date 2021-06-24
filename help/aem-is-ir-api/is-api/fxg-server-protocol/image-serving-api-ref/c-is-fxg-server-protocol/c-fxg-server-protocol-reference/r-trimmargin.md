---
description: 設定修剪邊距。 設定在PDF檔案中設定的修剪邊界。
solution: Experience Manager
title: trimMargin
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: dc6e31f8-d3be-44d3-8342-a4ef4b3fd61b
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '62'
ht-degree: 0%

---

# trimMargin{#trimmargin}

設定修剪邊距。 設定在PDF檔案中設定的修剪邊界。

` trimMargin=[ *[!DNL top]*[, *[!DNL left]*= *[!DNL top]*[, *[!DNL bottom]*= *[!DNL top]*[, *[!DNL right]*= *[!DNL left]*]]]]` 點

預設情況下，`trimMargin`設定為`viewWidth`和`viewHeight`所定義的文檔的完整大小。 若未指定，*[!DNL left]*、*[!DNL bottom]*&#x200B;和&#x200B;*[!DNL right]*&#x200B;值會預設為&#x200B;*[!DNL top]*&#x200B;值。
