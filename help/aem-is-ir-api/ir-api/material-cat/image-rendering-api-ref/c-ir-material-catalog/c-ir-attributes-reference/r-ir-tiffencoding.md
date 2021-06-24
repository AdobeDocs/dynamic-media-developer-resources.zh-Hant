---
description: TIFF編碼格式。 指定TIFF影像的壓縮格式（實際上是fmt=命令的第三個值的預設值）。
solution: Experience Manager
title: TiffEncoding
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 6a6fa8f5-4497-438d-914c-3f6d4c08ef09
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '77'
ht-degree: 5%

---

# TiffEncoding{#tiffencoding}

TIFF編碼格式。 指定TIFF影像的壓縮格式（實際上是fmt=命令的第三個值的預設值）。

若無壓縮，則設為0；若為LZW，則設為1；若為減氣(ZIP)，則設為2；若為JPEG壓縮，則設為3。

## 屬性 {#section-469f5a1225464542866f5353edd92db3}

列舉。

## 預設 {#section-a3c5152a9f464e4987ed7c05d35b1169}

如果未定義或為空，則從`default::TiffEncoding`繼承。

## 另請參閱 {#section-1601425e5ac3486da4df8e7fa55981b2}

[fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c)
