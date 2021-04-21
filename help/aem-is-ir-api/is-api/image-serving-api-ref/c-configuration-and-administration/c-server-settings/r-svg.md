---
description: 只有在需要SVG轉譯時，才需要考慮本節中的設定。
solution: Experience Manager
title: SVG
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 1%

---


# SVG{#svg}

只有在需要SVG轉譯時，才需要考慮本節中的設定。

## SV::SvgHeapSize - SVG堆大小{#section-59ab17681daa4be8b5d794713e1a504e}

SVG轉換器的Java堆大小。 預設為「200m 」(200 MB)。

## PS::svgProvider.rootPaths - SVG資料根資料夾{#section-70fe575b0ad54e3b8b6d3a01ea8f1f44}

SVG源資料檔案的位置。 可以是相對於&#x200B;*[!DNL install_folder]*&#x200B;的一個或多個絕對檔案路徑或路徑，以分號分隔。 通常設定為與`IS::RootPath`相同的值。

## PS::svgProvider.SVGFileSizeLimit —— 最大SVG檔案大小{#section-b9c81e3e104642ebbdd9f000843d3256}

最大SVG源檔案大小（以千位元組為單位）。 當嘗試轉譯大於此限制的SVG檔案時，伺服器會傳回錯誤。 預設值為1024千位元組。

## IS::SvgMAxRenderRgnPixels - SVG輸出影像大小限制{#section-5be1fd9639424d878a5ffd11736d3920}

限制SVGRender可產生的影像大小。 大於0的整數值（以百萬像素為單位）。 如果演算作業超過大小限制，則會傳回錯誤。 預設為 4。

## PS::svgProvider.port —— 平台伺服器監聽埠{#section-f7e42a96c2dd4523b46f0557c239e659}

用於SvgRender的埠，用於從平台伺服器獲取要嵌入到SVG渲染中的影像。

重要資訊：要使SVGRender元件正常工作，必須將此配置選項設定為與`TC::PsPort`相同的值。

## PS::svgProvider.fontRoot - SVG字型檔案資料夾{#section-a8d45b0d68504945b8780f5eac351b0d}

指定SvgRender在何處可找到轉換SVG文本所需的字型檔案；通常為`IS::RootPaths`中指定的路徑之一。 預設值為[!DNL *[!DNL install_folder]*/images]。

## SVG::SVGRender.port,IS::SVGTcpPort - SVG通信埠{#section-608687123aa644b7b58fe42385d71b79}

配置Image Server和SVGRender元件通信的埠。

>[!NOTE]
>
>要使SVGRender元件正常工作，必須為`SVG::SVGRender.port`和`IS::SVGTcpPort`指定相同的埠號。

