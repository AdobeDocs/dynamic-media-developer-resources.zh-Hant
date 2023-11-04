---
description: 影像的檢視轉換
solution: Experience Manager
title: 影像的檢視轉換
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fc20cbc2-9d66-4c52-80c2-9ba7c3b54744
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 0%

---

# 影像的檢視轉換{#view-transform-for-images}

回應時傳回給使用者端的影像 `req=img` 請求是從複合影像衍生而來，考量到下列值： `wid=`， `hei=`， `fit=`， `scl=`， `rgn=`， `attribute::DefaultPix`， `attribute::MaxPix`和複合影像的大小。

如果 `wid=` 和 `hei=` 已指定，並且 `scl=` 不會，會縮放複合影像，使其完全符合所定義的檢視矩形 `wid=` 和 `hei=`. 如果檢視矩形的外觀比例與複合影像的外觀比例不同，則縮放後的複合影像會使用 `align=` 值（如果已指定），否則會置中。 影像資料未涵蓋的任何空間都會填滿 `bgc=` 或若未指定，則使用 `attribute::BkgColor`.

如果 `scl=` 指定時，複合影像會以該縮放係數縮放。 如果 `wid=` 和/或 `hei=` 也會指定，縮放的影像隨後會被裁剪成 `wid=` 和/或 `hei=` 或視需要新增額外空間。 `align=` 指定影像的裁切位置或新增額外空間，並填滿任何額外空間 `bgc=` 或 `attribute::BkgColor`.

如果兩者皆非 `wid=`， `hei=` 也不 `scl=` 都會指定，而且如果複合影像的寬度或高度超過 `attribute::DefaultPix`，則複合影像會縮放以不超過 `attribute::DefaultPix`. 否則，不使用縮放即可使用複合影像。

若要確保傳回檢視影像時不會進行任何進一步的縮放，請指定 `scl=1`.

如果 `rgn=` 指定後，回覆影像會據此裁切，以得出最終的回覆影像大小。 將此大小與 `attribute::MaxPix` （若已定義），且如果回覆影像在任一尺寸中較大，則會產生錯誤。

如果 `fmt=` 指定不含Alpha的資料，回覆影像中的任何透明區域都會填滿 `bgc=` 或 `attribute::BkgColor`.
