---
description: 支援四種類型的圖層。
solution: Experience Manager
title: 圖層類型
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 0%

---


# 圖層類型{#layer-types}

支援四種類型的圖層。

## 影像圖層{#section-3e53df1437694272aca03f927fc0db07}

圖層必須有`src=`命令，該命令指定要用作圖層的影像。 可以用`mask=`指定單獨的影像以用作圖層遮罩，或者該影像可以具有α通道。 影像圖層的大小一律是從影像衍生而來，但影像通常會使用`size=`命令縮放以符合影像大小。 剪輯路徑可以與`clipPath=`一起應用。

## 文字圖層{#section-dc2aec6416a340bcb20c1f884323c8d0}

必須有`text=`或`textPs=`命令，該命令以富文本格式(RTF)文本片段的形式提供文本內容。 文字圖層可依其內容自行調整大小，或可以指定明確的大小（例如，如果要將文字包住特定寬度，或文字必須限制在特定區域內）。 `textPs=` 支援將文字流入以定義為任意形狀的 `textFlowPath=` 任意形狀，並移至以定義為任意路徑 `textPath=`。`textPs=` 也支援將文字轉換為文字方塊或以任意角度( `textAngle=`)指定形狀。

## 單色圖層{#section-56dfb672756643dda08dc93294809eb0}

範本中的圖層0通常使用純色圖層，因此複合影像的大小是固定的，且與任何影像內容無關。 實色圖層需要`color=`屬性，以及`size=`或`mask=`，並支援大部分其他命令和屬性來修改外觀。 使用`clipPath=`可以給出任意形狀的單色圖層。

## 效果圖層{#section-dd3b628bc6734077af4c0ddcebcee05f}

Photoshop風格的圖層特效，例如陰影和發光效果，由IS使用特殊的子圖層來實作，子圖層可附加在影像、文字和純色圖層上。 這些效果圖層繼承父圖層遮色片和父圖層的位置，而且功能有限。
