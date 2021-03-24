---
description: 影像伺服器(IS)要求可用作材質影像。
solution: Experience Manager
title: 內嵌影像伺服器要求
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 0%

---


# 嵌入式映像伺服器請求{#embedded-image-server-requests}

影像伺服器(IS)要求可用作材質影像。

在`src=`命令中指定請求，如下所示：

` …&src=is( *[!DNL imageServingRequest]*)&…`

`is`代號區分大小寫。

巢狀請求不得包含「影像伺服」根路徑(通常為[!DNL http:// *[!DNL server]*/is/image/&quot;])，但可能包含預處理規則Token。

在巢狀請求中指定（在請求URL中或`catalog::Modifier`或`catalog::PostModifier`中）時，會忽略下列IS命令：

* `bgc=`
* `fmt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `qlt=`
* `quantize=`
* `req=`

同樣被忽略的是適用於嵌入式IS請求的映像目錄的`attribute::MaxPix`和`attribute::DefaultPix`。

如果巢狀請求的結果影像包含遮色片(alpha)資料，則一律會傳遞至材質。 使用純色背景影像圖層以避免不想要的alpha。

嵌入的IS請求的映像結果可通過包括`cache=on`來被選擇性地快取。 預設情況下，會禁用中間資料的快取。 只有當中間影像預期在合理時段內於不同請求中重複使用時，才應啟用快取。 套用標準伺服器端快取管理。 資料以無損格式快取。
