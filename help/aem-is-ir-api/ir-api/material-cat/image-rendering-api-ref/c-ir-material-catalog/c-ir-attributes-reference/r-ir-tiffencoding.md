---
title: TiffEncoding
description: TIFF編碼格式。 指定TIFF影像的壓縮格式（實際上是fmt=命令的第三個值的預設值）。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6a6fa8f5-4497-438d-914c-3f6d4c08ef09
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 4%

---

# TiffEncoding{#tiffencoding}

TIFF編碼格式。 指定TIFF影像的壓縮格式（實際上是`fmt=`命令第三個值的預設值）。

設定為`0`以不壓縮，`1`以LZW壓縮，`2`以deflate (ZIP)壓縮，以及`3`以JPEG壓縮。

## 屬性 {#section-469f5a1225464542866f5353edd92db3}

列舉。

## 預設 {#section-a3c5152a9f464e4987ed7c05d35b1169}

如果未定義或空白，則繼承自`default::TiffEncoding`。

## 另請參閱 {#section-1601425e5ac3486da4df8e7fa55981b2}

[fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c)
