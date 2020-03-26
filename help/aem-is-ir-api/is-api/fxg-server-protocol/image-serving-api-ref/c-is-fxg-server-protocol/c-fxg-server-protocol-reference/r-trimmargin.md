---
description: 設定修剪邊界。 設定在PDF檔案中設定的修剪邊界。
seo-description: 設定修剪邊界。 設定在PDF檔案中設定的修剪邊界。
seo-title: trimMargin
solution: Experience Manager
title: trimMargin
topic: Scene7 Image Serving - Image Rendering API
uuid: af94f9e8-a32e-439a-817a-a40aa8dc7dd4
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# trimMargin{#trimmargin}

設定修剪邊界。 設定在PDF檔案中設定的修剪邊界。

` trimMargin=[ *[!DNL top]*[, *[!DNL left]*= *[!DNL top]*[, *[!DNL bottom]*= *[!DNL top]*[, *[!DNL right]*= *[!DNL left]*]]]]` 點

預設情況下， `trimMargin` 將設定為由和定義的文檔的完 `viewWidth` 整大小 `viewHeight`。 如 *[!DNL left]*&#x200B;果未指 *[!DNL bottom]*&#x200B;定，則 *[!DNL right]* 會將值、值和 *[!DNL top]* 值預設為值。
