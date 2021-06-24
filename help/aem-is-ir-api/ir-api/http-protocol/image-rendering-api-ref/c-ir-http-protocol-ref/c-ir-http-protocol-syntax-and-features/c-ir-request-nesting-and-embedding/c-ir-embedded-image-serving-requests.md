---
description: 影像伺服器(IS)請求可用作材料影像。
solution: Experience Manager
title: 內嵌影像伺服器請求
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 4ece9738-45e0-43c0-ba1c-2a05ef1f39be
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 0%

---

# 內嵌影像伺服器請求{#embedded-image-server-requests}

影像伺服器(IS)請求可用作材料影像。

在`src=`命令中指定請求，如下所示：

` …&src=is( *[!DNL imageServingRequest]*)&…`

`is`代號區分大小寫。

巢狀請求不得包含「影像伺服」根路徑(通常為[!DNL http:// *[!DNL server]*/is/image/&quot;])，但可能包含預先處理規則Token。

在巢狀請求中指定時（在請求URL中或`catalog::Modifier`或`catalog::PostModifier`中），會忽略下列IS命令：

* `bgc=`
* `fmt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `qlt=`
* `quantize=`
* `req=`

套用至內嵌IS請求的影像目錄的`attribute::MaxPix`和`attribute::DefaultPix`也會遭到忽略。

如果巢狀請求的結果影像包含遮色片(Alpha)資料，則一律會傳遞至材料。 使用純色背景影像層來避免不想要的Alpha。

可選擇包含`cache=on`來快取內嵌IS要求的影像結果。 預設會停用中繼資料的快取。 只有當中間映像預期在合理的時間段內在不同請求中重複使用時，才應啟用快取。 標準伺服器端快取管理適用。 資料以無損格式快取。
