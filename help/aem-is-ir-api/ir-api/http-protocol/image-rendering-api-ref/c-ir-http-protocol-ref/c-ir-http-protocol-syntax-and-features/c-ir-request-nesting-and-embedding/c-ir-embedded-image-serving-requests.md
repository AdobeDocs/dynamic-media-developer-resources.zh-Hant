---
title: 內嵌影像伺服器要求
description: 影像伺服器(IS)要求可作為材質影像使用。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4ece9738-45e0-43c0-ba1c-2a05ef1f39be
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 0%

---

# 內嵌影像伺服器要求{#embedded-image-server-requests}

影像伺服器(IS)要求可作為材質影像使用。

在`src=`命令中指定要求，如下所示：

` …&src=is( *[!DNL imageServingRequest]*)&…`

`is`權杖區分大小寫。

巢狀要求不得包含「影像伺服」根路徑（通常為 [!DNL http:// *[!DNL server]*/is/image/"]），但可能包含前置處理規則權杖。

在巢狀要求中指定下列IS命令時（在要求URL中或在`catalog::Modifier`或`catalog::PostModifier`中），會略過這些命令：

* `bgc=`
* `fmt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `qlt=`
* `quantize=`
* `req=`

套用至內嵌IS要求的影像目錄中有`attribute::MaxPix`和`attribute::DefaultPix`個也遭到忽略。

如果巢狀請求的結果影像包含遮色片(alpha)資料，則會一律傳遞至材質。 使用純色背景影像圖層來避免不需要的Alpha。

內嵌IS要求的影像結果可透過包含`cache=on`選擇性地進行快取。 依預設，會停用中繼資料的快取。 只有在合理時段內於不同請求中重複使用中間影像時，才應啟用快取。 標準伺服器端快取管理適用。 資料會以無損格式快取。
