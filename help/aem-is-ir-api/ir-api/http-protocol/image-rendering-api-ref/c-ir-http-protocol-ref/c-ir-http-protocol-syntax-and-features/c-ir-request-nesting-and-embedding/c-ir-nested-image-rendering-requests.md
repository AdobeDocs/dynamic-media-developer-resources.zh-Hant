---
description: 對於高級應用程式，可以將渲染操作的結果用作材料影像，就像從「影像服務」獲得的影像一樣。
seo-description: 對於高級應用程式，可以將渲染操作的結果用作材料影像，就像從「影像服務」獲得的影像一樣。
seo-title: 巢狀影像演算請求
solution: Experience Manager
title: 巢狀影像演算請求
topic: Scene7 Image Serving - Image Rendering API
uuid: 12551bd5-ff5f-45d6-81e9-5ba0be47a425
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 巢狀影像演算請求{#nested-image-rendering-requests}

對於高級應用程式，可以將渲染操作的結果用作材料影像，就像從「影像服務」獲得的影像一樣。

在命令中指定渲染請求，可將其用作材料圖 `src=` 像，如下所示：

` …&src=ir{ *[!DNL renderRequest]*}&…`

代 `ir` 號區分大小寫。

巢狀請求不得包含「影像演算」根路徑(通常 `http:// *[!DNL server]*/ir/render/'`)，但可能包含預處理規則Token。

在巢狀請求中指定（在請求URL中或在或中）時，會忽略 `catalog::Modifier` 下列命 `catalog::PostModifier`令：

* `fmt=`
* `qlt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `req=`
* `bgc=`

也會忽略套 `attribute::MaxPix` 用至 `attribute::DefaultPix` 巢狀演算請求的材質目錄。

可選擇性地通過包括來快取嵌套IR請求的影像結果 `cache=on`。 預設情況下，會禁用中間資料的快取。 只有當中間影像預期在合理時段內於不同請求中重複使用時，才應啟用快取。 套用標準伺服器端快取管理。 資料以無損格式快取。
