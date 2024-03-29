---
description: 支援四種型別的圖層。
solution: Experience Manager
title: 圖層型別
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9819a73d-1108-414a-831f-37ba94c3feb9
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 0%

---

# 圖層型別{#layer-types}

支援四種型別的圖層。

## 影像圖層 {#section-3e53df1437694272aca03f927fc0db07}

影像圖層必須有 `src=` 指定做為圖層的影像。 可透過指定單獨的影像 `mask=` 要做為圖層遮色片使用，或影像可能已經有Alpha色版。 影像圖層的大小一律會衍生自影像，但通常會使用縮放影像以符合大小。 `size=` 命令。 剪裁路徑可以套用 `clipPath=`.

## 文字圖層 {#section-dc2aec6416a340bcb20c1f884323c8d0}

必須有 `text=` 或 `textPs=` 以RTF文字片段的形式提供文字內容的命令。 文字圖層可以自行調整其內容大小，也可以指定明確的大小。 例如，如果要將文字換行成特定寬度，或文字必須限制在特定區域中。 `textPs=` 支援將文字排入定義的任意形狀 `textFlowPath=` 和至定義的任意路徑 `textPath=`. `textPs=` 也支援以任意角度將文字演算到文字方塊或指定形狀中( `textAngle=`)。

## 純色圖層 {#section-56dfb672756643dda08dc93294809eb0}

純色圖層通常用於範本中的圖層0，因此複合影像的大小是固定的且獨立於任何影像內容。 純色圖層需要 `color=` 屬性，以及 `size=` 或 `mask=`，並支援大部分其他指令和屬性來修改外觀。 純色圖層可以指定任意形狀 `clipPath=`.

## 效果圖層 {#section-dd3b628bc6734077af4c0ddcebcee05f}

Photoshop樣式的圖層效果（例如掉落陰影和光暈效果）是使用IS使用特殊子圖層來實作，這些子圖層可以附加到影像、文字和純色圖層。 這些效果圖層會繼承父圖層遮色片並從父圖層定位，功能也會受到限制。
