---
description: 設定媒體邊界。 設定PDF檔案中設定的媒體邊界。
solution: Experience Manager
title: mediaMargin
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5bba0dc2-a496-4380-9def-12f9e683eafb
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 0%

---

# mediaMargin{#mediamargin}

設定媒體邊界。 設定PDF檔案中設定的媒體邊界。

` mediaMargin=[ *[!DNL top]*[, *[!DNL left]*= *[!DNL top]*[, *[!DNL bottom]*= *[!DNL top]*[, *[!DNL right]*= *[!DNL left]*]]]]`點

根據預設，`mediaMargin`設定為由`viewWidth`和`viewHeight`定義之檔案的完整大小。 如果未指定，*[!DNL left]*、*[!DNL bottom]*&#x200B;和&#x200B;*[!DNL right]*&#x200B;值會預設為&#x200B;*[!DNL top]*&#x200B;值。
