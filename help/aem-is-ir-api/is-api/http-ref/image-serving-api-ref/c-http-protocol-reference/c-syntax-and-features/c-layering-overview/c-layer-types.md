---
description: 支援四種類型的層。
solution: Experience Manager
title: 圖層類型
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9819a73d-1108-414a-831f-37ba94c3feb9
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 0%

---

# 圖層類型{#layer-types}

支援四種類型的層。

## 影像層 {#section-3e53df1437694272aca03f927fc0db07}

影像層必須具有`src=`命令，該命令指定要用作圖層的影像。 可以用`mask=`指定單獨的影像以用作層掩模，或者該影像可能已具有Alpha通道。 影像層的大小始終從影像中導出，但通常使用`size=`命令縮放影像以適合。 剪輯路徑可以與`clipPath=`一起應用。

## 文字層 {#section-dc2aec6416a340bcb20c1f884323c8d0}

必須具有`text=`或`textPs=`命令，該命令以RTF格式文本片段的形式提供文本內容。 文本圖層可以根據其內容自行調整大小，或者可以給定明確大小（例如，文本要包裝到特定寬度，或者文本必須限制在特定區域內）。 `textPs=` 支援將文本流入由定義的任意形狀， `textFlowPath=` 並流入由定義的任意路 `textPath=`徑。`textPs=` 也支援將文本渲染到文本框或以任意角度指定形狀( `textAngle=`)。

## 實色層 {#section-56dfb672756643dda08dc93294809eb0}

模板中通常將實色層用於圖層0，因此複合影像的大小是固定的，並且與任何影像內容無關。 實色層需要`color=`屬性，以及`size=`或`mask=`，並且支援大多數其它命令和屬性來修改外觀。 可使用`clipPath=`給定任意形狀的實色層。

## 效果層 {#section-dd3b628bc6734077af4c0ddcebcee05f}

Photoshop樣式的圖層效果（如投影和發光效果）由IS使用可附加到影像、文本和實色層的特殊子層來實現。 這些效果層從父層繼承父層掩碼和位置，並且功能有限。
