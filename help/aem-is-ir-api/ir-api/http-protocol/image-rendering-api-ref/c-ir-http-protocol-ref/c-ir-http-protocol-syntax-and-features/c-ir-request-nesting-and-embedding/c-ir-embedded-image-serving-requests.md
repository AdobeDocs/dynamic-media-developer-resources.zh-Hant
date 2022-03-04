---
title: 嵌入式映像伺服器請求
description: 影像伺服器(IS)請求可以用作材料影像。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4ece9738-45e0-43c0-ba1c-2a05ef1f39be
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 0%

---

# 嵌入式映像伺服器請求{#embedded-image-server-requests}

影像伺服器(IS)請求可以用作材料影像。

在 `src=` 命令，如下所示：

` …&src=is( *[!DNL imageServingRequest]*)&…`

的 `is` 令牌區分大小寫。

嵌套請求不得包括Image Service根路徑(通常 [!DNL http:// *[!DNL server]*/is/image/"])，但可能包括預處理規則令牌。

當在嵌套請求中指定（在請求URL中或在中）時，將忽略以下IS命令 `catalog::Modifier` 或 `catalog::PostModifier`):

* `bgc=`
* `fmt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `qlt=`
* `quantize=`
* `req=`

也忽略 `attribute::MaxPix` 和 `attribute::DefaultPix` 應用於嵌入式IS請求的影像目錄。

如果嵌套請求的結果影像包括掩碼(α)資料，則始終將其傳遞給材料。 使用純色背景影像圖層以避免不希望的Alpha。

可選地通過包括嵌入式IS請求的影像結果來快取 `cache=on`。 預設情況下，中間資料的快取被禁用。 僅當中間映像在合理的時間段內以不同請求重新使用時，才應啟用快取。 應用標準伺服器端快取管理。 資料以無損格式快取。
