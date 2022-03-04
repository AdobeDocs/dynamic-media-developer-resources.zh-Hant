---
title: 嵌套影像呈現請求
description: 對於高級應用，可以將渲染操作的結果用作材料影像，就像從影像服務獲得的影像一樣。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 52c12786-bbe7-4410-87bb-6245d782a68c
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 0%

---

# 嵌套影像呈現請求{#nested-image-rendering-requests}

對於高級應用，可以將渲染操作的結果用作材料影像，就像從影像服務獲得的影像一樣。

通過在 `src=` 命令，如下所示：

` …&src=ir{ *[!DNL renderRequest]*}&…`

的 `ir` 令牌區分大小寫。

嵌套請求不得包括影像呈現根路徑(通常 `http:// *[!DNL server]*/ir/render/'`)，但可能包括預處理規則令牌。

當在嵌套請求中指定（在請求url中或在中）時，將忽略以下命令 `catalog::Modifier` 或 `catalog::PostModifier`):

* `fmt=`
* `qlt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `req=`
* `bgc=`

也忽略 `attribute::MaxPix` 和 `attribute::DefaultPix` 應用於嵌套渲染請求的材料目錄。

通過包括嵌套IR請求的影像結果可以選擇性地被快取 `cache=on`。 預設情況下，中間資料的快取被禁用。 僅當中間映像在合理的時間段內以不同請求重新使用時，才應啟用快取。 應用標準伺服器端快取管理。 資料以無損格式快取。
