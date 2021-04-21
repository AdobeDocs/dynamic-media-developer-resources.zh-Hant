---
description: 對於高級應用程式，可以將渲染操作的結果用作材料影像，就像從「影像服務」獲得的影像一樣。
solution: Experience Manager
title: 巢狀影像演算請求
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '198'
ht-degree: 0%

---


# 巢狀影像演算請求{#nested-image-rendering-requests}

對於高級應用程式，可以將渲染操作的結果用作材料影像，就像從「影像服務」獲得的影像一樣。

演算請求可在`src=`命令中指定，如下所示：

` …&src=ir{ *[!DNL renderRequest]*}&…`

`ir`代號區分大小寫。

巢狀請求不得包含「影像演算」根路徑（通常`http:// *[!DNL server]*/ir/render/'`），但可能包含預處理規則Token。

在巢狀請求中指定（在請求URL中或`catalog::Modifier`或`catalog::PostModifier`中）時，會忽略下列命令：

* `fmt=`
* `qlt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `req=`
* `bgc=`

套用至巢狀演算請求的材質目錄的`attribute::MaxPix`和`attribute::DefaultPix`也會被忽略。

可選擇性地通過包括`cache=on`來快取嵌套IR請求的影像結果。 預設情況下，會禁用中間資料的快取。 只有當中間影像預期在合理時段內於不同請求中重複使用時，才應啟用快取。 套用標準伺服器端快取管理。 資料以無損格式快取。
